# tiktok-shop-commission-rates-impact

## **Project Summary**

TikTok Shop currently operates on a uniform 8% commission model for all influencers. This project evaluates a proposed policy change for March 1, 2026, which would increase the commission to 15% for "large" influencers (those with 50,000+ followers). The core objective is to determine if this nearly doubled payout generates enough incremental sales to justify the increased cost to the platform.

## **DAG Analysis**

To identify the causal effect of the commission increase, we mapped the relationships between the platform's variables. The DAG identifies Commission (D) as the treatment and Sales (Y) as the outcome.

The Running Variable (R) is the follower count, with a strict Cutoff (c) at 50,000. We identified two primary confounders:

Creator Ability (alpha_i): Unobserved traits like persuasiveness or content quality that influence both follower growth and sales.

Time Shocks (Time_FE): Monthly seasonality (e.g., platform-wide demand spikes)

## **Method Used**

We employed four distinct econometric strategies to ensure the results were robust across different assumptions:

Sharp Regression Discontinuity (RD): Compared creators just above the 50K threshold to those just below it during March 2026. This isolates the effect of the "jump" in commission for nearly identical influencers.

Fuzzy RD: Accounted for imperfect enforcement where some creators near the 50K mark might receive the 15% rate.

Fixed Effects (FE) Model: Analyzed within-creator changes from February to March. This allowed us to control for time-invariant traits (alpha_i) by using each creator as their own control group.

Difference-in-Differences (DiD): Compared the change in sales for the "Treated" group (50K+ followers) against the "Control" group (<50K followers) over the Feb–Mar period.


## **Result of Analysis**

Across all models, the analysis yielded a statistically non-significant result. We found no statistically significant evidence that increasing the commission rate from 8% to 15% led to a short-run increase in sales.

While 50K+ creators do have higher average sales, the data suggests this is due to their existing scale and inherent ability, not the higher commission.

Large influencers appear relatively inelastic to marginal commission changes in the short term, possibly because they are already operating near their content production capacity.

The estimated treatment effects were economically small and failed to pass standard significance thresholds(p>0.05).

## **Business Implications to Clients**

Our findings indicate that increasing commission from 8% to 15% for creators above 50,000 followers does not produce a measurable short-run increase in sales. This suggests that a uniform commission increase for large creators may raise payout costs without generating proportional revenue gains.

Rather than implementing a blanket policy, TikTok should consider more targeted incentive designs, such as performance, based bonuses or tiered commission structures focused on high-growth or mid-tier creators. Additionally, longer-term data or pilot experiments may help identify dynamic or heterogeneous responses that are not captured in this short panel setting.
