---
license: cc-by-4.0
language:
  - en
pretty_name: ShirtMap Local Merch Index
tags:
  - commerce
  - retail
  - local-business
  - apparel
  - prices
  - united-states
size_categories:
  - n<1K
---

# ShirtMap Local Merch Index

T-shirts from real, named local businesses across the United States: what they cost, who sells them, and where those businesses are. Every row is a public listing on [ShirtMap](https://shirtmap.com), a map-based marketplace for local-business merch (brewery tees, bookshop shirts, hometown designs).

This is first-party data: ShirtMap operates the marketplace the rows describe. Prices for externally sold shirts are re-verified against the seller's own website on an automated daily cycle.

## Live source

The canonical, always-current dataset is served by ShirtMap itself:

- CSV: https://shirtmap.com/data/local-merch-index.csv
- JSON (includes computed statistics): https://shirtmap.com/data/local-merch-index.json
- Human-readable statistics page: https://shirtmap.com/data

The files in this repository are periodic snapshots. For analysis that needs current data, fetch the live URLs.

## Schema

| Column | Type | Description |
|---|---|---|
| shirt_name | string | Listing title as shown on ShirtMap |
| business_name | string | The named local business selling or making the shirt |
| business_type | string | Business category (Brewery / Bar, Bookshop, Retail, ...) |
| town | string | The business's town |
| state | string | Two-letter US state or territory code |
| price_usd | string | Price in USD; empty when the listing is unpriced |
| price_max_usd | string | Top of a variant price range, when the store charges one; else empty |
| sold_on_shirtmap | bool string | true when the shirt is purchasable on ShirtMap with checkout |
| listing_url | string | The listing's public page on ShirtMap |
| updated | date | Date the listing's details last changed (YYYY-MM-DD) |

USD listings only. All fields are already public on the corresponding listing pages.

## License and citation

Creative Commons Attribution 4.0 (CC BY 4.0). Use it in research, journalism, or products, with credit.

Cite as: ShirtMap Local Merch Index, https://shirtmap.com/data

```bibtex
@misc{shirtmap_local_merch_index,
  title        = {ShirtMap Local Merch Index},
  author       = {{ShirtMap}},
  year         = {2026},
  howpublished = {\url{https://shirtmap.com/data}},
  note         = {Licensed under CC BY 4.0}
}
```

## About ShirtMap

ShirtMap is a small, independently run marketplace where every listing traces to a reviewed, named, located business. There are no anonymous sellers and no mass-generated catalogs; the authenticity policy is at https://shirtmap.com/authenticity.
