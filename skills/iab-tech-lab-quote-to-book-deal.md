---
name: iab-tech-lab-quote-to-book-deal
description: Discover a seller's products, check availability, obtain a non-binding quote and book it into a Deal ID against an IAB Tech Lab seller agent (agentic advertising API).
api: iab-tech-lab:seller-agent-api
generated: '2026-09-17'
method: generated
source: openapi/iab-tech-lab-seller-agent-openapi.json, openapi/iab-tech-lab-agentic-advertising-api-openapi.yaml, conventions/iab-tech-lab-conventions.yml
operations:
- list_products_products_get
- get_product_products__product_id__get
- check_avails_products_avails_post
- get_pricing_pricing_post
- create_quote_api_v1_quotes_post
- get_quote_api_v1_quotes__quote_id__get
- book_deal_api_v1_deals_post
- get_deal_api_v1_deals__deal_id__get
---

# Quote-to-book a programmatic direct deal

The seller agent is self-hosted by each publisher: base URL is whatever the operator deployed
(`http://localhost:8000` in the docs). Anonymous calls get public-tier price ranges; send
`Authorization: Bearer <buyer_api_key>` (or `X-Api-Key`) to unlock seat/agency/advertiser pricing.

1. **Browse the catalog** — `list_products_products_get` (`GET /products`, `limit`/`offset` pagination),
   then `get_product_products__product_id__get` for the one you want.
2. **Check inventory** — `check_avails_products_avails_post` (`POST /products/avails`) with the product
   and flight window. Optionally price it first with `get_pricing_pricing_post` (`POST /pricing`), which
   applies the tiered rate card to your buyer identity.
3. **Request a quote** — `create_quote_api_v1_quotes_post` (`POST /api/v1/quotes`). The quote is
   non-binding and carries `QuoteTerms`, `QuotePricing` (Money) and, for linear TV, `CancellationTerms`
   (`notice_days`, `cancellable_pct`, `deadline`). Since 2.4.2 this call is idempotent on
   `idempotency_key` — reuse the same key on retry.
4. **Read it back** — `get_quote_api_v1_quotes__quote_id__get` to confirm status and terms before
   committing.
5. **Book** — `book_deal_api_v1_deals_post` (`POST /api/v1/deals`) with the `quote_id` and a **required
   `idempotency_key`**. This is the commit point: the quote becomes bound and the response is a `Deal`
   with the Deal ID for DSP activation. A replay with the same key returns the same Deal without
   creating a second one. Booking requires a verified buyer key matching the quote (Unreleased changelog).
6. **Verify** — `get_deal_api_v1_deals__deal_id__get`.

Errors: `422` with `{detail:[{loc,msg,type}]}` for validation; `401` when a key is required; `403` when
a buyer key hits an operator route. There is no cancel endpoint — reversal is the seller's
`deprecate`/`migrate` path and the quote's `CancellationTerms` window (see conventions/).
