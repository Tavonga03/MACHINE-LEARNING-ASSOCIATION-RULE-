## Analysis of the COVID-19 Association Rules
The graph shows the Top 10 COVID-19 Association Rules generated using the Apriori algorithm. The horizontal axis represents lift, while the vertical axis shows the association rules discovered from the dataset.

### 1. Interpretation of the results

- Highest lift: The rule `WHO_Region_Americas, Confirmed_High → Recovered_High, Active_High, Deaths_High` has the highest lift, approximately 2.52. This indicates that the combination of these categories occurs together more frequently than expected if the antecedent and consequent were independent.
- Regional patterns: Several high-lift rules involve the Americas and Eastern Mediterranean regions. This suggests that the region categories are associated with particular combinations of COVID-19 statistics in this dataset.
- High case counts: Several rules connect `Confirmed_High` with `Recovered_High`, `Active_High`, and `Deaths_High`. This suggests that countries with confirmed cases above the dataset median frequently share other high-value categories.
- Low case counts: The rule `WHO_Region_Americas, Recovered_Low, Deaths_Low → Active_Low, Confirmed_Low` also has a lift above 2.3. This indicates a positive association between these low-value categories in the dataset.

### 2. What does lift mean?

| Lift value | Interpretation                                         |
| ---------- | ------------------------------------------------------ |
| Lift = 1   | No association beyond what independence would predict. |
| Lift > 1   | Positive association.                                  |
| Lift < 1   | Negative association.                                  |

The rules in your graph have lift values of approximately 2.3–2.5, suggesting positive associations.

### 3. Conclusion for your report

The Apriori algorithm identified relationships among COVID-19 confirmed cases, deaths, recoveries, active cases, and WHO regions. The strongest rule had a lift of approximately 2.52, indicating that its antecedent and consequent occurred together more frequently than expected under independence. The results also show associations between high confirmed cases and other high-value COVID-19 categories, as well as between low confirmed cases and other low-value categories. These findings demonstrate how association rule mining can identify patterns in country-level COVID-19 data. However, the results represent statistical associations and do not establish causation.

### 4. Important limitation

Your graph displays lift only. To evaluate the rules more fully, also examine their support and confidence in `association_rules.csv`. A high lift alone does not tell you how common or reliable a rule is, and the categories are defined using the dataset median rather than medical thresholds.
