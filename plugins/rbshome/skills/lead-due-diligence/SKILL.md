---
name: lead-due-diligence
description: Research one Dallas County or Collin County, Texas property for a real-estate investor and write a one-page brief from RBSHome public records. Use when the user asks for due diligence, a property brief, or everything RBSHome has on an address, appraisal-district account number or RBSHome lead ID.
---

# Property due diligence

Research the property the user names (a street address, an appraisal-district account number, or an RBSHome lead ID such as Collin:2771234) with the RBSHome tools.

1. If it is already a lead ID (County:account, such as Collin:2771234), use it as is. Otherwise resolve it with `search_properties`; if several properties match, ask the user which one. If it is not in Dallas County or Collin County, say that RBSHome covers only those two Texas counties and stop.
2. Call `get_property` with the sections `terrain`, `history`, `links` and `my_research`.
3. Call `find_owner_portfolio` for the owner's other properties.
4. Call `find_recent_buyers` for companies that bought property nearby.
5. Write a one-page brief with these headings: Snapshot, Tax status, Owner of record, Appraisal values, Terrain and flood, Nearby entity buyers, Open questions. End with the RBSHome link.

Rules:

- Use only numbers the tools returned, and cite each source with its data date.
- Do not estimate a value, ARV or offer price. Texas does not disclose sale prices, and appraised values are the appraisal district's figures, not prices.
- Share `url` values exactly as returned.
- If a section comes back in `section_errors`, say that part could not be loaded rather than guessing.
