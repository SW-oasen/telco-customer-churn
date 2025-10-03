# Power BI Dashboard Analysis - Telco Customer Churn
## Visual Documentation and Business Conclusions

**Dashboard File**: `telco-customer-churn.pbix` | `telco-customer-churn.pdf`  
**Data Source**: `churn_scored_tuned.csv` (1,410 customer records)  
**Analysis Date**: October 2025  
**Model Accuracy**: ~77.7%

---

## 📊 **Dashboard Structure Overview**

### **Page 1: Executive Summary Dashboard**
*Strategic overview for senior management*

#### Key Performance Indicators (KPI Cards)
1. **Overall Churn Rate**: 26.5%
   - **Status**: Red (Above 25% threshold)
   - **Business Impact**: Critical - immediate attention required
   - **Benchmark**: Industry average ~15-20%

2. **At-Risk Customers**: 178 customers
   - **Definition**: High and Very High risk categories (churn probability >50%)
   - **Revenue Impact**: Potential annual loss if churned
   - **Priority**: Immediate intervention required

3. **Annual Revenue at Risk**: $276,919K
   - **Calculation**: High-risk customers × monthly charges × 12 months
   - **Business Critical**: Significant revenue exposure
   - **Action Required**: Retention campaigns essential

4. **Model Accuracy**: 77.7%
   - **Performance**: Good predictive capability
   - **Confidence Level**: Reliable for business decisions
   - **Model Type**: Ensemble (Random Forest + Gradient Boosting)

#### Primary Visualizations

**Risk Distribution (Donut Chart)**
- **Purpose**: Show proportion of customers by risk level
- **Key Insight**: Risk distribution across customer base
- **Color Coding**: Green (Low) → Yellow (Medium) → Orange (High) → Red (Very High)
- **Business Value**: Quick visual risk assessment

**Churn Trend Analysis (Line Chart)**
- **X-axis**: Customer tenure groups or time periods
- **Y-axis**: Churn rate percentage
- **Key Finding**: New customers (0-12 months) show highest churn risk
- **Business Insight**: Onboarding period is critical for retention

#### Interactive Filters
- **Contract Type**: Month-to-month, One year, Two year
- **Customer Value Segment**: High, Medium, Low value
- **Tenure Groups**: New, Growing, Mature, Loyal customers

---

### **Page 2: Customer Risk Analysis Dashboard**
*Detailed risk factors and feature analysis*

#### Risk Heatmap (Matrix Visual)
- **Rows**: Contract Type (Month-to-month, One year, Two year)
- **Columns**: Payment Method (Electronic check, Credit card, Bank transfer, Mailed check)
- **Values**: Average churn probability
- **Key Finding**: Month-to-month + Electronic check = Highest risk combination
- **Business Action**: Target this segment for contract upgrades

#### Feature Importance Chart (Horizontal Bar Chart)
*Based on comprehensive machine learning analysis*

**Top Risk Factors (Ranked by Importance)**:
1. **Customer Tenure** (13.4%): Most critical predictor
   - **Insight**: New customers at highest risk
   - **Action**: Enhanced onboarding programs

2. **Monthly Charges** (9.5%): Price sensitivity factor
   - **Insight**: Higher charges correlate with churn risk
   - **Action**: Review pricing strategy and value proposition

3. **Total Charges** (8.9%): Customer lifetime value indicator
   - **Insight**: Lower total spend indicates higher risk
   - **Action**: Focus on customer engagement and service usage

4. **Fiber Optic Service** (6.4%): Service-specific risk
   - **Insight**: Fiber customers show different churn patterns
   - **Action**: Investigate service quality issues

5. **Electronic Check Payment** (4.4%): Payment method risk
   - **Insight**: Manual payment correlates with higher churn
   - **Action**: Promote automatic payment methods

6. **Two Year Contract** (3.1%): Contract protection factor
   - **Insight**: Longer contracts reduce churn significantly
   - **Action**: Incentivize long-term commitments

#### Risk Score Distribution (Histogram)
- **Purpose**: Show distribution of churn probability scores
- **X-axis**: Probability ranges (0-1)
- **Y-axis**: Customer count
- **Key Insight**: Identification of natural risk thresholds

---

### **Page 3: Business Intelligence Dashboard**
*Actionable insights and campaign strategies*

#### Campaign Strategy Matrix
**Risk-Based Action Framework**:

| Risk Level | Probability Range | Recommended Action | Priority |
|------------|------------------|-------------------|----------|
| **Very High** | ≥75% | Immediate Call Campaign | Critical |
| **High** | 50-74% | Proactive Outreach Program | High |
| **Medium** | 25-49% | Email Retention Campaign | Medium |
| **Low** | <25% | Monitor & Survey | Low |

#### ROI Calculator (Card Visuals)
- **Potential Savings**: Revenue recoverable through retention
- **Campaign Costs**: Estimated intervention costs ($25 per customer)
- **ROI Percentage**: Return on investment for retention campaigns
- **Business Case**: Financial justification for proactive measures

#### Action Priority Matrix (Scatter Plot)
- **X-axis**: Monthly charges (customer value)
- **Y-axis**: Churn probability (risk level)
- **Size**: Tenure (customer maturity)
- **Color**: Risk category
- **Purpose**: Identify high-value, high-risk customers for priority treatment

---

## 🎯 **Key Business Conclusions**

### **Critical Findings**

1. **Churn Crisis**: 26.5% churn rate significantly exceeds industry benchmarks
   - **Impact**: Immediate business threat requiring executive action
   - **Cost**: $276K+ annual revenue at risk from identified high-risk customers

2. **Tenure is King**: Customer tenure dominates all other risk factors (13.4% importance)
   - **Critical Period**: First 12 months are make-or-break for retention
   - **Business Priority**: Invest heavily in new customer onboarding and early engagement

3. **Pricing Pressure**: Combined pricing factors (Monthly + Total charges) account for 18.4% of churn risk
   - **Challenge**: Price sensitivity is a major churn driver
   - **Opportunity**: Value-based pricing and service bundling strategies

4. **Payment Method Matters**: Electronic check users show elevated churn risk
   - **Root Cause**: Manual payment friction increases churn likelihood
   - **Solution**: Migrate customers to automatic payment methods

5. **Contract Length Protection**: Two-year contracts significantly reduce churn
   - **Strategy**: Aggressive promotion of long-term commitments with incentives
   - **Trade-off**: Balance contract length with customer flexibility

### **Strategic Recommendations**

#### **Immediate Actions (0-30 days)**
1. **Emergency Intervention**: Launch immediate call campaign for 178 high-risk customers
2. **Payment Migration**: Offer incentives to move electronic check users to auto-pay
3. **Retention Budget**: Allocate emergency budget for high-value, high-risk customers

#### **Short-term Initiatives (1-3 months)**
1. **New Customer Success Program**: 
   - Dedicated onboarding team for first 12 months
   - Regular check-ins and service optimization
   - Early warning system for engagement drops

2. **Pricing Strategy Review**:
   - Value-based pricing analysis
   - Service bundle optimization
   - Competitive pricing benchmarking

3. **Contract Incentive Program**:
   - Two-year contract promotions
   - Equipment upgrades for long-term commitments
   - Service add-ons for contract extensions

#### **Long-term Strategic Shifts (3-12 months)**
1. **Customer Experience Transformation**:
   - Fiber service quality improvements
   - Digital payment experience enhancement
   - Proactive customer service model

2. **Predictive Analytics Integration**:
   - Real-time churn scoring system
   - Automated intervention triggers
   - Continuous model improvement

3. **Customer Segmentation Strategy**:
   - Value-based service tiers
   - Personalized retention offers
   - Risk-adjusted customer management

### **Expected Business Impact**

**Revenue Protection**: Successfully implementing these recommendations could:
- Reduce churn rate from 26.5% to 18-20% (industry average)
- Protect $200K+ in annual revenue
- Improve customer lifetime value by 15-25%
- Generate positive ROI within 6 months

**Competitive Advantage**: 
- Industry-leading customer retention rates
- Data-driven customer management
- Predictive intervention capabilities

---

## 📈 **Dashboard Usage Guidelines**

### **For Executives**
- Focus on **Page 1 (Executive Summary)** for strategic overview
- Monitor KPI trends monthly
- Use for board presentations and strategic planning

### **For Marketing Teams**
- Use **Page 3 (Business Intelligence)** for campaign planning
- Leverage risk segments for targeted messaging
- Track campaign ROI and effectiveness

### **For Customer Success Teams**
- Reference **Page 2 (Risk Analysis)** for operational insights
- Prioritize high-risk customer interventions
- Monitor feature importance for service improvements

### **For Data Analytics Teams**
- Maintain model accuracy monitoring
- Update risk thresholds based on business feedback
- Continuously refine predictive capabilities

---

## 🔧 **Technical Notes**

- **Data Refresh**: Monthly recommended, weekly during critical periods
- **Model Retraining**: Quarterly or when accuracy drops below 75%
- **Dashboard Performance**: Optimized for <3 second load times
- **User Access**: Role-based permissions configured

**File Locations**:
- **Source Data**: `/reports/tables/churn_scored_tuned.csv`
- **Dashboard**: `/dashboards/telco-customer-churn.pbix`
- **Documentation**: `/dashboards/PowerBI_Step_By_Step_Guide.md`

---

*This analysis represents a critical business intelligence tool for customer retention strategy. Regular monitoring and action on these insights is essential for business success.*