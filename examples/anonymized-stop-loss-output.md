# Anonymized Stop-Loss Output

This example uses synthetic, anonymized data. It is intended to show how the `amazon-product-manager` skill can structure a stop-loss or rework decision without exposing private seller data, advertising reports, supplier quotes, or account screenshots.

## User Request

```text
Use $amazon-product-manager to evaluate whether we should continue, rework, liquidate, or kill an Amazon US SKU.

Product:
- Kitchen storage accessory
- Retail price: $24.99
- Landed cost: $8.20
- FBA/referral/fulfillment estimate: $7.10
- Current contribution margin before ads: about $9.69

Recent performance:
- ACoS is rising from 32% to 48%
- TACoS is rising from 16% to 24%
- Organic rank dropped on two main keywords
- Rating is 4.1 with repeated complaints about fit, finish, and packaging damage
- Inventory cover is about 95 days
- New competitors entered with lower price and more reviews

Goal:
Give a clear stop-loss memo with Continue / Rework / Liquidate / Kill options, risks, missing evidence, and a 14-day action plan.
```

## Decision

`Rework Offer` with a controlled `Stop-Loss Review` path.

The SKU should not continue scaling under the current offer. The combination of rising ACoS/TACoS, organic rank decline, rating weakness, repeated product complaints, and 95 days of inventory cover suggests the problem is not only advertising efficiency. The offer needs product/listing repair and inventory-risk control before more budget is added.

Do not immediately kill the SKU if inventory can still be sold down without destroying brand economics. Do not increase ads until the review and conversion issues are separated from traffic-quality issues.

## Evidence Summary

| Area | Signal | Interpretation |
| --- | --- | --- |
| Margin | Contribution before ads is about $9.69 | There is some room, but not enough for sustained 48% ACoS |
| Advertising | ACoS rose from 32% to 48%, TACoS from 16% to 24% | Paid traffic is no longer converting profitably |
| Organic rank | Two main keywords declined | The listing may be losing relevance, conversion, or competitive position |
| Reviews | Rating 4.1 with repeated fit, finish, and packaging complaints | Product experience is likely hurting conversion and rank |
| Inventory | 95 days of cover | Inventory risk exists but is not yet an emergency liquidation case |
| Competition | Lower-priced competitors with more reviews entered | The current offer may be squeezed between price and trust barriers |

## Scorecard

| Factor | Score | Reason |
| --- | ---: | --- |
| Profit recoverability | 2/5 | Ads and conversion pressure are high |
| Product-fix potential | 3/5 | Complaints are specific enough to investigate |
| Inventory urgency | 3/5 | 95 days cover requires action, but not panic |
| Competitive position | 2/5 | Lower-price and higher-review competitors are pressuring the offer |
| Brand risk | 2/5 | Rating and packaging complaints may continue hurting conversion |
| Data confidence | 3/5 | Enough signals for a stop-loss review, but more cohort data is needed |

Total: 15/30. Recommended interpretation: `Rework Offer` or controlled sell-down, not scale.

## Recommended Path

### Option A: Continue

Not recommended under current evidence.

Only continue if conversion rate, review trend, and unit economics recover after immediate fixes. Continuing ad scale without fixing offer quality would likely accelerate losses.

### Option B: Rework Offer

Recommended first path.

Actions:

- Pause or reduce inefficient campaign segments.
- Separate exact-match winners from broad/auto waste.
- Refresh main image and bullets around the strongest verified use case.
- Address fit, finish, and packaging complaints.
- Request supplier corrective actions before reorder.
- Test a coupon or price adjustment only after margin impact is modeled.

### Option C: Liquidate

Use if rework signals fail within the review window.

Liquidation should be controlled, not panic-driven. Avoid training the market to expect a permanently lower price unless the SKU is being exited.

### Option D: Kill

Use only if the product defect pattern is structural or supplier fixes cannot pass validation.

Kill decision requires evidence that review complaints cannot be repaired without destroying margin, timeline, or brand trust.

## Missing Evidence

| Priority | Gap | Why It Matters | Next Step |
| --- | --- | --- | --- |
| P0 | Search-term report by spend, orders, ACoS, CVR | Identify whether ad waste or offer conversion is the main problem | Pull last 30/60/90 days |
| P0 | Review complaint frequency | Confirm whether fit, finish, and packaging issues are repeated enough to damage conversion | Tag negative reviews |
| P0 | Unit economics after coupon/price change | Avoid fixing conversion by destroying margin | Build margin scenarios |
| P1 | Keyword rank and conversion trend | Separate traffic loss from conversion loss | Compare main keywords weekly |
| P1 | Supplier corrective action | Determine whether quality problems are fixable | Request revised sample/packaging plan |
| P2 | Competitor offer map | Understand if the SKU is losing on price, trust, feature, or images | Compare top 10 direct competitors |

## 14-Day Action Plan

| Day | Action | Output |
| --- | --- | --- |
| 1 | Pull PPC search-term data and split by match type | Waste list and winner list |
| 2 | Tag negative reviews by fit, finish, packaging, size, durability, and expectation mismatch | Complaint frequency table |
| 3 | Recalculate margin under current price, coupon, lower price, and reduced ad spend | Margin scenario table |
| 4 | Pause or reduce worst ad segments | Spend-control log |
| 5 | Rewrite listing claims around verified strengths and remove overpromising | Listing revision draft |
| 6 | Ask supplier for packaging and finish corrective actions | Supplier action plan |
| 7 | Compare top 10 direct competitors by price, review count, rating, images, and offer | Competitor pressure map |
| 8-10 | Run controlled ad/listing test with capped budget | Early CVR and ACoS read |
| 11 | Review inventory sell-through and rank movement | Stop-loss dashboard |
| 12 | Decide whether fixes are working | Rework / liquidate recommendation |
| 13 | Prepare meeting memo | Decision packet |
| 14 | Decide continue controlled rework, start liquidation, or kill reorder | Meeting decision |

## Final Recommendation

Do not scale this SKU in its current form.

Run a 14-day stop-loss review focused on three gates:

1. Can ad waste be cut without losing all sales?
2. Can review complaints be addressed through listing, packaging, or supplier correction?
3. Can the SKU maintain acceptable contribution margin after realistic ads and discounting?

If all three gates improve, continue controlled rework. If one or more gates fail, begin liquidation planning and stop reordering until the product issue is fixed.
