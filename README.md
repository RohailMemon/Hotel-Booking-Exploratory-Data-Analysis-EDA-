**Hotel Booking Data - Exploratory Data Analysis (EDA)**

This project performs an Exploratory Data Analysis (EDA) on a hotel booking dataset, showcasing data cleaning, outlier detection, feature engineering, and visualization. The dataset contains hotel booking details such as lead time, length of stay, and average daily rate (ADR), and this analysis helps uncover booking trends, revenue performance, and customer behavior.

The goal is to demonstrate professional EDA skills, ensure data integrity, handle extreme values, and provide actionable insights.

**1. Data Collection & Understanding**
1. Loaded the dataset using Pandas.
2. Explored data types, dataset shape, and first few rows.
3. Identified missing values, duplicates, and extreme values.

**2. Data Cleaning & Preprocessing**
1. Handled Missing Values:
2. Filled missing values in children, country, agent, and company.
3. Removed Duplicates: Ensured uniqueness in booking records.
4. Converted Data Types.
5. Transformed reservation_status_date into a datetime format.

**3. Outlier Detection & Capping**
To ensure reliable analysis, extreme values were **identified and capped**:

| Feature                     | Issue Identified                       | Solution Applied     |
|-----------------------------|---------------------------------------|----------------------|
| **`adr`**                   | Unusual pricing spikes (up to $5400)  | **Capped at $500**   |
| **`lead_time`**             | Some bookings made >737 days in advance | **Capped at 365 days** |
| **`stays_in_weekend_nights`** | Extreme values (up to 19 nights)      | **Capped at 14 nights** |
| **`stays_in_week_nights`**  | Extreme values (up to 50 nights)      | **Capped at 14 nights** |
| **`total_nights`**          | Unusually long stays (up to 69 nights) | **Capped at 14 nights** |

**4. Exploratory Data Analysis (EDA)**
1. Analyzed Data Distribution:
2. Plotted histograms for lead_time, adr, stays_in_weekend_nights, stays_in_week_nights, and total_nights.
3. Checked for skewness and distribution patterns.
4. Visualized Outliers.
5. Used boxplots to confirm the presence of extreme values before capping.
6. Compared distributions before and after capping.

**Key Business Insights**
1. Lead time varies significantly, with most bookings made within 0-365 days before check-in.
2. ADR is mostly within $50-$200, but extreme outliers (above $500) were removed to avoid revenue misinterpretation.
3. Most stays are short-term, with 99% of guests staying 1-14 nights.

**Tech Stack**

| **Category**            | **Technology Used**  |
|-------------------------|---------------------|
| **Programming Language** | Python  |
| **Data Processing**      | Pandas, NumPy |
| **Visualization**        | Matplotlib |
| **Development Tools**    | Jupyter Notebook, GitHub |

**Conclusion**  

Our Exploratory Data Analysis (EDA) on the **Hotel Booking dataset** has enhanced data integrity by addressing missing values, removing duplicates, and capping extreme outliers. The analysis revealed that most bookings occur within **365 days**, with extreme lead times adjusted to maintain data reliability. Average Daily Rate (ADR) fluctuations were controlled by capping values at **$500**, ensuring accurate revenue insights. Additionally, stay durations were refined by capping total nights at **14**, aligning with realistic booking behaviors. These preprocessing steps have improved data quality, making the dataset well-structured for **business analytics, revenue forecasting, and cancellation pattern analysis**.

