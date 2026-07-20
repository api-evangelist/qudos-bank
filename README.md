# Qudos Bank (qudos-bank)

Qudos Bank is an Australian customer-owned (mutual) bank, 100% customer-owned since 1959, offering everyday transaction and savings accounts, term deposits, credit cards, home and personal loans, and offset accounts. Following its 2025 merger it now operates as a division of Bank Australia Limited (ABN 21 087 651 607, trading as Qudos Bank). As an Australian authorised deposit-taking institution and a designated data holder under the Consumer Data Right (CDR / Open Banking), it exposes a public Product Reference Data API and supports authenticated CDR consumer data sharing with accredited data recipients.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/qudos-bank/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/qudos-bank/refs/heads/main/apis.yml)

## Tags

- Financial
- Banks
- Open Banking
- CDR
- Consumer Banking
- Australia
- Customer Owned
- Mutual Bank
- Product Reference Data

## Timestamps

- **Created:** 2026-07-20
- **Modified:** 2026-07-20

## APIs

### Qudos Bank CDR Product Reference Data API

Public, unauthenticated Product Reference Data (PRD) API required of every Australian ADI under the Consumer Data Right. Returns Qudos Bank's openly available banking products (transaction and savings accounts, term deposits, credit cards, home and personal loans) with rates, fees, eligibility, and features. Confirmed live returning HTTP 200 JSON with an `x-v` response header (17 products, 4 pages) at the CDS-standard path `GET /cds-au/v1/banking/products` and `/cds-au/v1/banking/products/{productId}`.

- **Human URL:** [https://www.qudosbank.com.au/support/open-banking](https://www.qudosbank.com.au/support/open-banking)
- **Base URL:** `https://public.cdr.qudosbank.com.au/cds-au/v1/banking/products`

#### Tags

- CDR
- Open Banking
- Product Reference Data
- Banking Products
- Public API

#### Properties

- [Documentation](https://www.qudosbank.com.au/support/open-banking)
- [API Reference](https://consumerdatastandardsaustralia.github.io/standards/) — Consumer Data Standards (Data Standards Body)
- [OpenAPI](openapi/qudos-bank-cds-banking-products-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

## Common Properties

- [Website](https://www.qudosbank.com.au/)
- [Documentation](https://www.qudosbank.com.au/support/open-banking)
- [Blog](https://www.qudosbank.com.au/news-tools-tips/news-blog)
- [Terms of Service](https://www.qudosbank.com.au/support/legal)
- [Privacy Policy](https://www.qudosbank.com.au/support/legal/privacy)
- [Support](https://www.qudosbank.com.au/contact-us)
- [LinkedIn](https://www.linkedin.com/company/qudos-bank)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
