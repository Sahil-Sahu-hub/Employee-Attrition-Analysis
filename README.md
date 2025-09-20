# HR Analytics

## Project Title
HR Analytics: Diagnosing Workforce Attrition with Data-Driven Insights

## Brief One Line Summary
An HR analytics dashboard to identify, quantify, and mitigate employee attrition through structured workforce data analysis.

## Overview
Employee attrition is a recurring operational risk that impacts institutional knowledge, workforce morale, and replacement costs.  
This project addresses attrition by constructing a data-driven diagnostic dashboard, enabling stakeholders to assess turnover patterns and prescribe targeted interventions.  

The intended audience includes HR leadership, operational managers, and executive stakeholders tasked with workforce planning and retention strategy.  
Deliverables include a Power BI dashboard, structured datasets, and an insight report highlighting attrition drivers across demographic, tenure, and compensation cohorts.  

The analysis is based on [15 years of HRIS data / REPLACE_WITH_ACTUAL_PERIOD], enriched with external benchmarks (industry attrition rates, regional compensation norms), and transformed into aggregated features suitable for both descriptive and predictive analysis.  

## Problem Statement
The organization faces an overall attrition rate of **16.12%** (237 exits out of 1,470 employees), disproportionately affecting mid-career professionals (ages 26–35) and employees earning below $5K/month. High turnover in these segments disrupts succession pipelines, inflates hiring costs, and weakens business continuity.  
**Success criteria**: reduce attrition rate by ≥ 3% over 12–18 months, increase average tenure by ≥ 1 year, and lower early-tenure (1–3 years) turnover by ≥ 10% relative to baseline.

## Tools and Technologies
- **Languages**: Python 3.11, SQL (MySQL 8.0)
- **Libraries**: pandas, numpy, matplotlib, seaborn, scikit-learn
- **Visualization**: Power BI Desktop (v[REPLACE_WITH_VERSION])
- **Database**: MySQL Community Server
- **Containerization / Environment**: Docker, Conda
- **Version Control**: Git, GitHub
- **Other**: Jupyter Notebook for EDA and prototyping

## Methods
1. **Data Ingestion**
   - Extracted HRIS data (demographics, tenure, salary, job role).
   - Imported external salary benchmarks for context.
2. **Data Cleaning**
   - Removed duplicates.
   - Standardized categorical fields (job role, education).
   - Normalized date formats.
   - Excluded employees on long-term leave.
3. **Feature Engineering**
   - Age grouped into bins: *18–25, 26–35, 36–45, 46–55, 55+*.
   - Salary slabbed: *≤5K, 5–10K, 10–15K, 15K+*.
   - Tenure grouped: *0–1, 1–3, 3–5, 5+ years*.
   - Gender distribution encoded.
   - Derived KPIs: attrition rate by segment, tenure distribution, compensation-to-attrition elasticity.
4. **Exploratory Analysis**
   - Attrition counts by age, salary, job role, education field.
   - Attrition timelines across tenure years.
5. **Validation Strategy**
   - Cross-validation on tenure-based splits.
   - Benchmark comparison against external attrition metrics.
6. **Evaluation Metrics**
   - Attrition rate (%) per segment.
   - Turnover concentration index.
   - Salary-at-risk thresholds.
   - [Optional Predictive Extension] ROC-AUC, F1-score for attrition classifiers.

## Key Insights
- **Mid-Career Vulnerability**: Employees aged 26–35 show a 23% attrition rate.  
  *Implication*: Invest in mid-career growth and promotion pipelines.  
- **Gender Gap**: Female attrition at 17.01% vs. 14.80% for males.  
  *Implication*: Expand hybrid work policies and childcare benefits.  
- **Salary Slabs**: Sub-$5K salaries face 19% attrition vs. 8% in $5–8K bracket.  
  *Implication*: Revise compensation bands to improve retention.  
- **Early Tenure Drop-Off**: 1–3 year employees are most at risk.  
  *Implication*: Strengthen onboarding and early engagement programs.  
- **Department-Specific Risk**: Sales and R&D contribute disproportionately to attrition.  
  *Implication*: Adjust commission structures (Sales) and enhance skill training (R&D).  
- **Role-Specific Pressure**: Laboratory Technicians and Sales Executives account for ~50% of exits.  
  *Implication*: Prioritize retention in high-churn roles.  
- **Education Field Distribution**: Life Sciences and Medical dominate attrition counts.  
  *Implication*: Review career pathing and workload for these education tracks.  
- **Tenure Curve**: Sharp drop after Year 1, plateau after Year 3.  
  *Implication*: Employees either disengage quickly or embed for long term.

## Results & Conclusion
- **Overall Attrition Rate**: 16.12% (237 / 1,470 employees).  
- **Highest-Risk Group**: Ages 26–35 (116 exits).  
- **Salary Sensitivity**: ≤5K slab accounts for 163 exits (≈ 69% of total attrition).  
- **Tenure Impact**: 21% of exits occur within 1–3 years.  

**Interpretation**: Workforce stability hinges on pay competitiveness, early-tenure experience, and career progression visibility. Mid-career professionals represent the greatest flight risk.  

**Limitations & Assumptions**:  
- Industry benchmarks used are placeholders and must be validated against real datasets.  
- Predictive modeling not fully productionized—analysis remains diagnostic rather than prescriptive.  
- External labor market dynamics (e.g., economic downturns, sectoral hiring spikes) not modeled.  

## Future Work
- Integrate predictive attrition models (logistic regression, random forest, gradient boosting).  
- Incorporate employee engagement survey data for non-compensation factors.  
- Automate ETL pipelines for monthly/quarterly refresh.  
- Productionize dashboards with role-based access governance.  
- Conduct controlled A/B testing on interventions (e.g., pay adjustments, hybrid work rollout).  
- Build cost-of-attrition KPI (replacement cost × attrition count).  
- Implement monitoring and alerting runbooks for HR leadership.  

## Author & Contact

**Author**: Sahil Sahu  

**Role**: Data Analyst 

**Email**: [your_email@example.com]  

