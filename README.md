# Part 2 – KPI Experiment Analysis

## Business Context

A subscription-based digital product company launched a new onboarding and activation campaign to improve user conversion and early engagement. To evaluate the effectiveness of the campaign, an A/B experiment was conducted where users were randomly assigned to one of two groups:

* **Control Group:** Existing onboarding experience
* **Treatment Group:** New onboarding campaign

The objective of this project is to determine whether the new onboarding experience should be rolled out to all users based on business metrics, statistical evidence, and risk evaluation.

---

# Business Problem Statement

The company must decide whether the new onboarding campaign should replace the existing onboarding process.

This decision affects:

* Product Team
* Marketing Team
* Customer Success Team
* Business Leadership
* End Users

The campaign should increase paid user conversion while maintaining a positive customer experience. Before recommending a rollout, statistical evidence and guardrail metrics must be evaluated to ensure that improvements are meaningful and sustainable.

---

# Dataset Description

The dataset contains user-level experiment data with **1,408 users** and **16 columns**.

### Dataset Fields

* user_id
* signup_date
* experiment_group
* region
* device_type
* traffic_source
* plan_type
* visited_landing_page
* started_trial
* completed_onboarding
* converted_to_paid
* revenue_30d
* support_tickets_30d
* refund_requested
* days_to_convert
* engagement_score

The dataset includes user acquisition, onboarding, conversion, revenue, engagement, and customer support information.

---

# North Star Metric

## Paid Conversion Rate

### Definition

Paid Conversion Rate measures the percentage of users who convert from free users to paid subscribers.

### Formula

Paid Conversion Rate = (Paid Users ÷ Total Users) × 100

### Why this Metric?

Paid Conversion Rate directly reflects business growth because subscription revenue depends on converting users into paying customers.

### Supporting Metrics

The following metrics support the North Star Metric:

* Landing Page Visit Rate
* Trial Start Rate
* Onboarding Completion Rate
* Average Revenue Per User (ARPU)
* Average Revenue Per Converted User (ARPC)
* Engagement Score

These metrics help explain *why* Paid Conversion Rate changes but are not the primary success metric.

### Risk of Optimizing Only the North Star

Focusing only on Paid Conversion Rate could result in:

* Higher refund rates
* Increased support tickets
* Lower customer satisfaction
* Poor long-term retention
* Reduced revenue quality

Therefore, guardrail metrics must also be monitored.

---

# KPI Tree Summary

The KPI Tree is structured as follows:

### North Star Metric

* Paid Conversion Rate

### Primary KPI Drivers

**1. Acquisition**

* Landing Page Visit Rate
* Trial Start Rate

**2. Activation**

* Onboarding Completion Rate
* Engagement Score
* Days to Convert

**3. Monetization**

* Paid Conversion Rate
* Average Revenue Per User
* Average Revenue Per Converted User

### Guardrail Metrics

* Refund Rate
* Support Ticket Rate
* Engagement Score
* Days to Convert

---

# Data Cleaning and Preparation

Before analysis, the dataset was checked for data quality.

The following validation steps were performed:

* Checked for missing values
* Verified Control and Treatment group counts
* Checked duplicate User IDs
* Validated binary columns (0/1 values)
* Reviewed revenue outliers
* Examined segment distribution across experiment groups

No major data quality issues affecting the analysis were identified.

---

# Experiment Analysis Approach

The experiment compared Control and Treatment groups using the following metrics:

* User Count
* Landing Page Visit Rate
* Trial Start Rate
* Onboarding Completion Rate
* Paid Conversion Rate
* Average Revenue Per User
* Average Revenue Per Converted User
* Refund Rate
* Support Ticket Rate
* Engagement Score
* Average Days to Convert

Additional segment analysis was performed by:

* Region
* Device Type
* Traffic Source
* Plan Type

---

# Hypothesis Test Summary

A statistical hypothesis test was performed to determine whether the Treatment group significantly improved Paid Conversion Rate.

### Null Hypothesis (H₀)

The Treatment group does not improve Paid Conversion Rate.

### Alternative Hypothesis (H₁)

The Treatment group improves Paid Conversion Rate.

### Test Used

One-Tailed Two-Proportion Z-Test

### Significance Level

α = 0.05

The statistical results support the conclusion that the Treatment group performs better than the Control group.

---

# Guardrail Metrics Considered

The rollout decision was evaluated using the following guardrail metrics:

* Refund Rate
* Support Ticket Rate
* Engagement Score
* Days to Convert

These metrics ensure that improvements in conversion do not negatively impact customer experience or business performance.

---

# Final Recommendation

Based on the experiment analysis:

* Paid Conversion Rate improved.
* Revenue-related metrics improved.
* Engagement increased.
* Statistical testing confirmed the improvement was significant.
* Guardrail metrics remained stable.

**Recommendation:** **Launch the new onboarding campaign** while continuing to monitor key performance indicators and guardrail metrics after deployment.

---

# Assumptions and Limitations

### Assumptions

* Users were randomly assigned to experiment groups.
* Experiment data accurately represents user behavior.
* Conversion events are independent.

### Limitations

* Short experiment duration
* Long-term retention was not measured
* External marketing activities may influence results
* Future experiments may be required for additional validation

---

# Repository Structure

```text
part2_kpi_experiment/
├── data/
│   └── campaign_experiment_data.xlsx
├── analysis/
│   ├── experiment_analysis.xlsx
│   └── hypothesis_test_notes.md
├── outputs/
│   ├── experiment_summary.xlsx
│   ├── kpi_tree.png
│   └── recommendation_memo.md
├── screenshots/
│   ├── summary_metrics.png
│   ├── hypothesis_test_output.png
│   └── kpi_tree_preview.png
└── README.md
```

---

# Screenshots Included

The repository includes the following screenshots:

* **summary_metrics.png** – Control vs. Treatment summary metrics
* **hypothesis_test_output.png** – Statistical test output
* **kpi_tree_preview.png** – KPI Tree visualization

These screenshots provide supporting evidence for the experiment analysis and final recommendation.

---

# Conclusion

This project demonstrates a complete A/B experiment analysis, beginning with business problem definition and ending with a data-driven recommendation. By combining KPI analysis, statistical testing, guardrail evaluation, and segment analysis, the project provides a structured framework for deciding whether to launch the new onboarding campaign.

