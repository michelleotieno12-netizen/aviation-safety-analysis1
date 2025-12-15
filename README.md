
# Aviation Safety Analysis

This project analyzes historical aviation accident data to identify lower-risk aircraft for commercial and private aviation operations. The goal is to support data-driven aircraft acquisition decisions as the company expands into the aviation industry.

---

## Stakeholder
The primary stakeholder for this project is the Head of the Aviation Division, who is responsible for making aircraft purchasing and operational decisions.

---

## Business Understanding
As the company enters the aviation market, it faces significant safety, legal, and financial risks associated with aircraft operations. Leadership currently lacks data-driven insight into which aircraft manufacturers and models have historically demonstrated lower operational risk.

This project analyzes aviation accident data to identify aircraft types and manufacturers associated with fewer and less severe injuries. These insights are intended to support informed aircraft purchasing decisions and reduce overall operational risk.

### Key Business Questions
- Which aircraft manufacturers and models have historically been involved in fewer and less severe accidents?
- Are there observable trends in accident frequency or injury severity over time?
- Which aircraft characteristics are associated with lower overall risk?

---

## Data
**Source:** National Transportation Safety Board (1962–2023)

### Dataset Overview
The dataset consists of aviation accident and incident records collected by the National Transportation Safety Board. Each row represents a reported aviation event and includes information about aircraft characteristics, event timing, and injury outcomes.

### Initial Observations
- The dataset spans multiple decades, enabling long-term analysis of aviation safety trends.
- Several columns contain missing values, particularly in aircraft details and injury-related fields.
- The data includes a mix of categorical and numerical variables, requiring different preparation strategies.

These observations informed data cleaning decisions, feature selection, and the creation of risk metrics used in the analysis.

---

## Data Preparation
To support meaningful risk analysis, the dataset was reduced to variables relevant to aircraft identification and injury severity. Records missing aircraft make or model information were removed, as they could not support aircraft-level risk assessment.

Injury-related fields were converted to numeric values, and missing injury counts were replaced with zeros under the assumption that unreported values indicate no injuries. A total injury metric was created to serve as a proxy for accident severity.

---

## Exploratory Data Analysis
Accident records were aggregated by aircraft manufacturer to evaluate safety risk. Risk was assessed using the average number of injuries per accident, which serves as a proxy for accident severity.

Manufacturers with a sufficient number of recorded incidents were prioritized to ensure meaningful comparisons. The analysis highlights manufacturers associated with lower average injury counts per accident, suggesting relatively lower operational risk.

### Key Insights
- Some aircraft manufacturers are consistently associated with lower average injury severity.
- Accident frequency alone does not indicate risk; injury severity provides more actionable insight.
- These findings can inform aircraft selection decisions alongside operational and financial considerations.

---

## Recommendations

### Recommendation 1: Prioritize Aircraft from Lower-Risk Manufacturers
Certain aircraft manufacturers are associated with significantly lower average injury counts per accident. Prioritizing these manufacturers can help reduce safety risk and potential liability exposure.

**Business Impact:** Reduced injury severity lowers operational risk, insurance costs, and reputational damage.

---

### Recommendation 2: Avoid Decisions Based Solely on Accident Frequency
Some manufacturers appear frequently in accident records due to high usage rates rather than poor safety performance. Decisions should focus on injury severity metrics rather than raw accident counts.

**Business Impact:** Prevents the exclusion of widely used but relatively safe aircraft.

---

### Recommendation 3: Use Injury Severity as a Core Safety Metric
Average injury count per accident provides a more meaningful measure of risk than accident occurrence alone. This metric should be incorporated into ongoing aircraft evaluation and procurement processes.

**Business Impact:** Enables consistent, data-driven safety assessments for future aircraft acquisitions.

---

## Interactive Dashboard
An interactive Tableau dashboard allows stakeholders to explore aviation safety risk by manufacturer, injury severity, and trends over time.

[View the Tableau Dashboard](https://public.tableau.com/app/profile/eve.michelle/viz/AviationSafetyRiskAnalysis/Dashboard1?publish=yes)

---

## Conclusion
This analysis demonstrates that aviation safety risk varies meaningfully across aircraft manufacturers and is more accurately assessed using injury severity rather than accident frequency alone. By leveraging historical aviation accident data, this project identified manufacturers associated with lower average injury outcomes and highlighted patterns that can inform safer aircraft acquisition decisions.

The findings support a data-driven approach to entering the aviation market, emphasizing the importance of prioritizing lower-risk manufacturers, using severity-based safety metrics, and avoiding assumptions based solely on accident volume. While historical data cannot eliminate future risk, it provides valuable insight for reducing exposure to safety, financial, and reputational harm.

These results offer a strong foundation for informed aircraft procurement and can be extended through future analysis incorporating aircraft models, operational context, and cost considerations.
