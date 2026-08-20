# Instalação rápida

Cidadão MG Veículos: Transferência de Propriedade de Veículo é um servidor MCP remoto hospedado em `https://api.mcp.ai/p_cidadao_mg_veiculos_trans_prop`. Você não baixa nem roda nada localmente — só aponta seu cliente pra essa URL.

A auth acontece em runtime: clientes com **OAuth 2.1** (Claude Desktop, Cursor, VS Code recentes) abrem o browser na 1ª chamada (magic-link). Clientes sem OAuth recebem a tool `authenticate` — abra `https://app.mcp.ai/agent-auth`, faça login, copie o JWT e cole no chat.

---

## Claude (Web e Desktop)

[➕ Abrir no Claude e conectar](https://claude.ai/new?modal=add-custom-connector#settings/customize-connectors)

Manual: [claude.ai/customize/connectors](https://claude.ai/customize/connectors?surface=cowork) → **+** → **Adicionar conector personalizado** → `Cidadão MG Veículos: Transferência de Propriedade de Veículo` / `https://api.mcp.ai/p_cidadao_mg_veiculos_trans_prop`.

Config file (legado): `~/Library/Application Support/Claude/claude_desktop_config.json` (macOS) ou `%APPDATA%\Claude\claude_desktop_config.json` (Windows):

```json
{ "mcpServers": { "cidadao_mg_veiculos_trans_prop": { "type": "http", "url": "https://api.mcp.ai/p_cidadao_mg_veiculos_trans_prop" } } }
```

## Cursor

[➕ Instalar no Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=cidadao_mg_veiculos_trans_prop&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF9jaWRhZGFvX21nX3ZlaWN1bG9zX3RyYW5zX3Byb3AifQ==)

`.cursor/mcp.json`:
```json
{ "mcpServers": { "cidadao_mg_veiculos_trans_prop": { "url": "https://api.mcp.ai/p_cidadao_mg_veiculos_trans_prop" } } }
```

## VS Code (Copilot Chat)

[➕ Instalar no VS Code](vscode:mcp/install?name=cidadao_mg_veiculos_trans_prop&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_cidadao_mg_veiculos_trans_prop%22%7D)

`.vscode/mcp.json`:
```json
{ "servers": { "cidadao_mg_veiculos_trans_prop": { "type": "http", "url": "https://api.mcp.ai/p_cidadao_mg_veiculos_trans_prop" } } }
```

## Outros clientes MCP

Qualquer cliente com **MCP over HTTP**. URL fixa:

```
https://api.mcp.ai/p_cidadao_mg_veiculos_trans_prop
```

Dúvidas? [cidadao_mg_veiculos_trans_prop@mcp.ai](mailto:cidadao_mg_veiculos_trans_prop@mcp.ai)
