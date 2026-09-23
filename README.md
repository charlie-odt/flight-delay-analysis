# Statistical Analysis on Flight Delays

This project involves analyzing commercial flight tracking data to understand and quantify the impact of external factors (weather conditions and maintenance operations) on departure and arrival punctuality. 

The goal is to extract relevant data from multiple relational databases and build a statistical model to evaluate the risk of flight delays.

**Note:** Original data has been modified for this public repository. Table structure and code remain identical.

## Tools
* **Language :** Python 3
* **Data Manipulation :** NumPy, Pandas
* **Statistics & Machine Learning :** Scikit-Learn, SciPy
* **Data Visualization :** Matplotlib, Seaborn

## Key Steps of the Analysis

### 1. Setting Up Dataset & Feature Engineering
* Loaded multiple relational data sources (`flights`, `weather`, `maintenance`, `scope`).
* Handled temporal anomalies using `datetime64` type coercion.
* Created new variables, calculating exact time deltas to isolate departure and arrival delays.
* Encoded flight statuses (on-time, delayed, canceled) for better handling ofthe data by the model.

### 2. Data Merging & Integration
* Performed SQL-like inner merges between flight schedules and weather records at the exact scheduled departure time for each airport.
* Cross-referenced flight data with aircraft maintenance logs to investigate correlations related to recent technical operations.

### 3. Exploratory Data Analysis & Statistical Testing
* Visualized distributions using Kernel Density Estimation (KDE) for wind speed and visibility, comparing on-time versus delayed flights.
* Conducted hypothesis testing (Student's t-test via `scipy.stats`) to statistically validate or reject the impact of external factors on delay times.

### 4. Predictive Modeling
* Designed a classification pipeline using a Logistic Regression model.
* Trained the model to predict the probability of a flight delay based on weather conditions (clear, hazy, rain, storm).
* Evaluated model coefficients (odds ratios) to interpret the predictive weight of each weather variable.

## How to Run the Project

1. Clone this repository :
   ```bash
   git clone [https://github.com/charlie-odt/flight-delay-analysis.git](https://github.com/charlie-odt/flight-delay-analysis.git)
   ```
   
