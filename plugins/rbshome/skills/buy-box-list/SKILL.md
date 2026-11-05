---
name: buy-box-list
description: Build a tax-delinquent lead list in Dallas County or Collin County, Texas from the user's buy box with RBSHome. Use when the user describes criteria such as tier, score, lot size, property use, ZIP codes, appraised value, years delinquent or owner location and wants matching leads.
---

# Buy-box lead list

Turn the user's criteria into an RBSHome lead list.

1. If the user has not said Dallas or Collin County, ask which one. RBSHome covers only those two Texas counties.
2. If the criteria need attribute filters (for example road frontage, flood zone, slope or zoning), call `list_filter_fields` first and use only the keys it returns. Never guess a field key.
3. Call `filter_properties` with `count_only=true` and report the count with its data date.
4. Call `filter_properties` again for page 1, sorted by `levy` descending (largest balance first). Show each lead's address, owner of record, tier, balance, years delinquent and link, then the `map_url`.
5. Offer to save the filter with `save_filter`. Save it only if the user agrees, using the name they give.

Rules:

- Report counts and figures exactly as returned, with their data dates.
- No sale prices: Texas does not disclose them. Land values are appraisal-district (CAD) figures; for offer math on one lead use analyze_deal.
- If a daily limit is reached, tell the user when it resets and suggest narrowing the filter or counting first.
