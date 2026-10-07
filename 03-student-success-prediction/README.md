# Predicting Student Academic Success

## Question
**What behaviours separate high-performing students from the rest?**

## Data
- 6,607 student records with 19 academic, behavioural and socio-economic features
- Source: [Student Performance Factors – Kaggle](https://www.kaggle.com/datasets/grandmaster07/student-exam-performance-dataset-analysis/data)
- Place the file at `data/StudentPerformanceFactors.csv`
- Target: "High Performer" = exam score above the median (67)

## Method
- Exploratory data analysis of study hours, attendance, parental involvement, tutoring and income
- Filled missing values and encoded 13 categorical features
- Built a **Decision Tree**, tuned depth with 5-fold and 10-fold cross-validation
- Averaged feature importance over 100 random splits
- Built a **Random Forest** of 100 trees and compared it with the single tree

## Key results
| Model | Test accuracy |
|-------|---------------|
| Baseline (always "not high performer") | 54% |
| Decision Tree | 83% |
| **Random Forest** | **90%** |

- **Attendance** and **study hours** account for about 80% of the model's feature importance
- Background factors such as gender, school type and parental education had very little effect

## Files
- `student_success_prediction.ipynb` – full analysis
- `report.pdf` – exported report
