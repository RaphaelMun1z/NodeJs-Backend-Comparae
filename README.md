# Comparae — Backend

API e motor de coleta do Comparae. O backend expõe a API REST, autenticação administrativa, scraping agendado/manual, persistência em MongoDB, busca semântica opcional no Elasticsearch e notificações via Telegram.

## Requisitos

- Node.js 24+
- Docker Desktop, para MongoDB e Elasticsearch

## Desenvolvimento

```bash
copy .env.example .env
npm ci
docker compose -f docker-compose.infra.yml up -d
npm run dev
```

A API ficará disponível em `http://localhost:3000`. O `.env` é exclusivo deste subprojeto e não deve ser commitado.

## Executar tudo com Docker

```bash
docker compose up --build -d
```

Esse comando inicia a API e suas dependências. Para acompanhar os logs, use `docker compose logs -f backend`.

## Scripts

```bash
npm run build
npm start
npm run matching:test
npm run coleta:test
```
