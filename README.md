# Marketing Funnel & Campaign ROI Analytics

An end-to-end analysis of marketing performance across 6 channels and 12 campaigns: data cleaning in Python and SQL, and an interactive Power BI dashboard covering ROAS, CPA, CTR and the conversion funnel.

> **Note:** The dataset is synthetic. Some channels have unusually high revenue-to-spend ratios, so this project demonstrates method, not real marketing results.

![Dashboard](images/1_dashboard.png)

## Questions answered
- Which channels and campaigns return the most per dollar spent?
- Where is budget being wasted?
- Where does the funnel lose the most people?

## Tools
Python (pandas) · MySQL · Power BI (DAX)

## Data cleaning
- [What you fixed, e.g. removed duplicates, standardized channel/campaign names, fixed date formats, handled missing values]
- [Rows before and after cleaning, if you know them]
- Cleaned data loaded into MySQL (`marketing_analytics` database) and queried for totals by channel, campaign and month

## DAX measures
- ROAS = Revenue / Spend
- CPA = Spend / Conversions
- CTR = Clicks / Impressions
- Conversion rate = Conversions / Clicks

## Key findings
1. **Video and Display take 33% of spend but deliver 1.2% of revenue.** Display spent $171K and returned $110K, a net loss of about $60K (0.7x ROAS, $127 CPA).
2. **Paid Search is the best place to move budget:** the largest spend ($571K) at 21.7x ROAS and a $6 CPA.
3. **Email shows a 785x ROAS (68% of revenue on 3% of spend).** This is unrealistic, so it is flagged as a data-quality outlier and should be validated before any budget is shifted.
4. **Funnel:** [impressions] impressions, [clicks] clicks, 470,530 conversions (3.25% CTR, 6.04% click-to-conversion).

## Limitations
- Synthetic data, so findings don't reflect a real business.
- The Key Insights panel in the dashboard is static text and does not update with filters.

## Repository structure
- `scripts/`: Python cleaning scripts and SQL queries
- `dashboard/`: Power BI file and PDF export
- `images/`: dashboard screenshots
