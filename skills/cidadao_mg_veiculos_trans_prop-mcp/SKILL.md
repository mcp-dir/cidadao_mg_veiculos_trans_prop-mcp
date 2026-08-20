---
name: cidadao_mg_veiculos_trans_prop-mcp
description: Skill da REST API do Cidadão MG Veículos: Transferência de Propriedade de Veículo na MCP.AI: 1 endpoint em /api/cidadao_mg_veiculos_trans_prop. Cidadão MG Veículos: Transferência de Propriedade de Veículo, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# Cidadão MG Veículos: Transferência de Propriedade de Veículo — REST API skill

Você tem acesso à **Cidadão MG Veículos: Transferência de Propriedade de Veículo** REST API na MCP.AI.

> Cidadão MG Veículos: Transferência de Propriedade de Veículo, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago.

## Base URL

```
https://api.mcp.ai/api/cidadao_mg_veiculos_trans_prop
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
curl -X POST https://api.mcp.ai/api/cidadao_mg_veiculos_trans_prop/consultar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{"placa":"...","chassi":"...","renavam":"...","valor_venda":"...","crv":"...","email_vendedor":"...","nome_comprador":"...","email_comprador":"...","cep_comprador":"...","uf_comprador":"...","municipio_comprador":"...","numero_endereco_comprador":"..."}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/cidadao_mg_veiculos_trans_prop/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `cidadao_mg_veiculos_trans_prop_consultar`

Cidadão MG Veículos: Transferência de Propriedade de Veículo, consulta em fonte oficial. _(POST /api/cidadao_mg_veiculos_trans_prop/consultar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `login_cpf` | string | Não | Parâmetro de consulta "login_cpf". |
| `login_senha` | string | Não | Parâmetro de consulta "login_senha". |
| `pkcs12_cert` | string | Não | Parâmetro de consulta "pkcs12_cert". |
| `pkcs12_pass` | string | Não | Parâmetro de consulta "pkcs12_pass". |
| `placa` | string | Sim | Parâmetro de consulta "placa". |
| `chassi` | string | Sim | Parâmetro de consulta "chassi". |
| `renavam` | string | Sim | Parâmetro de consulta "renavam". |
| `valor_venda` | string | Sim | Parâmetro de consulta "valor_venda". |
| `crv` | string | Sim | Parâmetro de consulta "crv". |
| `quilometragem_hodometro` | string | Não | Parâmetro de consulta "quilometragem_hodometro". |
| `data_hora_hodometro` | string | Não | Parâmetro de consulta "data_hora_hodometro". |
| `cpf_vendedor` | string | Não | Parâmetro de consulta "cpf_vendedor". |
| `cnpj_vendedor` | string | Não | Parâmetro de consulta "cnpj_vendedor". |
| `email_vendedor` | string | Sim | Parâmetro de consulta "email_vendedor". |
| `cpf_comprador` | string | Não | Parâmetro de consulta "cpf_comprador". |
| `cnpj_comprador` | string | Não | Parâmetro de consulta "cnpj_comprador". |
| `nome_comprador` | string | Sim | Parâmetro de consulta "nome_comprador". |
| `email_comprador` | string | Sim | Parâmetro de consulta "email_comprador". |
| `cep_comprador` | string | Sim | Parâmetro de consulta "cep_comprador". |
| `uf_comprador` | string | Sim | Parâmetro de consulta "uf_comprador". |
| `municipio_comprador` | string | Sim | Parâmetro de consulta "municipio_comprador". |
| `logradouro_endereco_comprador` | string | Não | Parâmetro de consulta "logradouro_endereco_comprador". |
| `bairro_endereco_comprador` | string | Não | Parâmetro de consulta "bairro_endereco_comprador". |
| `numero_endereco_comprador` | string | Sim | Parâmetro de consulta "numero_endereco_comprador". |
| `complemento_endereco_comprador` | string | Não | Parâmetro de consulta "complemento_endereco_comprador". |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_cidadao_mg_veiculos_trans_prop` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
