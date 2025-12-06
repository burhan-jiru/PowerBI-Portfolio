# Power BI Dashboard Portfolio

## Dashboard 1: Adventure Works Cycles - Business Performance Dashboard

![Adventure Works Dashboard](https://raw.githubusercontent.com/burhan-jiru/PowerBI-Portfolio/main/Adventure%20Work%20Dashboard.gif)

### Overview
This interactive business intelligence dashboard provides a comprehensive overview of Adventure Works Cycles' performance metrics across multiple dimensions. The dashboard features six key visualizations designed to give stakeholders a 360-degree view of business health and performance trends.

### Key Visualizations

**Revenue Analysis by Geography**: A horizontal bar chart displays revenue distribution across major markets, with the United States leading at $9.44M, followed by the United Kingdom ($5.1M) and Australia ($5.0M), providing immediate insights into geographical performance and market penetration.

**Profitability Breakdown**: The cost and profit analysis reveals product category performance, with Accessories showing the highest profit margin at 26.11%, while Bikes and Clothing maintain margins of 10.91% and 19.07% respectively. This visualization helps identify the most profitable product segments and opportunities for margin optimization.

**Revenue Growth Trends**: A dynamic waterfall-style chart tracks monthly revenue growth rates from 2019 to 2020, highlighting volatility with peaks reaching 798% and significant drops to -100%, enabling stakeholders to identify seasonal patterns, market disruptions, and business cycle trends.

**Customer Segmentation**: The customer type analysis tracks the evolution of new, returning, and this-period customers from 2018 to 2020, showing substantial growth in both new customers (reaching 721) and this-period customers (721), while maintaining a stable returning customer base around 170-193 customers.

**Sales Forecasting**: A time-series visualization combines historical sales data with predictive forecasting, projecting revenue trends through 2021 with confidence intervals, reaching an estimated $0.68M by year-end. The gray shaded area represents forecast uncertainty.

**Key Performance Indicators**: The right panel displays critical metrics including Total Sales ($9.37M), Profit ($4.03M), Profit Margin (42.99%), Customer Count (7,549), Average Order Value ($1.02K), and Average Quantity per Order (2), providing at-a-glance business health indicators.

### Approach & Methodology

**Design Philosophy**: 
- Implemented a warm, earthy color palette (greens, beiges, earth tones) reflecting the outdoor/cycling brand identity
- Used a card-based layout for logical grouping of related metrics
- Ensured visual hierarchy with the most critical KPIs prominently displayed on the right
- Applied consistent spacing and alignment for professional appearance

**Data Modeling**:
- Created a star schema with fact tables for sales transactions and dimension tables for products, customers, geography, and time
- Implemented DAX measures for dynamic calculations including profit margins, growth rates, and customer segmentation
- Built time intelligence functions for year-over-year comparisons and trend analysis
- Designed calculated columns for customer classification logic (new vs. returning)

**Analytical Techniques**:
- Applied forecasting algorithms using Power BI's built-in time series analysis with exponential smoothing
- Utilized waterfall charts for variance analysis in revenue growth
- Implemented cohort analysis for customer behavior tracking
- Created custom tooltip pages for drill-through capabilities (not visible in static image)

### Data Sources

- **Sales Transactions**: Transactional database containing order details, quantities, prices, and timestamps
- **Product Catalog**: Master data for product hierarchies (Bikes, Accessories, Clothing)
- **Customer Database**: Customer demographics, acquisition dates, and purchase history
- **Geographic Data**: Territory and regional sales mapping
- **Sample Dataset**: Adventure Works sample database (Microsoft SQL Server sample database for demonstration purposes)

### Key Insights

1. **Geographic Concentration**: The United States represents approximately 37% of total revenue, suggesting heavy market concentration and opportunity for diversification in other regions.

2. **Product Mix Optimization**: While Bikes generate higher absolute revenue, Accessories deliver superior profit margins (26.11%), indicating potential for strategic focus on high-margin accessories cross-selling.

3. **Revenue Volatility**: The extreme month-over-month fluctuations (ranging from -100% to +798%) suggest significant seasonality or market disruptions, particularly visible during 2019-2020, likely correlated with external market factors or seasonal buying patterns.

4. **Customer Acquisition Success**: The dramatic increase in new customers from 43 (2018) to 721 (2020) represents 16.8x growth, indicating successful marketing initiatives and market expansion strategies.

5. **Order Economics**: With an average order value of $1.02K and average quantity of 2 items, the business model appears focused on higher-value transactions rather than volume plays.

6. **Growth Trajectory**: The sales forecast shows continued upward momentum with projected revenue reaching $0.68M by end of 2021, though the confidence interval suggests moderate uncertainty in forecasting accuracy.

7. **Customer Retention Challenge**: While new customer acquisition is strong, the relatively flat returning customer trend (around 170-193) suggests opportunity for improved retention strategies and loyalty programs.

---

## Dashboard 2: Bloomberg Billionaires Index - Global Wealth Analytics

![til](https://github.com/burhan-jiru/PowerBI-Portfolio/blob/6c349148ef9aecc08eba30656af517a70492a4ce/Bloomberg%20Dashboard.gif)

### Overview
This sophisticated financial dashboard analyzes global wealth distribution and changes among the world's wealthiest individuals, offering multiple perspectives on billionaire wealth dynamics across industries, geographies, and time periods.

### Key Visualizations

**Wealth Change Summary**: The header displays aggregate metrics showing a total wealth change of $71.96bn, with $81.63bn gained and $9.66bn lost, providing an immediate snapshot of overall wealth movement in the Bloomberg Billionaires Index.

**Industry and Geographic Distribution**: A horizontal bar chart breaks down total net worth by industry and country, with Technology leading at $1.2T (primarily from the United States), followed by Consumer goods, Finance, and Industrial sectors. This visualization reveals concentration patterns in both industry sectors and geographical regions.

**Country-Level Analysis**: A treemap visualization presents the total net worth of the top 500 richest individuals grouped by country, with the United States ($13.23T), China ($0.58T and additional segments), France, India, and Hong Kong dominating the landscape. The size of each block corresponds to wealth concentration, making it easy to compare relative economic power.

**Daily Wealth Fluctuations**: Two detailed lists track Yesterday's Top 10 Wealth Losers (led by Low Tuck Kwong at -$0.40bn, followed by He Xiangjian at -$0.40bn and Shiv Nadar at -$0.39bn) and Gainers (led by Bernard Arnault at $1.14bn, Jeff Bezos at $4.50bn, and Elon Musk at $3.80bn), providing granular insights into daily market impacts on individual fortunes.

**Industry Performance Metrics**: The bottom section features multiple bar charts showing last change and year-to-date (YTD) changes by industry. Technology shows the strongest YTD performance at $231bn, while sectors like Food & Beverage show negative trends (-$0.28M), revealing which industries are creating or destroying wealth.

**Global Wealth Distribution Map**: An interactive world map visualizes the sum of last change by country/region, with color gradients (orange to brown tones) indicating wealth concentration and movement patterns across continents, powered by Esri mapping technology.

**Industry-Region Matrix**: A comprehensive treemap in the bottom right breaks down total net worth by the intersection of industry and country, revealing that Technology wealth is heavily concentrated in China and the United States, while Finance, Energy, and Real Estate show more diversified geographic distribution.

### Approach & Methodology

**Design Philosophy**:
- Utilized a dark theme for the header to create visual impact and focus attention
- Implemented a modular layout with distinct sections for different analytical perspectives
- Used color coding consistently (red for losses, green/black for gains) to facilitate quick interpretation
- Applied treemaps and choropleth maps for effective visualization of hierarchical and geographic data

**Data Modeling**:
- Created a snowflake schema linking billionaire profiles to industry classifications, geographic locations, and daily wealth changes
- Implemented complex DAX measures for wealth aggregation across multiple dimensions
- Built dynamic rank calculations to identify top gainers and losers
- Designed running total calculations for year-to-date performance tracking
- Created bridge tables for many-to-many relationships (billionaires with multiple business interests)

**Analytical Techniques**:
- Applied clustering analysis to group billionaires by wealth brackets (1-100, 101-200, 201-300 ranks)
- Utilized hierarchical aggregation for multi-level treemap visualizations
- Implemented real-time update mechanisms for daily wealth changes
- Created custom geocoding for accurate map visualizations
- Designed drill-through functionality from summary to individual billionaire details

**Interactive Features**:
- Rank group filtering (1-100, 101-200, 201-300, 301-400, 401-500)
- Country/Region and Industry slicers for cross-filtering all visualizations
- Tooltips displaying additional context on hover
- Cross-highlighting between related visualizations

### Data Sources

- **Bloomberg Billionaires Index**: Real-time wealth tracking data updated daily
- **Market Data Feeds**: Stock prices, currency exchange rates, and asset valuations
- **Corporate Filings**: SEC disclosures, annual reports, and ownership stakes
- **Geographic Mapping**: Esri ArcGIS for spatial data and country boundaries
- **Industry Classifications**: GICS (Global Industry Classification Standard) or custom taxonomy
- **Historical Data**: Time-series data for trend analysis and YTD calculations

*Note: This appears to be a demonstration dashboard using simulated or sample Bloomberg data structure*

### Key Insights

1. **Technology Dominance**: Technology sector holds over $1.2T in wealth, representing approximately 35-40% of total billionaire wealth, highlighting the transformative impact of digital economy and innovation on wealth creation.

2. **Geographic Concentration**: The United States dominates with $13.23T across multiple sectors, representing roughly 40-45% of global billionaire wealth, followed by China with significant holdings in Technology, Consumer, and Industrial sectors.

3. **Daily Volatility**: The presence of multiple billionaires with daily losses exceeding $200M demonstrates the extreme volatility of concentrated wealth positions, primarily driven by stock market fluctuations.

4. **Top Individual Performers**: Jeff Bezos ($4.50bn gain), Elon Musk ($3.80bn gain), and Bernard Arnault ($1.14bn gain) led daily gains, reflecting strong performance in e-commerce, electric vehicles, and luxury goods sectors respectively.

5. **Industry Divergence**: While Technology shows strong YTD gains ($231bn), traditional sectors like Food & Beverage are experiencing wealth destruction, indicating structural shifts in the global economy.

6. **Wealth Distribution Inequality**: The treemap visualization reveals extreme concentration, with the top 3 countries (US, China, France) holding the vast majority of billionaire wealth, underscoring global wealth inequality trends.

7. **Emerging Market Presence**: Countries like India, Hong Kong, Mexico, and Russia show growing presence in the billionaire index, indicating wealth creation in emerging economies, though still significantly behind developed markets.

8. **Sector-Geography Correlation**: The Industry-Region matrix reveals that certain industries cluster geographically (e.g., Technology in US/China, Energy in US/Russia), suggesting regional competitive advantages and ecosystem effects.

9. **Net Wealth Flow**: Despite individual losses, the overall positive net change ($71.96bn) indicates wealth creation is outpacing destruction, driven primarily by asset appreciation in equity markets.

10. **Diversified vs. Concentrated Wealth**: The diversified sector shows significant wealth across multiple countries, suggesting that billionaires with portfolio diversification strategies may achieve more stable wealth preservation.

---

## Technical Specifications

### Tools & Technologies
- **Power BI Desktop**: Primary development environment
- **DAX (Data Analysis Expressions)**: For calculated measures and columns
- **Power Query (M Language)**: For data transformation and ETL processes
- **Custom Visuals**: Esri Maps, advanced charts from AppSource
- **Power BI Service**: For dashboard publishing and sharing (if applicable)

### Performance Optimization
- Implemented incremental refresh for large datasets
- Created aggregation tables for improved query performance
- Optimized DAX formulas to reduce calculation time
- Used variables in DAX to avoid repeated calculations
- Established proper relationships with appropriate cardinality

### Best Practices Applied
- Followed star schema design principles for optimal performance
- Implemented row-level security for sensitive data (where applicable)
- Created comprehensive documentation for DAX measures
- Used consistent naming conventions across all objects
- Established data refresh schedules and error handling
- Designed mobile-responsive layouts for multi-device access

---

## Repository Information

This repository contains:
- GIF demonstrations of dashboard interactivity
- Sample data files (sanitized/anonymized)
- Documentation and technical specifications
- DAX measure library
- Design guidelines and color palettes used

### Future Enhancements
- Real-time data integration via APIs
- Advanced predictive analytics using Python/R integration
- Natural language Q&A functionality
- Automated report distribution via email subscriptions
- Integration with Microsoft Teams for collaborative analysis
