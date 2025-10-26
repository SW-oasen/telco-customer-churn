# Telco Customer Churn Analysis

A comprehensive machine learning project for predicting customer churn in telecommunications industry using advanced analytics, feature engineering, and multiple modeling approaches.

## portfolio website on GitHub
https://sw-oasen.github.io/yuchuan-portfolio/#projects

## 📊 Project Overview

This project analyzes customer churn patterns for a telecommunications company and builds predictive models to identify customers at risk of churning. The analysis includes exploratory data analysis, feature engineering, hyperparameter optimization, and comprehensive feature importance analysis.

## 🎯 Objectives

- **Predict Customer Churn**: Build accurate ML models to identify at-risk customers
- **Feature Analysis**: Understand key drivers of customer churn behavior
- **Business Intelligence**: Provide actionable insights for retention strategies
- **Model Optimization**: Implement advanced hyperparameter tuning and threshold optimization
- **Interpretability**: Use multiple methods to explain model predictions

## 📁 Project Structure

```
telco-customer-churn/
├── data/
│   ├── WA_Fn-UseC_-Telco-Customer-Churn.csv    # Original dataset
│   └── telco__customer_churn_clean.csv          # Cleaned dataset
├── notebooks/
│   ├── 01_data_prep.ipynb                       # Data cleaning & EDA
│   ├── 02_modeling.ipynb                        # Baseline modeling
│   ├── 03_feature_engineering_and_tuning.ipynb  # Advanced ML pipeline
│   └── 04_feature_importance_analysis.ipynb     # Feature analysis
├── reports/
│   ├── figures/                                 # Generated visualizations
│   └── tables/
│       ├── churn_scored_holdout.csv            # Baseline predictions
│       └── churn_scored_tuned.csv              # Optimized predictions
├── dashboards/                                  # Power BI dashboards
└── README.md
```

## 🔧 Technology Stack

### Core Libraries
- **Python 3.8+**
- **Pandas** - Data manipulation and analysis
- **NumPy** - Numerical computing
- **Scikit-learn** - Machine learning algorithms
- **Matplotlib/Seaborn** - Data visualization

### Advanced Libraries
- **Optuna** - Bayesian hyperparameter optimization
- **SHAP** *(optional)* - Model interpretability
- **Plotly** *(optional)* - Interactive visualizations

### Models Used
- **RandomForestClassifier** - Ensemble tree-based model
- **HistGradientBoostingClassifier** - Gradient boosting
- **LogisticRegression** - Linear baseline model

## 🚀 Quick Start

### 1. Environment Setup
```bash
# Clone or download the project
cd telco-customer-churn

# Install required packages
pip install pandas numpy scikit-learn matplotlib seaborn optuna

# Optional: Install advanced visualization libraries
pip install plotly shap
```

### 2. Run Analysis
Execute notebooks in order:

1. **Data Preparation**: `01_data_prep.ipynb`
   - Data cleaning and preprocessing
   - Exploratory data analysis
   - Data quality assessment

2. **Baseline Modeling**: `02_modeling.ipynb`
   - Model comparison and evaluation
   - Threshold optimization
   - Performance metrics analysis

3. **Advanced Pipeline**: `03_feature_engineering_and_tuning.ipynb`
   - Feature engineering and interaction terms
   - Automated hyperparameter optimization
   - Production-ready model pipeline

4. **Feature Analysis**: `04_feature_importance_analysis.ipynb`
   - Multi-method feature importance analysis
   - SHAP interpretability (if available)
   - Statistical significance testing

## 📈 Key Features

### Data Processing
- ✅ Automated data cleaning and preprocessing
- ✅ ID column detection and removal
- ✅ Missing value handling
- ✅ Categorical encoding with OneHotEncoder
- ✅ Numerical feature scaling

### Feature Engineering
- ✅ **Tenure Buckets** - Customer lifecycle segmentation
- ✅ **Service Count** - Total subscribed services indicator
- ✅ **Revenue to Date** - Customer value calculation
- ✅ **Contract-Payment Risk** - High-churn combination detection
- ✅ **Family Status** - Customer demographic grouping

### Model Optimization
- ✅ **Bayesian Optimization** with Optuna (50 trials each)
- ✅ **Cross-validation** based model selection
- ✅ **Threshold Optimization** for business metrics
- ✅ **Automated parameter tuning** for multiple algorithms

### Feature Importance Analysis
- ✅ **Tree-based Importance** - Feature split contribution
- ✅ **Permutation Importance** - Predictive value assessment
- ✅ **Correlation Analysis** - Linear relationship detection
- ✅ **SHAP Values** - Local and global interpretability
- ✅ **Statistical Testing** - Significance validation

## 📊 Model Performance

### Baseline Results
- **Random Forest**: ~85% accuracy, 0.82+ AUC
- **Gradient Boosting**: ~84% accuracy, 0.81+ AUC  
- **Logistic Regression**: ~80% accuracy, 0.78+ AUC

### Optimized Results
- **Best Model**: Determined by hyperparameter optimization
- **Optimized Threshold**: Balanced precision/recall for actionable predictions
- **Risk Categories**: Low, Medium, High, Very High customer segments

## 💼 Business Impact

### Customer Segmentation
- **High-Risk**: Month-to-month + Electronic check customers
- **New Customers**: 0-12 months tenure require attention
- **Service Engagement**: Fewer services = higher churn risk

### Retention Strategies
1. **Contract Incentives** - Promote long-term contracts
2. **Payment Optimization** - Encourage automatic payments
3. **Service Bundling** - Increase customer engagement
4. **Early Intervention** - Target new customer onboarding

### Expected Business Value
- **Improved Retention** through targeted interventions
- **Cost Optimization** by focusing on high-risk segments
- **Revenue Protection** via proactive customer engagement

## 📋 Output Files

### Prediction Files
- `churn_scored_holdout.csv` - Baseline model predictions with risk categories
- `churn_scored_tuned.csv` - Optimized model predictions with enhanced features

### Analysis Reports  
- `consolidated_feature_rankings.csv` - Feature importance across all methods
- `statistical_significance.csv` - Feature significance test results
- Various visualization outputs in `reports/figures/`

### File Schema
```csv
customerid, churn_actual, churn_proba, churn_pred, risk_category, [original_features...]
```

## 🔍 Key Insights

### Top Churn Drivers
1. **Contract Type** - Month-to-month contracts show highest churn
2. **Payment Method** - Electronic check payments correlate with churn
3. **Tenure** - New customers (0-12 months) at highest risk
4. **Service Engagement** - Fewer subscribed services increase churn probability
5. **Monthly Charges** - Higher charges without proportional value increase risk

### Statistical Findings
- **Feature Significance**: Most engineered features show statistical significance (p < 0.05)
- **Model Consistency**: Feature importance rankings consistent across multiple methods
- **Predictive Power**: Advanced features improve model performance by 3-5% AUC

## 🛠 Customization

### Adding New Features
1. Modify `create_engineered_features()` function in notebook 03
2. Update preprocessing pipeline for new data types
3. Re-run hyperparameter optimization for best results

### Model Selection
- Change `models` dictionary in notebooks to test different algorithms
- Adjust Optuna parameters for different optimization strategies
- Modify cross-validation strategy based on data characteristics

### Business Rules
- Update threshold optimization criteria in notebook 02/03
- Modify risk categories in export functions
- Adjust evaluation metrics based on business priorities

## 📚 Dependencies

### Required
```
pandas>=1.3.0
numpy>=1.21.0
scikit-learn>=1.0.0
matplotlib>=3.4.0
seaborn>=0.11.0
optuna>=3.0.0
```

### Optional (Enhanced Features)
```
plotly>=5.0.0          # Interactive visualizations
shap>=0.41.0           # Advanced model interpretability
```

## 🤝 Contributing

1. Fork the repository
2. Create feature branch (`git checkout -b feature/enhancement`)
3. Commit changes (`git commit -am 'Add new feature'`)
4. Push to branch (`git push origin feature/enhancement`) 
5. Create Pull Request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 📞 Support

For questions or issues:
- Review notebook documentation and comments
- Check output logs for error details
- Verify data file paths and formats
- Ensure all required libraries are installed

## 🎯 Future Enhancements

- [ ] Deep learning models (Neural Networks)
- [ ] Time-series analysis for churn prediction
- [ ] Real-time model deployment pipeline
- [ ] A/B testing framework for retention strategies
- [ ] Advanced feature engineering with domain expertise
- [ ] MLOps pipeline with model monitoring

---

**Last Updated**: October 2025  
**Version**: 1.0  
**Status**: ✅ Production Ready
