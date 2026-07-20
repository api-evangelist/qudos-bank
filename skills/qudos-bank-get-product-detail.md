---
name: Get Qudos Bank product detail
description: >-
  Fetch full detail for a single Qudos Bank product — rates, fees, features,
  eligibility, constraints and bundles — by productId from the public,
  unauthenticated CDR Product Reference Data API.
api: openapi/qudos-bank-cds-banking-products-openapi.yml
operations: [getBankingProductDetail]
---

# Get Qudos Bank product detail

Use this skill after **list-products** to retrieve everything about one product.
Public CDR endpoint — **no authentication required.**

## Endpoint

`GET https://public.cdr.qudosbank.com.au/cds-au/v1/banking/products/{productId}`
(operationId `getBankingProductDetail`)

## Steps

1. Obtain a `productId` from `listBankingProducts`.
2. Call `GET /banking/products/{productId}` with header `x-v: 3`.
3. The response `data` is a `BankingProductDetailV7`: the summary fields plus
   child collections —
   - `depositRates[]` and `lendingRates[]` (each with `tiers[]`),
   - `fees[]`, `features[]`, `constraints[]`, `eligibility[]`, `bundles[]`,
   - `instalments`, and `additionalInformation` URIs.
   See `data-model/qudos-bank-data-model.yml` for the entity graph.

## Error handling

CDS error envelope `{ errors: [ { code, title, detail } ] }`. Expect:
- `404 urn:au-cds:error:cds:resource/unavailable` — unknown/withdrawn productId,
- `404 urn:au-cds:error:cds:resource/invalid` — malformed productId,
- `406 urn:au-cds:error:cds:header/unsupported-version` — bad `x-v`.

Idempotency: read-only GET — safe to retry.
