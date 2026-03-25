**📊 Customer Churn Reduction - A-B Testing - Retention-Analytics**
A customer analytics case study where insights lead to decisions and not just dashboards.

Data Analyst & Business Analyst Project – SQL • Power BI • Customer Insights • A/B Testing • Decision Support

This project demonstrates how a Data Analyst / Business Analyst turns raw customer activity into business decisions.
It focuses on customer value, churn prediction, retention strategy validation, and automated insight delivery and not building pipelines or engineering systems.

**⭐ Business Outcome Summary**

Using customer behavior analysis, churn modeling, and an A/B retention test:
Retention improved by +35.3% in the offer group (B)
p-value: 0.0006 → statistically significant
Recommendation: Scale the offer to at-risk customers (90+ days inactive)
Expected Impact: Prevent churn, recover revenue, and improve 30-day return rate

**🎯 Project Purpose**

To help business and product teams answer:
| Business Question                           | Answered Through                       |
| ------------------------------------------- | -------------------------------------- |
| Who are our most valuable customers?        | Segmentation & LTV tiers               |
| Which customers are at risk and why?        | Churn scoring + inactivity patterns    |
| How much revenue could churn cost us?       | Revenue-at-risk analysis               |
| Does an incentive actually change behavior? | A/B experiment w/ significance testing |
| What action should we take next?            | Rule-based AI insights for CRM         |

📈 **Dashboards (Power BI)**
These dashboards were designed based on business questions and acceptance criteria.

Customer Behavior Dashboard:
Lifetime value tiers
Repeat purchase behavior
Revenue by segment
Engagement overview

Used by: Marketing & CRM Teams
Supports decisions like:
Which customer segments should receive targeted upsell or reactivation campaigns?
Where should the company focus to grow high-value, repeat-purchase customers?

📍 dashboards/Customer Behavior dashboard.pbix
📸 ![Customer Behavior Dashboard](https://raw.githubusercontent.com/swatiLalwani/sales-intelligence-customer-analytics/main/dashboards/screenshots/customer%20behavior.png)

Churn & Retention Dashboard:
Churn vs retention %
At-risk customers
Revenue at risk
Days since last purchase

Used by: Customer Success & Retention Teams
Supports decisions like:
Which customers to re-engage immediately based on inactivity?
How much revenue is currently at risk if no action is taken?
📍 dashboards/Customer churn dashboard.pbix
📸 ![Churn & Retention Dashboard](https://raw.githubusercontent.com/swatiLalwani/sales-intelligence-customer-analytics/main/dashboards/screenshots/customer%20churn.png)

**🧪 A/B Test – Retention Offer Impact:**
| Step                     | File                                      |
| ------------------------ | ----------------------------------------- |
| Assign groups            | `/ab_testing/sql/random_assignment.sql`   |
| Load or simulate results | `/ab_testing/simulate_ab_outcomes.py`     |
| Validate experiment      | `/ab_testing/sql/validate_assignment.sql` |
| Statistical test         | `/ab_testing/code/ab_significance.py`     |

A/B Result:
📈 +35.3% improvement in 30-day retention
🧪 p = 0.0006 (statistically significant)
💡 Decision: Roll out retention offer to at-risk customers
💵 Outcome: Prevents churn & protects recurring revenue

Decision Recommendation:
➡️ Scale incentive to customers inactive 90+ days
➡️ Send personalized offer + follow-up touchpoint
➡️ Monitor revenue impact over next 30 days

**🤖 Automated Insight Generation:**
A lightweight rules engine creates CRM-ready insights:
Why at risk
Recommended action
Confidence level

| Insight Task         | File                        |
| -------------------- | --------------------------- |
| Generate insights    | `ai_insights.py`            |
| Insert/Update to SQL | `upsert_ai_insights.py`     |
| Power BI Input View  | `automated_ai_insights.sql` |

Output:
"Customer is AT_RISK due to 180+ days inactivity and low repeat history. Recommend reactivation offer. Confidence: High."


**📌 How This Project Drives Decisions (Before vs After Impact)**
| Stage               | Business State                                                                                                                                                                                |
| ------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Before Analysis** | No visibility into which customers were most at risk, no data-backed criteria for incentive targeting, and decisions based on assumptions rather than performance.                            |
| **After Analysis**  | Identified high-risk segments, quantified churn drivers, and validated that a retention offer improved return rate by **+35.3% (p=0.0006)** — enabling a confident, data-backed rollout plan. |


**📂 Repository Structure:**

sales-intelligence-customer-analytics/
│
├── datasets/                  # CRM & ERP input data
├── analytics/                 # KPI logic, churn, segmentation, risk
├── dashboards/                # Power BI reports & screenshots
├── ab_testing/                # Experiment setup, outcomes & significance
├── ai_insights/               # Automated recommendations
├── docs/                      # BRD, use cases, user stories (BA)
└── README.md

**🛠 Tools Used:**

SQL Server → analysis logic, KPIs, experiment setup
Power BI → dashboarding & decision reporting
Python → A/B results, insight generation, export to CSV/SQL
BA Documentation → BRD • Use Cases • User Stories • Acceptance Criteria

**⚠️ Data Assumptions & Limitations: **
To maintain transparency in decision-making, the following assumptions were applied:
30-day return was used as a proxy for retention; longer-term behavior may differ.
The offer strategy was tested only on at-risk customers (90+ days inactive).
Revenue impact was measured at the order level; customer lifetime value forecasting was not included.
📌 Next Step if implemented:
Extend evaluation to 60–120 day periods and measure contribution to long-term LTV and net revenue retention.

**📩 Contact:**
If you'd like a walkthrough or want to discuss the project for a role:
📧 swati.lalwani1214@gmail.com
🔗 LinkedIn available on request
