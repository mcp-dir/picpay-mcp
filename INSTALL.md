# Instalação rápida

PicPay MCP é um servidor MCP remoto hospedado em `https://api.mcp.ai/p_picpay`. Você não baixa nem roda nada localmente — só aponta seu cliente pra essa URL.

A auth acontece em runtime: clientes com **OAuth 2.1** (Claude Desktop, Cursor, VS Code recentes) abrem o browser na 1ª chamada (magic-link). Clientes sem OAuth recebem a tool `authenticate` — abra `https://app.mcp.ai/agent-auth`, faça login, copie o JWT e cole no chat.

---

## Claude (Web e Desktop)

[➕ Abrir no Claude e conectar](https://claude.ai/customize/connectors?modal=add-custom-connector&mcpName=PicPay%20MCP&mcpServerUrl=https%3A%2F%2Fapi.mcp.ai%2Fp_picpay)

Manual: [claude.ai/customize/connectors](https://claude.ai/customize/connectors) → **+** → **Adicionar conector personalizado** → `PicPay MCP` / `https://api.mcp.ai/p_picpay`.

Config file (legado): `~/Library/Application Support/Claude/claude_desktop_config.json` (macOS) ou `%APPDATA%\Claude\claude_desktop_config.json` (Windows):

```json
{ "mcpServers": { "picpay": { "type": "http", "url": "https://api.mcp.ai/p_picpay" } } }
```

## Cursor

[➕ Instalar no Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=picpay&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF9waWNwYXkifQ==)

`.cursor/mcp.json`:
```json
{ "mcpServers": { "picpay": { "url": "https://api.mcp.ai/p_picpay" } } }
```

## VS Code (Copilot Chat)

[➕ Instalar no VS Code](vscode:mcp/install?name=picpay&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_picpay%22%7D)

`.vscode/mcp.json`:
```json
{ "servers": { "picpay": { "type": "http", "url": "https://api.mcp.ai/p_picpay" } } }
```

## Outros clientes MCP

Qualquer cliente com **MCP over HTTP**. URL fixa:

```
https://api.mcp.ai/p_picpay
```

Dúvidas? [picpay@mcp.ai](mailto:picpay@mcp.ai)
