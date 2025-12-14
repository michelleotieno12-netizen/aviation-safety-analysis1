# Aviation Safety Analysis
This project analyzes historical aviation accident data to identify lower-risk aircraft for commercial and private aviation operations.

### Stakeholder
The primary stakeholder for this project is the Head of the new Aviation Division, who is responsible for making aircraft purchasing and operational decisions.

## Business Understanding
The company is expanding into the aviation industry and needs to make informed decisions about which aircraft to purchase and operate. Aviation accidents carry significant safety, legal, and financial risks, and leadership currently lacks insight into which aircraft have historically demonstrated lower risk.

The goal of this project is to analyze aviation accident data to identify aircraft types and manufacturers associated with fewer and less severe accidents. These insights will support data-driven aircraft acquisition decisions and help minimize operational risk as the company enters the aviation market.

### Key Business Questions
- Which aircraft makes and models have historically been involved in fewer and less severe accidents?
- Are there trends in accident frequency or severity over time?
- Which aircraft characteristics are associated with lower overall risk?

## Data
Source: National Transportation Safety Board (1962–2023)

### Dataset Overview

The dataset consists of aviation accident and incident records collected by the National Transportation Safety Board. Each row represents a reported aviation event and includes information about aircraft characteristics, event timing, and injury outcomes.

### Initial Observations

- The dataset spans multiple decades, providing a long-term view of aviation safety trends.
- Several columns contain missing values, particularly in fields related to aircraft details and injury counts.
- Both categorical and numerical features are present, which will require different preparation strategies in later steps.

These observations will guide data cleaning, feature selection, and risk metric creation in the next phase.

## Analysis
Exploratory data analysis, aggregation, and visualization will be used to identify trends and risk factors.

## Conclusion
This analysis provides three actionable recommendations to guide aircraft acquisition decisions.

## Data Preparation

To support meaningful risk analysis, the dataset was reduced to columns relevant to aircraft identification and injury severity. Records missing aircraft make or model information were removed, as these entries could not support aircraft-level risk assessment.

Injury-related fields were converted to numeric values, and missing injury counts were replaced with zeros under the assumption that unreported values indicate no injuries. A total injury metric was created to serve as a proxy for accident severity.

## Exploratory Data Analysis

To evaluate aircraft safety risk, accident records were aggregated by aircraft manufacturer. Risk was assessed using the average number of injuries per accident, serving as a proxy for accident severity.

Manufacturers with a sufficient number of recorded incidents were prioritized to ensure meaningful comparisons. The analysis highlights aircraft manufacturers that are associated with lower average injury counts per accident, suggesting lower operational risk relative to peers.

### Initial Insights

- Some aircraft manufacturers show consistently lower average injury counts per accident.
- Accident frequency alone does not indicate risk; injury severity provides more actionable insight.
- These findings can guide initial aircraft selection decisions, subject to further operational and financial considerations.


### RECOMENDATIONS

### Recommendation 1: Prioritize Aircraft from Lower-Risk Manufacturers
Analysis shows that certain aircraft manufacturers are associated with significantly lower average injury counts per accident. The company should prioritize aircraft purchases from these manufacturers to reduce safety risk and potential liability exposure.

**Business Impact:** Lower injury severity reduces operational risk, insurance costs, and reputational damage.

---

### Recommendation 2: Avoid Decisions Based Solely on Accident Frequency
Some aircraft manufacturers appear frequently in accident records due to high usage rates, not necessarily poor safety performance. Decision-making should focus on accident severity metrics rather than raw accident counts.

**Business Impact:** Prevents incorrectly excluding widely used but safe aircraft from consideration.

---

### Recommendation 3: Use Injury Severity as a Core Safety Metric
Average injury count per accident provides a more actionable measure of risk than accident occurrence alone. This metric should be incorporated into ongoing aircraft evaluation and procurement processes.

**Business Impact:** Enables consistent, data-driven safety assessments for future aircraft acquisitions.

### Additional Visual Insights

Several supporting visualizations were created to contextualize aircraft risk. A scatter plot comparing accident frequency and injury severity highlights why severity-based metrics are more meaningful than raw counts. A stacked bar chart illustrates differences in injury types among lower-risk manufacturers, emphasizing fatal and serious injury reduction. Finally, a time-series view shows how injury severity has evolved over time, supporting long-term strategic planning.

