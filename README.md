# Airbnb Data Analysis

A comprehensive data analysis project exploring Airbnb listing data to uncover insights about pricing, room types, and neighborhood distributions.

## 📋 Overview

This project analyzes Airbnb Open Data to understand patterns in listing prices, room type distributions, and geographic patterns across different neighborhoods. The analysis includes data cleaning, exploratory data analysis, and data visualization.

## 📊 Dataset

The project uses the **Airbnb Open Data** dataset (`Airbnb_Open_Data.csv`), which contains:
- **102,599 listings** (before cleaning)
- **26 columns** including:
  - Listing information (ID, name, host details)
  - Location data (neighborhood, coordinates, country)
  - Pricing information (price, service fee)
  - Room details (room type, construction year)
  - Review metrics (number of reviews, review rate, last review date)
  - Availability and booking information

## 🛠️ Requirements

The analysis is performed using Python with the following libraries:

- `pandas` - Data manipulation and analysis
- `numpy` - Numerical computing
- `matplotlib` - Data visualization
- `seaborn` - Statistical data visualization

## 📁 Project Structure

```
Airbnb_DataAnalysis/
├── Airbnb_Open_Data.csv      # Dataset file
├── Data_analysis.ipynb       # Jupyter notebook with analysis
├── README.md                 # Project documentation
└── Airbnb Data Analysis Project Report.pdf                 # Project report
```

## 🔍 Analysis Steps

### 1. Data Loading
- Load the CSV dataset into a pandas DataFrame
- Handle data type warnings for mixed-type columns

### 2. Data Cleaning
- **Missing Values**: Handle missing data in various columns
- **Date Conversion**: Convert 'last review' to datetime format
- **Price Cleaning**: Remove currency symbols and convert price/service fee to numeric
- **Data Removal**: Drop columns with insufficient data (license, house_rules)
- **Deduplication**: Remove duplicate entries
- **Final Dataset**: ~101,410 listings after cleaning

### 3. Exploratory Data Analysis

#### Price Distribution
- Histogram visualization showing the distribution of listing prices
- KDE (Kernel Density Estimation) overlay for smooth distribution visualization

#### Room Type Analysis
- Count plot showing distribution across room types:
  - Entire home/apt
  - Private room
  - Shared room
  - Hotel room

#### Neighborhood Distribution
- Analysis of listings across neighborhood groups (Manhattan, Brooklyn, Queens, Bronx, Staten Island)
- Standardization of neighborhood group names (e.g., "brookln" → "Brooklyn")

#### Price vs. Room Type
- Box plot visualization comparing price ranges across different room types
- Identifies pricing patterns and outliers

## 📈 Key Findings

1. **Price Distribution**: The dataset shows a fairly even distribution of listing prices across different price ranges, indicating a wide variety of accommodation prices.

2. **Room Type Popularity**: 
   - Entire home/apt and Private room listings dominate the dataset
   - Shared room and Hotel room are less common

3. **Geographic Distribution**:
   - Manhattan and Brooklyn have the highest number of listings
   - Queens, Bronx, and Staten Island have fewer listings

4. **Pricing Patterns**:
   - Shared rooms tend to have lower prices
   - Private rooms, Entire home/apt, and Hotel rooms show higher and more varied price ranges

## 🚀 How to Run

1. **Install Dependencies**
   ```bash
   pip install pandas numpy matplotlib seaborn jupyter
   ```

2. **Launch Jupyter Notebook**
   ```bash
   jupyter notebook
   ```

3. **Open the Notebook**
   - Open `Data_analysis.ipynb`
   - Ensure `Airbnb_Open_Data.csv` is in the same directory

4. **Run All Cells**
   - Execute all cells sequentially to reproduce the analysis

## 📝 Notes

- The dataset contains some missing values which are handled during the cleaning process
- Some columns have mixed data types that require careful type conversion
- Geographic coordinates are available for mapping visualizations (not implemented in current analysis)

## 🔮 Future Enhancements

- Geographic mapping of listings using coordinates
- Time series analysis of reviews and availability
- Advanced statistical analysis and predictive modeling
- Correlation analysis between different features
- Host performance analysis

