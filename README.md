# Quantium Data Analytics - Retail Strategy Project

## 🛒 Project Overview

This project demonstrates advanced retail analytics capabilities through a comprehensive analysis of customer transaction data and store performance metrics. Completed as part of the Quantium Data Analytics job simulation, the project focuses on analyzing chip purchasing behaviors, identifying key customer segments, and evaluating the effectiveness of new store layouts through controlled experimentation.

## 🎯 Business Objectives

- Analyze customer purchasing behaviors to identify high-value segments
- Evaluate the impact of trial store layouts on sales performance
- Provide data-driven recommendations for category management and store optimization
- Develop a framework for ongoing performance monitoring and testing

## 📊 Project Structure

The project consists of three interconnected tasks:

### Task 1: Data Preparation and Customer Analytics
Comprehensive analysis of transaction data to understand customer purchasing patterns and identify key business opportunities.

### Task 2: Experimentation and Uplift Testing
Statistical evaluation of trial store performance using matched control stores to measure the true impact of layout changes.

### Task 3: Analytics and Commercial Application
Executive reporting using the Pyramid Principle to communicate findings and strategic recommendations.

## 🔍 Key Findings

### Customer Segmentation Analysis

#### Top Performing Segments:
1. **Older Families (Budget)** - Highest total spend ($156,863.75) despite small population
2. **Young Singles/Couples (Mainstream)** - Large customer base with high engagement
3. **Retirees (Mainstream)** - Consistent purchasers with predictable patterns

#### Purchase Behavior Insights:
- **Average chips per customer**: Older Families lead with 9.07-9.25 packs per customer
- **Price sensitivity**: Mainstream Young/MidAge Singles & Couples willing to pay $4.00-4.07 per unit
- **Seasonal trends**: December shows peak sales with 21,225 transactions

### Product Performance

#### Top Brands by Segment:
- **Universal favorites**: Kettle, Doritos, Pringles
- **Mainstream preferences**: Tyrrells (+23% affinity), Twisties (+23% affinity)
- **Underperformers**: Burger chips (-50% affinity)

#### Pack Size Analysis:
- **Most popular**: 175g (highest volume)
- **Secondary preference**: 150g
- **Opportunity**: 270g shows high affinity but lower current sales

### Store Trial Results

| Trial Store | Control Store | Sales Uplift | Customer Uplift | Trial Period Performance |
|------------|--------------|--------------|-----------------|-------------------------|
| Store 77 | Store 233 | Positive | Significant | 2/3 months significant |
| Store 86 | Store 155 | Mixed | Positive | High customer volume, lower conversion |
| Store 88 | Store 237 | Positive | Moderate | 2/3 months significant |

## 💡 Strategic Recommendations

### 1. Customer-Focused Strategies

#### Older Families (Budget)
- Implement value pack promotions (Buy 2, Get 1 Free)
- Focus on bulk purchasing options
- Position products for family sharing occasions

#### Young Singles/Couples (Mainstream)
- Introduce premium and limited-edition flavors
- Leverage trendy marketing and social media engagement
- Create combo deals with complementary products

#### Retirees (Mainstream)
- Emphasize trusted, established brands
- Cross-promote with dips and accompaniments
- Maintain consistent pricing and availability

### 2. Product Optimization

#### Inventory Management
- Increase stock of 175g and 150g pack sizes
- Test expanded distribution of 270g packs
- Phase out underperforming Burger chips SKUs

#### Brand Partnerships
- Develop exclusive flavors with Kettle, Doritos, and Pringles
- Create store-brand alternatives for price-sensitive segments
- Launch seasonal limited editions for holiday peaks

### 3. Store Layout Implementation

Based on trial results:
- **Rollout Strategy**: Prioritize implementation in stores similar to Trial Store 77
- **Conversion Focus**: Apply Store 86 learnings to improve transaction values
- **Monitoring Framework**: Establish KPIs for ongoing performance tracking

## 📈 Technical Implementation

### Data Processing Pipeline

```python
# Key libraries used
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
from scipy import stats
from datetime import datetime

# Core analysis functions
def segment_customers(df):
    """Segment customers by affluence and life stage"""
    return df.groupby(['LIFESTAGE', 'PREMIUM_CUSTOMER']).agg({
        'TOT_SALES': 'sum',
        'LYLTY_CARD_NBR': 'nunique',
        'PROD_QTY': 'mean'
    })

def match_control_stores(trial_store, candidate_stores, metrics):
    """Find best control store match using correlation analysis"""
    # Implementation details in notebooks
    pass

def calculate_uplift(trial_sales, control_sales, scaling_factor):
    """Calculate sales uplift with statistical significance"""
    # Implementation details in notebooks
    pass
```

### Statistical Methods

- **T-tests**: Comparing trial vs control store performance
- **Correlation analysis**: Matching control stores to trial stores
- **Time series analysis**: Identifying seasonal patterns
- **Affinity indexing**: Understanding segment preferences


## 🛠️ Setup Instructions

### Prerequisites
- Python 3.7+
- Jupyter Notebook
- Microsoft Excel (for viewing source data)

### Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/quantium-retail-analytics.git
cd quantium-retail-analytics

# Create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Launch Jupyter Notebook
jupyter notebook
```

### Required Libraries

```txt
pandas==1.3.0
numpy==1.21.0
matplotlib==3.4.2
seaborn==0.11.1
scipy==1.7.0
scikit-learn==0.24.2
jupyter==1.0.0
openpyxl==3.0.7
```

## 📊 Key Visualizations

The analysis includes several critical visualizations:

1. **Transaction Trends**: Year-over-year comparison showing seasonal patterns
2. **Customer Segmentation Matrix**: Total sales by customer segment
3. **Product Affinity Analysis**: Brand and pack size preferences by segment
4. **Trial Store Performance**: Statistical significance testing results

## 🏆 Business Impact

### Quantifiable Results:
- Identified $376,013.65 opportunity in Older Singles/Couples segment
- Discovered 23% higher affinity for Tyrrells and Twisties in Mainstream segment
- Validated store layout changes with statistically significant sales uplift

### Strategic Value:
- Data-driven framework for category management decisions
- Scalable methodology for future store trials
- Customer-centric approach to product assortment

## 📝 Methodology Notes

### Data Quality Considerations
- Handled date formatting inconsistencies in transaction data
- Removed outlier transactions (e.g., negative quantities)
- Validated customer segment assignments

### Statistical Rigor
- 95% confidence intervals for all trial comparisons
- Multiple hypothesis testing corrections applied
- Seasonal adjustments for fair comparisons

## 🚀 Future Enhancements

1. **Predictive Modeling**: Develop forecasting models for demand planning
2. **Real-time Dashboards**: Create interactive visualizations for ongoing monitoring
3. **Basket Analysis**: Examine product combinations and cross-selling opportunities
4. **Price Optimization**: Test price elasticity by segment
5. **Geographic Expansion**: Apply learnings to new store locations

## 👥 Contributors

- **Andrea Che** - Data Analysis, Visualization, and Reporting
- **Quantium Team** - Project guidance and data provision

## 🙏 Acknowledgments

This project was completed as part of the Quantium Data Analytics job simulation, providing real-world experience with retail analytics and strategic decision-making.

## 📜 License

This project is for educational and portfolio purposes. The data and analysis methodologies remain the property of Quantium Group Pty Limited.

---

