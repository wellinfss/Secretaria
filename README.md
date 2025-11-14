# Secretaria - Sistema de Integração Chatwoot

Olá! 👋

Este repositório contém a configuração para integração do Chatwoot com Baileys API para WhatsApp.

## Descrição

O projeto utiliza Docker Compose para orquestrar os seguintes serviços:
- **Chatwoot**: Plataforma de atendimento ao cliente
- **Baileys API**: API para integração com WhatsApp
- **PostgreSQL**: Banco de dados (com suporte a pgvector)
- **Redis**: Cache e fila de mensagens
- **Sidekiq**: Processamento de jobs em background
- **n8n**: Automação de workflows

## Configuração

As variáveis de ambiente estão definidas no arquivo `.env` dentro do diretório `chatwoot-local/`.

### Pré-requisitos

- Docker
- Docker Compose

### Como executar

```bash
cd chatwoot-local
docker-compose up -d
```

## Acesso aos serviços

- **Chatwoot**: http://localhost:3000
- **n8n**: http://localhost:5678

## Segurança

⚠️ **Importante**: Os arquivos `Secrets.txt` e `KeyGoogle.txt` estão configurados no `.gitignore` para não serem versionados. Mantenha suas credenciais seguras e nunca as compartilhe publicamente.

## Locale

O sistema está configurado para utilizar o locale `pt_BR` (Português Brasileiro).
