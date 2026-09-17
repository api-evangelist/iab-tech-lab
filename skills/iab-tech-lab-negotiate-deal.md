---
name: iab-tech-lab-negotiate-deal
description: Run a multi-round price negotiation with an IAB Tech Lab seller agent — submit a proposal, read counters, message the negotiation, and settle on terms before booking.
api: iab-tech-lab:seller-agent-api
generated: '2026-09-17'
method: generated
source: openapi/iab-tech-lab-seller-agent-openapi.json (Proposals, Negotiation tags), https://iabtechlab.github.io/buyer-agent/guides/negotiation/
operations:
- search_media_kit_media_kit_search_post
- submit_proposal_proposals_post
- counter_proposal_proposals__proposal_id__counter_post
- get_negotiation_status_proposals__proposal_id__negotiation_get
- post_negotiation_message_api_v1_negotiations_messages_post
- create_quote_api_v1_quotes_post
- book_deal_api_v1_deals_post
---

# Negotiate, then book

Authenticate as a buyer (`Authorization: Bearer <buyer_api_key>`) — negotiation is a tiered feature
that anonymous callers do not get.

1. **Find inventory** — `search_media_kit_media_kit_search_post` (`POST /media-kit/search`) with an
   `AudienceFilterModel`, or browse `GET /media-kit/packages`.
2. **Quote first** — the pricing guide documents a quote-then-propose sequence: call
   `create_quote_api_v1_quotes_post` so the proposal anchors on a real `QuotePricing`.
3. **Propose** — `submit_proposal_proposals_post` (`POST /proposals`) with your target CPM and terms.
   Since 2.4.0 a failed proposal returns a structured `errors[]` (`ProposalErrorDetail`) rather than a
   bare message — read it before retrying.
4. **Read the seller's move** — `get_negotiation_status_proposals__proposal_id__negotiation_get`
   returns `NegotiationRoundResponse` (`NegotiationRound` with `NegotiationAction`, `Money`, and a
   `NegotiationStatus`).
5. **Counter or message** — `counter_proposal_proposals__proposal_id__counter_post` for a new price, or
   `post_negotiation_message_api_v1_negotiations_messages_post` (`POST /api/v1/negotiations/messages`,
   a `NegotiationMessage` carrying `BuyerIdentity` and an action) for free-text or structured moves.
   Respect the buyer strategy caps (target CPM, max CPM, concession limits) the buyer-agent guide describes.
6. **Settle** — when the status reaches an accepted round, book with `book_deal_api_v1_deals_post` using
   the agreed quote and a required `idempotency_key`.

Every write here is a 422-validated JSON body; pagination on the list calls is `limit`/`offset`.
