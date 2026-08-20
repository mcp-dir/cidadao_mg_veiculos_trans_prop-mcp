# Instalação detalhada

Cidadão MG Veículos: Transferência de Propriedade de Veículo é um servidor MCP remoto. Aponte seu cliente pra `https://api.mcp.ai/p_cidadao_mg_veiculos_trans_prop`. Snippets rápidos: [INSTALL.md](../INSTALL.md).

| Cliente | URL | Auth |
|---|---|---|
| Claude Desktop | `https://api.mcp.ai/p_cidadao_mg_veiculos_trans_prop` | OAuth 2.1 ou agent-auth |
| Cursor | `https://api.mcp.ai/p_cidadao_mg_veiculos_trans_prop` | OAuth 2.1 ou agent-auth |
| VS Code (Copilot) | `https://api.mcp.ai/p_cidadao_mg_veiculos_trans_prop` | OAuth 2.1 ou agent-auth |

A config JSON é a mesma em todos: só a URL, sem headers.

## Desinstalar

Remova o bloco `mcpServers.cidadao_mg_veiculos_trans_prop` (ou `servers.cidadao_mg_veiculos_trans_prop` no VS Code) do config do cliente e reinicie.
