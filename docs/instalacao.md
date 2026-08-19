# Instalação detalhada

DETRAN MG: Registrar Intenção de Venda de Veículo é um servidor MCP remoto. Aponte seu cliente pra `https://api.mcp.ai/p_detran_mg_reg_intencao_venda`. Snippets rápidos: [INSTALL.md](../INSTALL.md).

| Cliente | URL | Auth |
|---|---|---|
| Claude Desktop | `https://api.mcp.ai/p_detran_mg_reg_intencao_venda` | OAuth 2.1 ou agent-auth |
| Cursor | `https://api.mcp.ai/p_detran_mg_reg_intencao_venda` | OAuth 2.1 ou agent-auth |
| VS Code (Copilot) | `https://api.mcp.ai/p_detran_mg_reg_intencao_venda` | OAuth 2.1 ou agent-auth |

A config JSON é a mesma em todos: só a URL, sem headers.

## Desinstalar

Remova o bloco `mcpServers.detran_mg_reg_intencao_venda` (ou `servers.detran_mg_reg_intencao_venda` no VS Code) do config do cliente e reinicie.
