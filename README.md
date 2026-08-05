# Bankstatemently API

Bankstatemently API — turn bank statement PDFs into structured, spreadsheet-ready data. OpenAPI spec + integration guide.

Current spec version: `1.0.0`.

## What this API does

Send a bank statement PDF, get back structured accounts, transactions, and
metadata as JSON — or a ready-to-import CSV, XLSX, QBO, or Xero file.

## Auth

API key auth: pass `X-API-Key: bsk_live_...` on every request. Generate a
key from your [dashboard](https://bankstatemently.com/developers).

## Spec

`openapi.json` in this repo is copied verbatim from the canonical,
contract-tested spec on every sync — it is generated output, never hand-edited
here. The same spec is served live at
[`/v1/openapi.json`](https://api.bankstatemently.com/v1/openapi.json).

## Docs

Full integration guide: [https://bankstatemently.com/developers](https://bankstatemently.com/developers)
