```markdown
```
```markdown
# Beyond the Bleachers: Proactive CRM Strategies for NFL Season Ticket Retention

**Author:** [[Author Name] Robert Slowik]
**Contact:** [[LinkedIn Profile URL](https://www.linkedin.com/in/rslowik/)] 

---

## Executive Summary
Customer churn in professional sports ticketing represents millions of dollars in lost annual revenue. For this project, I acted as a CRM Data Analyst for an NFL franchise to proactively identify Season Ticket Holders at risk of non-renewal. 

Instead of jumping straight to a "black box" machine learning model, I engineered a highly interpretable, **Rules-Based Risk Scoring Matrix** using Python and Pandas. This heuristic model flags at-risk accounts based on behavioral and transactional data, allowing the ticket sales team to deploy targeted retention strategies before the renewal deadline.

---

## Business Problem
In the NFL, season-ticket holders represent a core revenue stream for franchises. However, every offseason, teams face the silent threat of fan churn: season-ticket holders choosing not to renew their packages. Without an automated way to spot early warning signs of disengagement, front-office teams are left reacting to cancellations. Across the evaluated account base of 1,000 accounts, 3.9% of accounts did not renew, resulting in a loss of $168,246.

**Objective:** 
The objective of this project was to develop a CRM rules-based risk scoring matrix that identifies season ticket accounts at risk of churning prior to the renewal window. Specifically, this project aims to:
-	Uncover the core behavioral drivers behind fan non-renewal.
-	Apply CRM business rules to assign, define, and evaluate risk tiers.
-	Segment the entire account base into actionable risk tiers to deploy targeted, cost-effective CRM retention strategies.

---

## The Data
The analysis is based on a synthetic dataset representing a 9-game NFL home schedule. 

**Key Features Evaluated:**
*   **Behavioral:** `ticket_utilization_pct`, `secondary_resale_pct`, `games_attended`
*   **Financial:** `total_annual_ticket_spend`, `total_season_concession_spend`
*   **Operational/Sentiment:** `complaints_logged`, `customer_satisfaction_score`, `rep_touchpoints_count`
*   **Contextual:** `tenure_years`, `seat_tier`, `team_wins_attended`

---

## Methodology & CRM Business Rules

Using Pandas, I calculated a composite risk score for each account based on proven hospitality and sports industry thresholds:

1.  **Low Utilization (+30 pts):** `ticket_utilization_pct < 50%`. (Fans missing over half the season experience a severe drop in perceived ROI).
2.  **High Secondary Resale (+25 pts):** `secondary_resale_pct > 55%`. (Account acts more like a ticket broker than a fan; highly volatile to market/team performance).
3.  **Friction/Service Failures (+25 pts):** `complaints_logged >= 2`. (Systemic poor experiences erode brand loyalty).
4.  **Detractors / Unresponsive (+20 pts):** `CSAT <= 4` or missing survey data. (Active dissatisfaction or total disengagement).

Accounts were then segmented into **High Risk (80+ pts)**, **Medium Risk (40-79 pts)**, and **Low Risk (<40 pts)** tiers.

---

## Strategic CRM Recommendations

Based on the risk segmentation, I developed the following intervention playbook for the Account Executive (AE) team:

1.	**Targeted Offseason Campaigns**: Deploy automated alerts to flag high-risk and medium-risk accounts weeks prior to package renewal deadlines, allowing the account management team to intervene early.
2.	**Implementation of flexible mini plans**: Implement half-season or premium 3-game packages for accounts with over 60% resale activity. This lowers their spend and reserves tickets for fans rather than those using tickets as a financial asset.
3.	**Engagement Interventions**: Trigger automated outreach (e.g., seat upgrade offers or concession vouchers) when a fan misses a game after reporting a complaint or provides a low satisfaction score.

---

## Tech Stack & Skills Demonstrated
*   **Language:** Python 3
*   **Libraries:** `pandas`, `numpy`, `matplotlib`, `seaborn`
*   **Techniques:** Exploratory Data Analysis (EDA), Feature Engineering, Heuristic Modeling, Data Visualization, Business Strategy

---

```