# Qudos Bank (qudos-bank)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
