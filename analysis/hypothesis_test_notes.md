# Hypothesis Test Notes

## Experiment Objective

The purpose of this experiment is to determine whether the new onboarding and activation campaign (Treatment Group) performs better than the existing onboarding experience (Control Group) in improving user conversion while maintaining healthy business metrics.

---

# Business Decision

The business must decide whether the new onboarding campaign should be rolled out to all users.

This decision impacts:

* Product Team
* Marketing Team
* Customer Success Team
* Business Leadership
* End Users

The decision should be based on statistically significant evidence rather than observed differences alone.

---

# North Star Metric

**Paid Conversion Rate**

Paid Conversion Rate measures the percentage of users who successfully convert from free users to paid subscribers.

**Formula**

Paid Conversion Rate = (Number of Paid Conversions / Total Users) × 100

This metric directly reflects business growth because subscription revenue depends on converting users into paying customers.

---

# Metric Being Tested

**Primary Metric:** Paid Conversion Rate

This metric was selected because:

* It directly measures campaign success.
* It has the strongest relationship with revenue growth.
* It is the primary KPI used by leadership for evaluating onboarding performance.

---

# Null Hypothesis (H₀)

There is **no significant difference** in the Paid Conversion Rate between the Control Group and the Treatment Group.

[
H_0: p_{Treatment} \leq p_{Control}
]

---

# Alternative Hypothesis (H₁)

The Treatment Group has a **higher Paid Conversion Rate** than the Control Group.

[
H_1: p_{Treatment} > p_{Control}
]

---

# Type of Test

**One-Tailed Two-Proportion Z-Test**

A one-tailed test is appropriate because the business objective is specifically to determine whether the new onboarding experience performs **better** than the existing one, not merely whether it is different.

---

# Significance Level

**α = 0.05 (5%)**

Decision Rule:

* If **p-value < 0.05**, reject the Null Hypothesis.
* If **p-value ≥ 0.05**, fail to reject the Null Hypothesis.

---

# Test Inputs

* Population 1: Control Group
* Population 2: Treatment Group
* Success Event: User converted to a paid subscription
* Variable Type: Binary (Converted = 1, Not Converted = 0)

---

# Statistical Test Output

The two-proportion Z-test compares the Paid Conversion Rates of the Control and Treatment groups.

The analysis provides:

* Sample size for each group
* Number of successful conversions
* Conversion rates
* Z-statistic
* P-value

---

# Decision

Based on the hypothesis test:

* Compare the calculated p-value with the significance level (0.05).
* If the p-value is less than 0.05, the Treatment Group demonstrates a statistically significant improvement in Paid Conversion Rate.

---

# Business Interpretation

If the Treatment Group shows a statistically significant increase in Paid Conversion Rate, the new onboarding campaign provides evidence of improved user activation and business value.

However, the rollout decision should not rely solely on conversion improvements.

The following guardrail metrics must also be evaluated:

* Refund Rate
* Support Ticket Rate
* Engagement Score
* Days to Convert
* Revenue Quality

Only if these metrics remain stable or improve should the campaign be considered for a full launch.

---

# Assumptions

The hypothesis test assumes:

* Users were randomly assigned to Control and Treatment groups.
* Observations are independent.
* Sample sizes are sufficiently large for normal approximation.
* Conversion outcomes are binary.
* Data accurately reflects user behavior during the experiment.

---

# Conclusion

The hypothesis test provides statistical evidence to support the business decision. If the Treatment Group achieves a significantly higher Paid Conversion Rate without negatively affecting guardrail metrics, the recommendation is to proceed with launching the new onboarding experience to a broader user base.
