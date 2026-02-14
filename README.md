# OilyGiant Oil Company - Well Location Selection and Risk Assessment Project

### Problem Context:
Development of a comprehensive machine learning system to identify the most profitable oil drilling locations for OilyGiant company across three different regions, using geological survey data to predict oil reserves and assess financial risks associated with drilling investments.

### Objective:
Build predictive models to estimate oil reserves in potential drilling sites and perform risk assessment analysis to determine the optimal region for investment, considering a budget of $100 million for developing 200 oil wells with minimum acceptable risk threshold of 2.5%.

Technical Competencies Used:
Exploratory Data Analysis (EDA):
- Investigation of 3 regional datasets (geo_data_0, geo_data_1, geo_data_2) with 100,000 records each
- Analysis of geological features (f0, f1, f2) and oil production volumes
- Data quality assessment including duplicate detection and missing value analysis
- Statistical analysis of oil production distributions across regions

Data Preprocessing:
- Feature-target separation for supervised learning
- Train-validation split (75:25 ratio) with consistent random state
- Data type validation and structure optimization
- Handling of duplicate well IDs representing consecutive drilling operations

Machine Learning Model Development:
- Linear Regression: Primary predictive model for oil reserve estimation
- Model training on geological features (f0, f1, f2) to predict oil production volumes
- Cross-validation using separate validation sets for each region
- Model performance comparison against baseline (mean prediction)

Financial Analysis:
- Profit calculation incorporating oil price ($4,500 per unit) and drilling costs ($500,000 per well)
- Break-even analysis determining minimum production threshold (111.11 units per well)
- Revenue optimization through selection of top 200 most promising wells per region

Advanced Statistical Analysis - Bootstrapping:
- Bootstrap sampling: 1,000 iterations with 500-sample resampling
- Monte Carlo simulation: Risk assessment through repeated sampling with replacement
- Confidence interval calculation: 95% confidence intervals for profit estimation
- Risk quantification: Probability calculation of negative returns

Risk Assessment:
- Statistical hypothesis testing for investment decision-making
- Probability distribution analysis of potential profits and losses
- Comparative risk analysis across three geographical regions

### Main Libraries:
- pandas: Data manipulation, sampling, and statistical operations
- numpy: Mathematical operations and random state management
- scikit-learn: Machine learning algorithms and evaluation metrics
  - LinearRegression: Primary predictive algorithm
  - train_test_split: Data splitting functionality
  - mean_squared_error: Model evaluation metric
- matplotlib: Data visualization and plotting

### Final Results:
Comprehensive risk-based investment analysis with clear regional recommendations:

Model Performance:
- Region 1: RMSE = 37.58, Average predicted volume = 92.59 units
- Region 2: RMSE = 0.89, Average predicted volume = 68.73 units  
- Region 3: RMSE = 40.03, Average predicted volume = 94.97 units

Financial Analysis:
- Region 1: Average profit = $3.79M, Risk of loss = 9.0%
- Region 2: Average profit = $4.63M, Risk of loss = 1.3%
- Region 3: Average profit = $4.08M, Risk of loss = 7.4%

Strategic Recommendation:
- Region 2 selected as optimal investment location
- Lowest risk profile: 1.3% probability of loss (below 2.5% threshold)
- Highest average profit: $4.63M per investment cycle
- Superior model accuracy: Lowest RMSE indicating reliable predictions

Business Impact:
- Enables data-driven location selection for oil drilling operations
- Provides quantitative risk assessment for investment decisions
- Supports strategic planning with confidence intervals and probability distributions
- Facilitates optimal resource allocation across geographical regions
