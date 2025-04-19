# Retail Analytics Dashboard - Executive Insights

## Overview
This is a job stimulator of Tata Group online retail by Forage. This project provides strategic insights for an online retail business, addressing key questions from the CEO and CMO. The analysis focuses on revenue trends, customer segmentation, and market expansion opportunities while overcoming data challenges including missing customer names and 4,000+ unique product descriptions.

**Key Technical Components**:
- Created product categorization logic using REGEX
- Developed seasonal trend analysis
- Implemented forecasting models
- Designed interactive dashboards for executive decision-making

---

## Q1: CEO - Seasonal Revenue Analysis (2011)

### Objective
Analyze monthly revenue trends and seasonal patterns to inform next year's forecasting strategy.

**Approach**:
1. Excluded 2010 data and postage fees
2. Created product categories and seasonal trends using REGEX patterns
3. Implemented 3-month and 12-month forecasting models

**Key Visualizations**:
1. **Monthly Revenue by Category**  
   ![Line Chart](link-to-screenshot)  
   - Gift Items dominated revenue (67% of total)
   - November peak: $1,071,746 (Christmas shopping surge)
   
2. **Seasonal Trends Analysis**  
   ![Area Chart](link-to-screenshot)  
   - Winter accounted for 42% of annual revenue
   - Seasonal Decorations peaked at $1,424,981 in November

3. **Product Forecast Models**  
   ![Forecast Charts](link-to-screenshot)  
   - Seasonal Decorations projected to grow 38% QoQ in 2012
   - Gift Items forecast to maintain stable growth (+12% YoY)

**Strategic Insights**:
- Prioritize inventory for Seasonal Decorations in Q4
- Expand Gift Items assortment for holiday gifting
- Develop winter-themed marketing campaigns

---

## Q2: CMO - Top 10 Country Analysis

### Objective
Identify high-potential markets excluding domestic (UK) performance.

**Key Findings**:
![Dual-Axis Chart](link-to-screenshot)  
1. Netherlands leads with $268K revenue (580% higher than average)
2. Germany shows strong quantity-volume ratio (2,850 units/$150K revenue)
3. France demonstrates premium product potential (High revenue/unit ratio)

**Action Items**:
- Develop localized marketing for Benelux region
- Consider distribution centers in Germany for efficiency
- Explore premium product lines in France

---

## Q3: CMO - Customer Retention Strategy

### Objective
Identify top 10 customers for retention and loyalty programs.

**Key Visualization**:
![Pareto Chart](link-to-screenshot)  
- Top 3 customers contribute 58% of total revenue
- 90% revenue concentration in top 7 customers

**Retention Strategy**:
1. Implement VIP customer program
2. Create personalized product bundles
3. Develop account-based marketing campaigns

---

## Q4: CEO - Global Expansion Planning

### Objective
Identify high-demand regions for international expansion.

**Heatmap Analysis**:
![Global Heatmap](link-to-screenshot)  
1. Western Europe shows concentrated demand (Netherlands, Germany, France)
2. Nordic countries demonstrate emerging potential
3. APAC region shows untapped opportunities

**Expansion Strategy**:
1. Phase 1: Strengthen European presence
2. Phase 2: Explore Nordic fulfillment centers
3. Phase 3: Localize offerings for APAC markets

---

## Data Challenges & Solutions

1. **Missing Customer Data**  
   - Focused on Customer ID analysis for segmentation
   - Created customer lifetime value metrics

2. **Product Categorization**  
   - Developed REGEX-based classification system:
   ```sql
   IF REGEXP_MATCH(LOWER([Description]), 'christmas|winter...') 
   THEN 'Seasonal Decorations'
   ...