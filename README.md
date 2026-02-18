Sicily Airbnb Investment Analysis

Data-driven analysis of 50.000+ Airbnb listings across Sicily to identify optimal investment opportunities.

[Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[Pandas](https://img.shields.io/badge/Pandas-2.0+-green.svg)](https://pandas.pydata.org/)

Author: Monika Kwiatkowska  
Project Date: February 2026

Project Overview

This project analyses the Sicily Airbnb market from an investor perspective, providing insights on:
- Where to invest (location analysis across 50+ neighborhoods)
- What to buy (property type performance comparison)
- How to operate (Superhost performance benchmarking)

The analysis examines 50,394 Airbnb listings across Sicily, delivering data-driven recommendations for property investors entering the short-term rental market.

Context: Created as part of my Data Analytics portfolio, demonstrating end-to-end analysis from data cleaning through strategic recommendations. Connects directly to my experience as a Sales Analyst in the travel industry.

Business Questions

1. Which neighborhoods in Sicily offer the best investment potential?
Comprehensive analysis of pricing power, competition levels, and market dynamics to identify high-ROI opportunities.

2. What property features and types drive higher revenue?
Comparison of property types, room configurations, and market positioning to determine optimal investments.

3. How do Superhost properties perform compared to regular listings?
Quantitative analysis of Superhost premium: pricing, reviews, and revenue implications.

Key Findings

Finding #1: Suburban Coastal Premium
Beach towns near Palermo command 30% higher prices with 95% less competition than the capital city

- Carini: €127/night average (327 listings)
- Terrasini: €120/night average (338 listings)  
- Palermo City: €97/night average (7,330 listings)

Strategic Insight: Coastal locations offer pricing premiums but require higher minimum stays (5-6 days vs 4.8 in Palermo), indicating more seasonal, vacation-focused demand.

Finding #2: Three Distinct Market Segments
Clear segmentation creates different investment opportunities based on risk tolerance

| Market Segment | Location | Avg Price | Listings | Guest Profile | Risk Level |
| Premium  | Carini/Terrasini | €120-127 | 300-400 | Beach tourists | Medium-High (seasonal) |
| Volume    | Palermo City | €97 | 7,330 | Urban/year-round | Low-Medium (competition) |
| Value     | Bagheria | €92 | 178 | Budget travelers | Low (emerging) |

Key Takeaway: Sicily offers diverse entry points for different investor profiles - from high-premium coastal properties to stable urban volume plays.

Finding #3: Superhost Status Drives Measurable Premium
Superhosts generate 8% higher revenue through pricing power and booking advantages

Performance Metrics:
- Pricing Premium: +7.9% (€124 vs €115/night)
- Review Advantage: 4.86 vs 4.71 rating (+0.15 points)
- Booking Proof: 54 average reviews vs 13 for regular hosts (+314%)
- Market Share: 24.7% of listings are Superhosts
- Annual Impact: €1,652 additional revenue per year

ROI Analysis: For serious investors, Superhost status provides €1,652/year premium that justifies the operational investment in maintaining 4.8+ ratings and 90%+ response rates.

Investment Recommendations

Strategy A: Premium Coastal Investment
Target: Carini or Terrasini beach properties

Financial Projection:
- Average nightly rate: €120-127
- Expected annual revenue: €22,000-23,000 (50% occupancy)
- Revenue premium vs Palermo: +26%

Advantages:
- 30% higher nightly rates
- 95% less competition than Palermo
- Strong beach tourism demand

Risks:
- Seasonal concentration (higher min stays)
- Weather dependency
- Vacation-only positioning

Ideal For: Investors with capital for quality beachfront properties, comfortable with seasonal cash flow patterns.

Strategy B: Volume Urban Investment  
Target: Palermo city apartments

Financial Projection:
- Average nightly rate: €97
- Expected annual revenue: €17,700 (50% occupancy)
- Market size: 7,330 active listings

Advantages:
- Year-round urban demand
- Flexible booking patterns (4.8 day minimum)
- Business + tourist traffic

Risks:
- Intense competition (7,330 listings)
- Price compression
- Lower per-night margins

Ideal For: Investors prioritizing occupancy stability over premium pricing; those comfortable with competitive marketing.

Strategy C: Value Entry Point
Target: Bagheria suburban properties

Financial Projection:
- Average nightly rate: €92
- Expected annual revenue: €16,800 (50% occupancy)
- Competition: Only 178 listings

Advantages:
- Minimal competition
- Lower acquisition costs
- Proximity to Palermo (suburban access)

Risks:
- Lower tourist brand recognition
- Unproven demand levels
- May require aggressive pricing

Ideal For: First-time investors testing the market; value-focused plays banking on future Palermo metro growth.

Methodology

Data Collection
- Source: [Inside Airbnb](http://insideairbnb.com/get-the-data.html) 
- Region: Sicily, Italy (all neighborhoods)
- Date: February 2026 
- Initial Sample: 57,531 listings
- Final Sample: 50,394 listings after cleaning 

Data Processing

1. Price Standardization
- Removed currency symbols ($, €) and commas
- Converted to numeric format
- Filtered outliers: removed prices <€10 or >€1,000
- Rationale: Focus on typical investment properties

2. Missing Value Treatment
- Price (5,642 missing): Deleted rows - cannot analyse without price
- Bedrooms (978 missing): Filled with median values
- Reviews (15,940 missing): Set to 0 for new listings without reviews
- Neighbourhoods (critical): Deleted incomplete records

3. Feature Engineering
- Created `price_category`: Budget (<€50), Mid-range (€50-150), Luxury (>€150)
- Calculated `est_annual_revenue`: price × 365 × 0.5 (50% occupancy assumption)
- Converted `is_superhost`: Binary field from 't'/'f' string values

Analysis Techniques

Exploratory Data Analysis:
- Distribution analysis and statistical summaries
- Outlier detection and treatment
- Correlation exploration

Segmentation Analysis:
- Geographic clustering by price and competition
- Property type performance comparison  
- Host category benchmarking (Superhost vs Regular)

Investment Scoring:
- Multi-criteria framework combining pricing power and competition levels
- Normalized metrics for cross-comparison
- Risk-reward classification

Key Assumptions
- 50% Occupancy Rate: Conservative industry standard for vacation rentals
- Static Market: Current pricing trends assumed to continue
- Representative Sample: Inside Airbnb data captures full market dynamics

Tech Stack

Programming & Analysis:
- Python 3.8+
- pandas - Data manipulation and aggregation
- NumPy - Numerical computations  
- Matplotlib & Seaborn - Data visualization

Environment:
- Jupyter Notebook - Interactive analysis
- Google Colab - Cloud execution
- Google Drive - Data storage

Project Structure

sicily-airbnb-analysis/
│
├── README.md                          # Project overview 
│
├── sicily_airbnb.ipynb                # Complete analysis notebook
│   ├── Data Exploration               # Initial EDA and quality checks
│   ├── Data Cleaning                  # Preprocessing and feature engineering
│   ├── Market Analysis                # Neighbourhood and property analysis
│   ├── Palermo Deep Dive              # Metropolitan area comparison
│   ├── Superhost Analysis             # Performance benchmarking
│   └── Investment Recommendations     # Strategic insights
│
├── data/                              # Data files (not in repo - download from source)
│   ├── listings.csv                   # Raw data
│   └── listings_cleaned.csv           # Processed data
│
└── requirements.txt                   # Python dependencies

How to Run

Prerequisites
- Python 3.8 or higher
- Google Colab account (free) OR local Jupyter installation

Option 1: Google Colab (Recommended - No Installation)

1. Open the notebook
   - Click on `sicily_airbnb.ipynb` in this repository
   - Click "Open in Colab" button

2.*Download data
   - Visit [Inside Airbnb - Sicily](http://insideairbnb.com/get-the-data.html)
   - Download `listings.csv.gz` for Sicily 
   - Upload to your Google Drive: `/Sicily_Airbnb_Project/data/listings.gz`

3. Run the analysis
   - Mount Google Drive (first cell)
   - Runtime = Run all
   - Analysis completes in 5 minutes

Option 2: Local Installation

1. Clone repository
```bash
git clone https://github.com/your-username/sicily-airbnb-analysis.git
cd sicily-airbnb-analysis
```

2. install dependencies
```bash
pip install -r requirements.txt
```

3. Download data (same as above)

4. Run Jupyter
```bash
jupyter notebook sicily_airbnb.ipynb
```

Limitations & Future Work

Current Limitations

Temporal Constraints:
- Snapshot data from single point in time (February 2026)
- No historical trend analysis or year-over-year growth calculations
- Cannot model seasonal price variations

Occupancy Assumptions:
- Revenue estimates based on 50% occupancy assumption
- Actual booking rates may vary significantly by location and season
- No access to real occupancy or booking data

Market Dynamics:
- Static analysis does not account for competitive responses
- Regulatory changes not incorporated
- Tourism trends and external factors not modelled

Future Enhancements

Phase 2 Additions:
- Calendar data integration for month-by-month seasonality analysis
- Historical data tracking for growth trend identification
- Predictive occupancy modeling using machine learning
- Amenity-level analysis (pool, parking, sea view pricing impact)
- Dynamic pricing recommendations

Phase 3 Advanced:
- Competitor density heatmaps with geographic clustering
- Guest review sentiment analysis (NLP)
- Multi-year ROI modelling with appreciation assumptions
- Regulatory risk assessment by municipality
About

This project was created as part of my Data Analytics portfolio, demonstrating practical skills in:

Business Analysis - Translating data into strategic investment recommendations  
Data Wrangling - Cleaning and preprocessing 50k+ records  
Exploratory Analysis - Uncovering non-obvious market patterns  
Statistical Analysis - Segmentation and comparative benchmarking  
Data Visualization - Communicating insights through charts  
Strategic Thinking - Risk-reward frameworks and investor profiling  

Background: MSc Data Analytics graduate (April 2026) with hands-on experience as a Sales Analyst in the travel industry. This project combines analytical rigor with domain expertise in tourism and hospitality data.

Why This Project Matters: During my sales analyst role, I regularly analysed booking patterns and market performance using Tableau and Excel. This Sicily analysis extends those skills to a comprehensive investment framework, demonstrating the ability to deliver actionable business intelligence.

Connect With Me

I'm actively seeking Data Analyst and Business Intelligence roles in Berlin's tech ecosystem.

- LinkedIn: https://www.linkedin.com/in/monikakwiatkowska/
- Email: 6monikakwiatkowska@gmail.com
- GitHub: https://github.com/monikkwiatkowska

Skills: Python • SQL • Tableau • Excel • Data Analysis • Business Intelligence • Statistical Analysis

License

This project is open source and available under the MIT License.

Acknowledgments

- Data Source: [Inside Airbnb](http://insideairbnb.com/) - Thank you for making tourism data publicly available for analysis
- Inspiration: Real-world investment decision frameworks for short-term rental markets
- Learning: This project was developed to demonstrate end-to-end analytical capabilities for portfolio purposes

Last Updated: February 2026
Analysis based on data current as of September 2025

If you found this analysis helpful, please star this repository!

