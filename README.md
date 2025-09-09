# 💼 Employee Attrition Prediction and Retention Strategies for HR

## 📌 Introduction
Employee attrition (turnover) is a critical challenge for businesses, leading to operational inefficiencies, higher recruitment costs, and reduced workforce morale. By leveraging **predictive analytics and machine learning**, organizations can anticipate which employees are at risk of leaving and take proactive measures to improve retention.  

This project applies **data mining and classification models** to forecast attrition, identify key influencing factors (e.g., salary, overtime, job satisfaction), and provide HR with actionable insights for employee retention strategies.  

## 🎯 Objectives
- Develop predictive classification models to identify employees “likely to stay” or “likely to leave.”
- Discover major contributors to attrition, including compensation, overtime, work-life balance, and job satisfaction.
- Recommend data-driven HR strategies to improve retention.
- Support proactive decision-making with actionable insights.
- Reduce hiring costs and enhance organizational efficiency through better retention.

## 📊 Dataset
- **Source**: Kaggle
- **Records**: 1,471 employees  
- **Features**: 35 attributes (demographics, job roles, compensation, satisfaction, tenure, etc.)
- **Target Variable**: `Attrition (Yes/No)`

### Key Attributes
| Attribute             | Description | Type | Relevance |
|-----------------------|-------------|------|-----------|
| Age                   | Employee age | Integer | Influences attrition risk |
| Attrition             | Employee left (Yes/No) | Categorical | Target variable |
| BusinessTravel        | Travel frequency | Categorical | Impacts work-life balance |
| MonthlyIncome         | Monthly salary | Integer | Strong predictor of attrition |
| JobSatisfaction       | Satisfaction rating (1–4) | Integer | Directly impacts retention |
| OverTime              | Overtime hours (Yes/No) | Categorical | Indicates burnout risk |
| YearsAtCompany        | Tenure in company | Integer | Loyalty indicator |

## 🛠️ Data Preprocessing
- **Data Cleaning**: Removed duplicates and irrelevant constant features (`EmployeeCount`, `Over18`).
- **Feature Engineering**:  
  - Label Encoding for binary variables (e.g., `Attrition`, `OverTime`).  
  - One-Hot Encoding for categorical features (`BusinessTravel`, `JobRole`).  
  - Min-Max Scaling for numerical features (`Age`, `MonthlyIncome`, `DistanceFromHome`).  
- **Data Splitting**: 70% training, 30% testing with stratified sampling to handle class imbalance.

## 🤖 Models Used
Three machine learning models were implemented:
1. **Logistic Regression** – interpretable coefficients, best precision/recall for attrition.  
2. **Random Forest** – handles non-linear interactions, provides feature importance.  
3. **Gradient Boosting** – sequential learning, strong on imbalanced datasets.  

### Evaluation Metrics
| Model               | Accuracy | Precision | Recall | F1-Score |
|---------------------|----------|-----------|--------|----------|
| Logistic Regression | 0.89     | 0.70      | 0.34   | 0.46     |
| Random Forest       | 0.86     | 0.62      | 0.08   | 0.14     |
| Gradient Boosting   | 0.87     | 0.57      | 0.26   | 0.36     |

📌 **Key Finding**: Logistic Regression outperformed other models in identifying attrition cases, despite dataset imbalance.

## 📈 Exploratory Data Analysis (EDA) Highlights
- Majority of workforce aged **30–40 years** → mid-career group most vulnerable.  
- Employees with **low income ($2000–5000)** show higher attrition risk.  
- Attrition is highest in employees with **≤5 years tenure**.  
- **Frequent overtime and business travel** strongly correlated with resignations.  
- Job satisfaction and work-life balance play crucial roles in retention.  

## 🔑 Key Insights
- **Compensation**: Low salaries strongly drive attrition → need competitive pay & incentives.  
- **Workload**: Frequent overtime increases burnout → review work-hour policies.  
- **Career Growth**: Employees with limited promotion prospects are more likely to leave.  
- **Demographics**: Young and single employees show higher turnover intentions.  
- **Engagement**: Job involvement and satisfaction reduce attrition risk significantly.  

## ✅ Recommendations
1. **Compensation Strategy**  
   - Regular salary benchmarking and performance-based incentives.  
   - Stock options and bonuses to retain high performers.  

2. **Work-Life Balance**  
   - Flexible working hours, remote work options, and reduced overtime.  
   - Recognition and rewards for extra effort.  

3. **Career Development**  
   - Mentorship, training, and promotion opportunities for younger employees.  
   - Transitional roles and retirement support for older employees.  

4. **Employee Engagement**  
   - Regular job satisfaction surveys.  
   - Feedback mechanisms to address workplace concerns.  

5. **Tenure Support**  
   - Strong onboarding and career progression pathways.  
   - Enhance employee involvement and recognition programs.  

## 📌 Conclusion
Employee attrition is driven by a mix of financial, personal, and work-related factors. Among the tested models, **Logistic Regression proved most effective** for predicting turnover cases.  

By addressing salary competitiveness, managing overtime, improving work-life balance, and fostering career growth, organizations can significantly reduce attrition. Implementing predictive analytics equips HR teams with data-driven insights to proactively retain talent and improve organizational resilience.  

## ⚙️ Tech Stack
- **Python** (pandas, numpy, scikit-learn, matplotlib, seaborn)  
- **Machine Learning**: Logistic Regression, Random Forest, Gradient Boosting  
- **Visualization**: Matplotlib, Seaborn  
- **Dataset Source**: Kaggle  
