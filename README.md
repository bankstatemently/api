# Bankstatemently API

**Convert bank statement PDFs into structured data — CSV, Excel, JSON, QBO, and Xero-compatible formats.**

→ **Full documentation:** [bankstatemently.com/developers/api](https://bankstatemently.com/developers/api)
→ **Interactive docs:** [Postman collection](https://documenter.getpostman.com/view/52862871/2sBXcKBHki)
→ **MCP server:** [bankstatemently.com/developers/mcp](https://bankstatemently.com/developers/mcp)

---

## Overview

The Bankstatemently API lets you programmatically convert bank statement PDFs into clean, structured financial data. Upload a PDF, poll for completion, then export in the format your application needs.

**Base URL:** `https://api.bankstatemently.com/v1`

**Authentication:** API key via `X-API-Key` header. Get your key at [bankstatemently.com/developers](https://bankstatemently.com/developers).

---

## Quick Start

```bash
# 1. Upload a PDF
curl -X POST https://api.bankstatemently.com/v1/documents \
  -H "X-API-Key: your_api_key" \
  -F "file=@statement.pdf"

# 2. Poll for completion
curl https://api.bankstatemently.com/v1/documents/{id} \
  -H "X-API-Key: your_api_key"

# 3. Export as CSV
curl https://api.bankstatemently.com/v1/documents/{id}/export/csv \
  -H "X-API-Key: your_api_key"
```

---

## Endpoints

| Method | Path | Description |
|--------|------|-------------|
| `POST` | `/v1/documents` | Upload a bank statement PDF |
| `GET` | `/v1/documents/{id}` | Check processing status |
| `GET` | `/v1/documents/{id}/export/json` | Export as JSON |
| `GET` | `/v1/documents/{id}/export/csv` | Export as CSV |
| `GET` | `/v1/documents/{id}/export/xlsx` | Export as Excel |
| `GET` | `/v1/documents/{id}/export/qbo` | Export as QBO (QuickBooks) |
| `GET` | `/v1/documents/{id}/export/xero` | Export as Xero CSV |
| `GET` | `/v1/credits` | Get current credit balance |

---

## OpenAPI Spec

The full OpenAPI 3.1.0 spec is in [`openapi.yaml`](./openapi.yaml).

You can import it directly into Postman, Insomnia, or any OpenAPI-compatible tool.

---

## Supported Banks

Works with **any bank worldwide** — upload a statement and the API handles detection automatically. A growing set of banks are independently accuracy-verified with published benchmark results.

→ [View accuracy-verified banks](https://bankstatemently.com/banks)

---

## Links

- Website: [bankstatemently.com](https://bankstatemently.com)
- API docs: [bankstatemently.com/developers/api](https://bankstatemently.com/developers/api)
- MCP server: [bankstatemently.com/developers/mcp](https://bankstatemently.com/developers/mcp)
- Postman: [View collection](https://documenter.getpostman.com/view/52862871/2sBXcKBHki)
- Support: [help@bankstatemently.com](mailto:help@bankstatemently.com)
