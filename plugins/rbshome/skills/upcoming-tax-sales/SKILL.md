---
name: upcoming-tax-sales
description: List RBSHome tax-delinquent leads in Dallas County or Collin County, Texas with the nearest scheduled tax-sale dates, then the user's saved filters with current counts. Use when the user asks about upcoming tax sales, sale dates or what is going to auction soon.
---

# Upcoming tax sales

1. Call `filter_properties` sorted by `next_sale` ascending with `page_size` 25. If the user named Dallas or Collin County, limit it to that county; otherwise include both.
2. For each lead, show the sale date, balance, years delinquent and link. Leave out leads with no scheduled sale date.
3. Call `list_saved_filters` with `with_counts=true` and show each saved filter's current lead count and map link.

Rules:

- Use the dates and figures exactly as returned and cite their data dates.
- Say that sale dates come from county records and can change; the user should confirm with the county before relying on one.
- RBSHome covers only Dallas and Collin counties.
