---
name: List Qudos Bank products
description: >-
  Retrieve Qudos Bank's openly available banking products (accounts, term
  deposits, cards, loans) from the public, unauthenticated CDR Product Reference
  Data API, with category filtering and pagination.
api: openapi/qudos-bank-cds-banking-products-openapi.yml
operations: [listBankingProducts]
---

# List Qudos Bank products

Use this skill to browse the products Qudos Bank currently offers. This is a
public Consumer Data Right (CDR) Product Reference Data endpoint — **no
authentication, API key, or token is required.**

## Endpoint

`GET https://public.cdr.qudosbank.com.au/cds-au/v1/banking/products`
(operationId `listBankingProducts`)

## Required convention

- Always send the version header **`x-v: 3`** (the version the endpoint serves).
  Omitting it can return `400 Missing Required Header`
  (`urn:au-cds:error:cds:header/missing`); an unsupported value returns
  `406 Unsupported Version`.

## Steps

1. Call `GET /banking/products` with header `x-v: 3`.
2. Optionally narrow with query params:
   - `product-category` — a CDS category enum such as
     `TRANS_AND_SAVINGS_ACCOUNTS`, `TERM_DEPOSITS`, `CRED_AND_CHRG_CARDS`,
     `RESIDENTIAL_MORTGAGES`, `PERS_LOANS`.
   - `updated-since` — ISO date-time to return only recently changed products.
3. Paginate with `page` (1-based) and `page-size`. Read `meta.totalRecords` and
   `meta.totalPages`; follow `links.next` until it is absent.
4. Each item carries `productId`, `name`, `productCategory`, `description`,
   `brand`, `applicationUri`, and an `additionalInformation` block of overview /
   eligibility / fees URIs. Pass a `productId` to the
   **get-product-detail** skill for rates, fees and features.

## Error handling

Errors use the CDS envelope `{ errors: [ { code, title, detail } ] }`
(see `errors/qudos-bank-problem-types.yml`). Common codes:
`urn:au-cds:error:cds:field/invalid-page-size` (400),
`urn:au-cds:error:cds:field/invalid-page` (422).

Idempotency: this is a read-only GET — safe to retry.
