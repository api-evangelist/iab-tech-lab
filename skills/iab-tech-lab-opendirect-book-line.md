---
name: iab-tech-lab-opendirect-book-line
description: Book guaranteed inventory through the OpenDirect 1.5.1 standard — create an order and line under an account, assign a creative, reserve, book, and know how to cancel or reset.
api: iab-tech-lab:opendirect-api
generated: '2026-09-17'
method: generated
source: openapi/iab-tech-lab-opendirect-1-5-1-swagger.yaml (no operationIds declared — steps cite method + path), mcp/iab-tech-lab-opendirect-mcp-tools.json
operations:
- POST /products/search
- POST /products/avails
- POST /accounts/{accountId}/orders
- POST /accounts/{accountId}/orders/{orderId}/lines
- POST /accounts/{accountId}/creatives
- POST /accounts/{accountId}/assignments
- PUT /accounts/{accountId}/orders/{orderId}/lines/{lineId}?reserve
- PUT /accounts/{accountId}/orders/{orderId}/lines/{lineId}?book
- PUT /accounts/{accountId}/orders/{orderId}/lines/{lineId}?cancel
- PUT /accounts/{accountId}/orders/{orderId}/lines/{lineId}?reset
- GET /accounts/{accountId}/orders/{orderId}/lines/{lineId}/stats
---

# Book an OpenDirect line

OpenDirect is a standard, not a hosted service: point at the seller's own base URL (the contract's
`opendirect.example.com/v1.5.1` is a placeholder) and use the OAuth 2.0 token that seller issues. In
MCP form the same flow is `search_products` -> `create_order` -> `create_line` -> `create_creative` ->
`create_assignment` (mcp/iab-tech-lab-opendirect-mcp-tools.json, OpenDirect 2.1).

1. **Find product** — `POST /products/search` (`ProductSearch`), then `POST /products/avails`
   (`ProductAvailsSearch`) for impressions in your flight.
2. **Create the order** — `POST /accounts/{accountId}/orders` (`Order`: dates, budget, currency).
3. **Add a line** — `POST /accounts/{accountId}/orders/{orderId}/lines` (`Line` referencing the
   `productId`); it starts in **Draft**.
4. **Creative** — `POST /accounts/{accountId}/creatives`, then bind it with
   `POST /accounts/{accountId}/assignments` (`Assignment` = line + creative). Required before booking
   unless the product's `AllowNoCreative` is true.
5. **Reserve (optional hold)** — `PUT .../lines/{lineId}?reserve`: Draft -> Reserved, may be
   asynchronous; a Declined result sets `StateChangedReason`.
6. **Book** — `PUT .../lines/{lineId}?book` from Draft or Reserved: moves to **Booked** (or Declined).
   Poll the line until the state settles — booking may be asynchronous.
7. **Measure** — `GET .../lines/{lineId}/stats`.

Reversal: `PUT .../lines/{lineId}?cancel` works only while the line is **Reserved, Booked, or
InFlight** and moves it to Canceled; `?reset` returns a Reserved, Declined or Expired line to Draft.
Errors: 400 (validation), 401 (token), 404 (unknown account/order/line), 500 (retry with backoff).
