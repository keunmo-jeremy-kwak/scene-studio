# Scene Studio - Bridge Platform API Draft

This repository now contains an API-first draft for a dynamic Bridge Platform.

## Added

- `openapi/bridge-platform.yaml`: OpenAPI 3.1 endpoints and schemas for dynamic bridge-page loading, storytelling modules, products, community, ad mediation, rewards, coupons, and analytics.
- `schemas/bridge-page.schema.json`: JSON Schema for bridge page resolve response.
- `schemas/entities.schema.json`: Reusable entity schemas.

## Example flow

1. Ad traffic lands on `/?s=minjung-beauty&utm_campaign=spring_sale`.
2. Frontend calls `GET /api/v1/bridge-pages/resolve`.
3. API returns seller-specific content, products, and CTA config.
4. Frontend logs events to `POST /api/v1/events`.
5. Gamification/coupon endpoints are called based on user actions.
