#  Phase 1 — Aircraft Risk Analysis for Safe Fleet Decisions

This project applies data-driven analytics to identify safe and commercially viable aircraft models for a new aviation business. By examining decades of safety reports, the goal is to support smarter fleet acquisition decisions based on real-world incident history.

---

##  Business Relevance

Aviation operators rely on safety analytics to:

- Minimize financial losses from accidents
- Improve compliance and regulatory approval
- Reduce fatality risks and enhance public trust
- Guide fleet investment and maintenance strategy

Smarter aircraft selection = lower liability + higher commercial success.

---

##  Project Objectives

1. Identify aircraft models with the lowest accident incidence
2. Evaluate injury outcomes and aircraft damage severity
3. Compare safety performance across multiple aircraft categories
4. Recommend safe + cost-effective fleet and contract options

---

##  Dataset Description

| Feature | Description |
|--------|-------------|
| Event Date | When the aviation incident occurred |
| Aircraft Make & Model | Manufacturer + configuration |
| Investigation Type | Accident vs Incident |
| Injury Severity | None, Minor, Serious, Fatal |
| Total Injuries | # of people affected |

 120+ cleaned aviation incident reports analyzed

---

##  Data Preparation

- Removed records with missing aircraft model information
- Standardized categorical values for damage + severity
- Focused on models with sufficient incident reporting
- Used weighted impact (fatal > serious > minor) for safety ranking

---

##  Tableau Dashboard (Interactive)

🔗 View Dashboard Here:  
https://public.tableau.com/views/Project_AviationRiskAnalysisDashboard/AirSafetyDashboard

### Visuals Included
1) Damage Severity vs Injury Outcomes  
2) Reported Incidents by Aircraft Make  
3) Quantified Safety Ranking of Aircraft Models  

---

##  Key Insights

1️ *High-Risk Models*  
Cessna 152, Cessna 172, Piper PA-28-140  
→ High incident frequency + higher severe outcomes  
→ *Not ideal for new operators without insurance buffering*

2️ *Safest Operational Option*  
Cessna 206B  
→ 92% of cases result in only *minor* damage  
→ Low repair + insurance cost

3️ *Commercially Strongest*  
Boeing 737  
→ *Near-perfect safety record in dataset*  
→ Economically strong for passenger route deployment

---

##  Recommendations

| Category | Recommendation |
|---------|---------------|
|  Immediate Purchase | Cessna 206B – low damage cost & proven safety |
|  Passenger Fleet | Lease Boeing 737 where possible |
|  Conditional Use | Cessna 152/172 only with risk-transfer contracts |

---

##  Tools Used

| Category | Tools |
|--------|------|
| Data Analysis | Python, Pandas, NumPy |
| Visualization | Tableau, Seaborn, Matplotlib |
| Notebook | Jupyter |
| Version Control | Git + GitHub |

---

##  Project Structure
