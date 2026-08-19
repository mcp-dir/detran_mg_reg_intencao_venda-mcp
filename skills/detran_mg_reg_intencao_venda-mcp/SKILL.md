---
name: detran_mg_reg_intencao_venda-mcp
description: Skill da REST API do DETRAN MG: Registrar Intenção de Venda de Veículo na MCP.AI: 1 endpoint em /api/detran_mg_reg_intencao_venda. DETRAN MG: Registrar Intenção de Venda de Veículo, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# DETRAN MG: Registrar Intenção de Venda de Veículo — REST API skill

Você tem acesso à **DETRAN MG: Registrar Intenção de Venda de Veículo** REST API na MCP.AI.

> DETRAN MG: Registrar Intenção de Venda de Veículo, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago.

## Base URL

```
https://api.mcp.ai/api/detran_mg_reg_intencao_venda
```

Todo endpoint é um **POST** na Base URL + o path abaixo. Os parâmetros vão no corpo JSON.

## Autenticação

Inclua em toda request:

```
Authorization: Bearer sk_live_...
Content-Type: application/json
```

> Gere sua chave em **https://app.mcp.ai/settings/api-keys** (workspace API key `sk_live_…`, não expira, revogável). Uma única chave serve pra todos os seus MCPs.

## Formato de resposta

```json
{ "ok": true, "tool": "<tool_id>", "result": <payload> }
```

## Exemplo cURL

```bash
curl -X POST https://api.mcp.ai/api/detran_mg_reg_intencao_venda/consultar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{"email_vendedor":"...","placa":"...","chassi":"...","renavam":"...","crv":"...","valor_venda":"...","nome_comprador":"...","email_comprador":"...","cep_comprador":"...","logradouro_endereco_comprador":"...","numero_endereco_comprador":"...","bairro_endereco_comprador":"...","municipio_endereco_comprador":"...","uf_endereco_comprador":"..."}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/detran_mg_reg_intencao_venda/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `detran_mg_reg_intencao_venda_consultar`

DETRAN MG: Registrar Intenção de Venda de Veículo, consulta em fonte oficial. _(POST /api/detran_mg_reg_intencao_venda/consultar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `cpf_vendedor` | string | Não | Parâmetro de consulta "cpf_vendedor". |
| `cnpj_vendedor` | string | Não | Parâmetro de consulta "cnpj_vendedor". |
| `email_vendedor` | string | Sim | Parâmetro de consulta "email_vendedor". |
| `placa` | string | Sim | Parâmetro de consulta "placa". |
| `chassi` | string | Sim | Parâmetro de consulta "chassi". |
| `renavam` | string | Sim | Parâmetro de consulta "renavam". |
| `crv` | string | Sim | Parâmetro de consulta "crv". |
| `hodometro` | string | Não | Parâmetro de consulta "hodometro". |
| `datahora_hodometro` | string | Não | Parâmetro de consulta "datahora_hodometro". |
| `valor_venda` | string | Sim | Parâmetro de consulta "valor_venda". |
| `cpf_comprador` | string | Não | Parâmetro de consulta "cpf_comprador". |
| `cnpj_comprador` | string | Não | Parâmetro de consulta "cnpj_comprador". |
| `nome_comprador` | string | Sim | Parâmetro de consulta "nome_comprador". |
| `email_comprador` | string | Sim | Parâmetro de consulta "email_comprador". |
| `rg_comprador` | string | Não | Parâmetro de consulta "rg_comprador". |
| `cep_comprador` | string | Sim | Parâmetro de consulta "cep_comprador". |
| `logradouro_endereco_comprador` | string | Sim | Parâmetro de consulta "logradouro_endereco_comprador". |
| `numero_endereco_comprador` | string | Sim | Parâmetro de consulta "numero_endereco_comprador". |
| `complemento_endereco_comprador` | string | Não | Parâmetro de consulta "complemento_endereco_comprador". |
| `bairro_endereco_comprador` | string | Sim | Parâmetro de consulta "bairro_endereco_comprador". |
| `municipio_endereco_comprador` | string | Sim | Parâmetro de consulta "municipio_endereco_comprador". |
| `uf_endereco_comprador` | string | Sim | Parâmetro de consulta "uf_endereco_comprador". |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_detran_mg_reg_intencao_venda` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
