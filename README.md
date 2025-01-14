# Uber Data Analysis and Visualization

This repository showcases an in-depth analysis and visualization of Uber pickup data for New York City (January to June 2015). The analysis is aimed at understanding patterns in Uber ride data, including pickup trends across months, days, and hours, as well as identifying locations with the highest demand.

## Libraries Used
- **Pandas**: For data manipulation and analysis.
- **NumPy**: For numerical operations and handling missing values.
- **Seaborn & Matplotlib**: For basic visualizations like bar charts and line plots.
- **Plotly**: For interactive charts and visualizations.
- **Folium**: For geographical visualizations, including heatmaps.

### Data Collection and Cleaning
1. **Data Extraction**:
   - Data was extracted from multiple sources, including "uber-raw-data-janjune-15.csv", which contains Uber ride data from January to June 2015 (approximately 15 million data points). To make the analysis feasible, a sample dataset was created from the original, reducing the data size to 1 million points.
   
2. **Data Cleaning**:
   - Checked for and handled **missing values** and **duplicate rows**.
   - Verified and amended **data types** for accurate analysis, ensuring proper formats for datetime, numerical, and categorical columns.

### Key Analyses

1. **Monthly Uber Pickup Analysis**:
   - Extracted the **month** from the `Pickup_date` column and converted it to month names.
   - Created a bar chart showing which months had the highest number of Uber pickups.
   - Additional derived features like **weekday**, **day**, **hour**, and **minute** were also extracted from the `Pickup_date`.

2. **Hourly Rush Analysis**:
   - Used **`groupby(['weekday', 'hour'])`** to create a pivot table.
   - Visualized rush hour patterns for each day of the week using multi-line plots.

3. **Active Vehicles by Base Number**:
   - Analyzed which **base number** had the most active vehicles by processing data from `Uber-Jan-Feb-FOIL.csv`.
   - Created a box plot to show the range of active vehicles per base number and used **Plotly**'s `px.violin` to visualize the data distribution.

4. **Location-Based Rush Analysis**:
   - Used **Latitude** and **Longitude** from the dataset to identify locations with the highest rush.
   - Created an interactive **heatmap** with **Folium** to visualize Uber rush locations across New York City.
   - The heatmap was added to a world map, providing geographical context.

5. **Hour and Weekday Analysis**:
   - Converted the `Date/Time` column to a datetime object, then extracted **hour** and **weekday** information.
   - Created a pivot table and used `.style.background_gradient()` to visually highlight rush patterns across different hours and days of the week.

### Automation of Analysis
To streamline the process and allow for repeated use with different datasets, the analysis was automated by defining functions to:
   - Apply the same transformations and analysis steps to different datasets.
   - Generate pivot tables and apply visualizations in an automated fashion, reducing manual coding effort.

### Visualizations
- **Bar charts**: For displaying trends over time (e.g., Uber pickups per month).
- **Line plots**: For visualizing hourly rush patterns.
- **Box plots and violin plots**: For analyzing the distribution of active vehicles across bases.
- **Heatmaps**: For identifying geographical locations of high Uber demand.
- **Pairwise analysis**: For examining the relationship between different time features like **hour** and **weekday**.

### Technologies Used
- **Python** (Pandas, NumPy, Seaborn, Matplotlib, Plotly, Folium)
- **Plotly**: Used for interactive charts and graphs.
- **Folium**: For creating heatmaps and geographical visualizations.

### Project Flow:
1. **Data Collection**: Extracted and cleaned data from CSV files.
2. **Data Cleaning**: Handled missing and duplicate data, ensured proper data types.
3. **Exploratory Data Analysis (EDA)**: Analyzed trends and patterns in Uber rides, focusing on month, day, hour, and location.
4. **Data Visualization**: Created interactive visualizations using **Plotly** and **Folium**.
5. **Automation**: Streamlined the process with reusable functions for easy analysis.

This repository provides insights into Uber usage patterns and can serve as a foundation for further analysis or more advanced machine learning models.

---

Feel free to explore the code, run the analysis on different datasets, and adapt the visualizations as needed for your own projects!

