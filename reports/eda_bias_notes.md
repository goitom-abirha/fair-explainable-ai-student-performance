# EDA & Initial Bias Notes

## Dataset Overview
- Total rows: 1044
- Total columns: 33
- Numeric features: 16 → ['age', 'Medu', 'Fedu', 'traveltime', 'studytime', 'failures', 'famrel', 'freetime', 'goout', 'Dalc', 'Walc', 'health', 'absences', 'G1', 'G2', 'G3']
- Categorical features: 17 → ['school', 'sex', 'address', 'famsize', 'Pstatus', 'Mjob', 'Fjob', 'reason', 'guardian', 'schoolsup', 'famsup', 'paid', 'activities', 'nursery', 'higher', 'internet', 'romantic']

## Missing Values
- No missing values detected across all features.

## Outcome Variable (G3) Summary
- Mean G3: 11.34
- Min G3: 0
- Max G3: 20

## Group-wise G3 Differences (Bias Inspection)
The table below shows the largest differences in mean G3 across key demographic and socio-economic groups:

| group_var   | min_group   |   min_mean | max_group   |   max_mean |   gap |
|:------------|:------------|-----------:|:------------|-----------:|------:|
| Medu        | 1           |    10.1782 | 4           |    12.5098 | 2.332 |
| Fedu        | 1           |    10.3672 | 0           |    12.3333 | 1.966 |
| school      | MS          |    10.5147 | GP          |    11.6334 | 1.119 |
| internet    | no          |    10.5346 | yes         |    11.5538 | 1.019 |
| romantic    | yes         |    10.8302 | no          |    11.6241 | 0.794 |
| famsize     | GT3         |    11.1897 | LE3         |    11.7092 | 0.519 |
| Pstatus     | T           |    11.299  | A           |    11.6694 | 0.37  |
| sex         | M           |    11.2031 | F           |    11.4484 | 0.245 |

## Interpretations (Auto-generated, edit as needed)
- Some groups show meaningful differences in average G3 scores.
- These gaps may indicate potential bias or structural inequality.
- Further fairness evaluation will be needed during modeling.

---
_This report was auto-generated from Week 2 notebook output._
