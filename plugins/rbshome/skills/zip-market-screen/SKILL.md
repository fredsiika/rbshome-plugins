---
name: zip-market-screen
description: Rank ZIP codes in Dallas County or Collin County, Texas by tax-delinquent lead supply and ownership transfers with RBSHome. Use when the user wants to compare ZIP codes, find where Tier A leads concentrate, or see where parcels are changing hands.
---

# ZIP code screen

1. If the user has not said Dallas or Collin County, ask which one.
2. Call `get_market_stats` with that county and `sort_by` set to `tier_a`.
3. Show the top 15 ZIP codes with Tier A leads, all leads, parcels that changed owners in the last 12 months, and the share bought by entities, each with its map link.
4. Show the caveats exactly as returned.

Rules:

- Do not add prices, days on market or sell-through rates. Texas does not disclose sale prices, and the data has none.
- Cite the sources and data dates the tool returns.
