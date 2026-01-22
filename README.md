# posopen-core

The domain engine of the posOpen platform.

This repository contains the **pure business logic** for point-of-sale operations:
products, pricing, transactions, inventory, tax, and receipts.

It is intentionally boring.

## What Lives Here
- Product & pricing models
- Sales transactions
- Tax / VAT calculation (region-aware)
- Inventory adjustments
- Refunds and voids
- Receipt data structures (not rendering)

## What Does NOT Live Here
- UI code
- Database code
- HTTP APIs
- Payment provider logic
- Framework-specific glue

## Design Principles
- Deterministic behavior
- Side-effect free where possible
- Explicit state transitions
- Testability over cleverness

## Consumers
This package is consumed by:
- `posopen-api`
- `posopen-sync`
- Client applications via adapters

## Stability Contract
Breaking changes here are **major version events**.

If in doubt: make it smaller.
