# Phase 1: Data-Driven Aircraft Risk Analysis for Safe Fleet Decisions

This project analyzes decades of aviation accident and incident records to support evidence-based fleet selection for new or expanding airlines and aviation startups.  
By examining aircraft makes, models, injury severity, and damage outcomes, the analysis identifies trends that reveal which aircraft demonstrate lower operational risk and stronger safety performance.

---

## Business Understanding

A new aviation operator aims to build a safety-first fleet strategy that aligns with regulatory standards and minimizes costly safety failures.  
This analysis provides actionable insights by addressing key strategic questions:

1. Which aircraft makes and models appear most often in historical safety reports?  
2. Which models record fewer serious injuries or destroyed-aircraft outcomes?  
3. How do accident versus incident ratios vary across different manufacturers?  
4. What insights can guide safer fleet decisions for new aviation entrants?

---

## Business Relevance

This project supports multiple aviation stakeholders in making informed, safety-conscious decisions:

- *Airline Operators:* Evaluate historical fleet safety performance for planning and acquisition.  
- *Manufacturers:* Identify long-term safety and reliability trends across aircraft models.  
- *Regulators:* Promote data-driven oversight and improved safety compliance.  
- *Investors and Insurers:* Assess operational risks before funding or underwriting fleets.  

By adopting a data-driven approach, stakeholders can minimize risk, improve safety outcomes, and strengthen brand reputation through transparent decision-making.

---

## Project Objectives

1. Quantify event frequency by aircraft make and model.  
2. Compare the proportion of *Accidents vs Incidents* across aircraft makes.  
3. Examine relationships between *Injury Severity* and *Aircraft Damage*.  
4. Identify potential *low-risk models* suitable for safety-focused fleet operations.

---

## Dataset Description

The dataset, Aviation_Data.csv, contains historical global accident and incident reports from aviation authorities.

| Feature | Description |
|----------|-------------|
| *Event Date* | Date of occurrence |
| *Investigation Type* | Classification as Accident or Incident |
| *Aircraft Make* | Manufacturer (e.g., Cessna, Boeing, Piper) |
| *Aircraft Model* | Model designation |
| *Injury Severity* | None / Minor / Serious / Fatal |
| *Aircraft Damage* | None / Minor / Substantial / Destroyed |
| *Location* | Area or region of the event |

These features were used to identify and normalize key dimensions for fleet safety evaluation.

---

## Analytical Approach

The analysis followed a structured data science workflow:

1. *Data Cleaning* — Normalized column names, handled missing values, and standardized formats.  
2. *Feature Engineering* — Defined categorical fields for severity, damage, and classification.  
3. *Exploratory Data Analysis (EDA)* — Visualized relationships between aircraft types, event frequencies, and safety outcomes.  
4. *Interpretation and Insights* — Translated analytical findings into actionable recommendations for fleet decision-makers.

All stages are fully documented and reproducible within the notebook:  
notebooks/phase1_analysis.ipynb

---

## Data Cleaning and Standardization Strategy

To ensure consistency and reliability in analysis, the following cleaning procedures were applied:

1. *Column Normalization* — Converted all column names to lowercase and used underscores for readability.  
2. *Core Feature Identification* — Selected relevant columns:  
   - Investigation Type  
   - Aircraft Make  
   - Aircraft Model  
   - Injury Severity  
   - Aircraft Damage  
   - Event Date  
3. *Category Normalization* — Standardized variations of categorical labels:  
   - Investigation Type: Accident / Incident  
   - Injury Severity: None / Minor / Serious / Fatal / Unknown  
   - Aircraft Damage: None / Minor / Substantial / Destroyed / Unknown  
4. *Data Integrity Checks* — Removed empty and duplicate records, ensuring valid make and model fields.

The cleaned dataset (df) was then used for all subsequent analysis and visualizations.

---

## Exploratory Data Analysis (EDA)

The exploratory phase examined key perspectives to identify safety-related trends:

### 1. Top Aircraft Models by Recorded Events
A bar chart illustrating the most frequently recorded aircraft models.  
This visualization highlights which aircraft have higher operational presence or exposure to incidents.

### 2. Accident vs Incident Distribution by Aircraft Make
A stacked bar visualization comparing how different manufacturers record accidents versus incidents.  
This provides insight into manufacturer reliability and the balance between minor and severe events.

### 3. Relationship Between Injury Severity and Aircraft Damage
A cross-tabulated analysis exploring the correlation between the severity of injuries and the level of aircraft damage.  
Findings confirm that *serious or fatal injuries* frequently coincide with *substantial or destroyed aircraft damage*.

---

## Key Insights Summary

- A limited number of aircraft models account for a majority of recorded events, reflecting fleet popularity and exposure levels.  
- Non-catastrophic *incidents* occur more frequently than fatal accidents for most makes, suggesting recoverability and strong structural integrity.  
- *Serious or Fatal* injuries are consistently aligned with *Substantial or Destroyed* aircraft outcomes, indicating that damage levels correlate with event severity.  
- Certain models demonstrate consistently lower proportions of severe outcomes, identifying them as potential low-risk fleet candidates.

---

## Conclusion

1. Event frequency alone cannot determine an aircraft’s safety; it must be contextualized within severity and exposure.  
2. Aircraft with lower proportions of fatal or destroyed outcomes provide stronger candidates for safety-focused fleet selection.  
3. A transparent, data-driven framework enhances confidence among operators, regulators, and investors by aligning evidence-based safety assessment with operational needs.

---

## Recommendations

### 1. Preferred Candidates
Focus on aircraft with historically *low fatality rates* and *fewer destroyed-aircraft outcomes*.  
Such models represent robust candidates for new fleet acquisition and long-term operational safety.

### 2. Caution List
Treat models combining *high event frequency* and *severe outcomes* as higher-risk.  
Implement stronger maintenance programs, enhanced pilot training, or restricted operational use.

### 3. Next Steps
Incorporate additional data sources—such as *flight hours* and *maintenance history*—to develop normalized safety performance scores.  
Align fleet decisions with regulatory and insurance risk frameworks to ensure sustainability and compliance.

---

## Tableau Dashboard

To complement this Python-based analysis, an interactive *Tableau Public dashboard* presents the key metrics visually.  
The dashboard enables dynamic exploration of event types, injury severity, and damage levels across aircraft makes and models.

*Tableau Public Link:*  
[Air Safety Dashboard — Igiraneza Rudahunga Alceste](https://public.tableau.com/app/profile/igiraneza.alceste/viz/Book1_17619452328360/AirSafetyDashboard?publish=yes)

If a static preview is available, it can be found in the images directory:

```text
images/air_safety_dashboard.png
