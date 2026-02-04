# Exploratory Data Analysis on the Automobiles Dataset

## Project Overview
This project performs an **Exploratory Data Analysis (EDA)** on a dataset of automobiles. The dataset consists of **193 observations and 24 variables** after cleaning. Each observation provides information about a specific automobile, including price, engine characteristics, fuel efficiency, body style, and manufacturer.

The main objectives of this EDA are to:  
- Understand the structure and quality of the dataset  
- Identify relationships between variables  
- Explore factors that influence car prices  
- Provide insights into fuel efficiency, engine size, horsepower, and manufacturer trends  

This analysis is performed using **Python** with libraries including `pandas`, `numpy`, `seaborn`, `matplotlib`, and `missingno`.

---

## Project Files
This project includes the following files:

- `Automobiles_EDA.ipynb` – Jupyter Notebook containing the full analysis with code, visualizations, and explanations.  
- `Automobiles_EDA_Report.pdf` – PDF version of the EDA report, summarizing the findings and insights.  
- `automobile.csv` – Dataset used for the analysis.


## Dataset
The dataset (`automobile.txt`) contains the following key features:  

- `make` – Manufacturer of the car  
- `body-style` – Car body style (e.g., sedan, hatchback)  
- `engine-size` – Size of the engine  
- `horsepower` – Engine power  
- `city-mpg` and `highway-mpg` – Fuel efficiency in city and highway conditions  
- `price` – Price of the car  
- Other engine, fuel, and dimensional attributes  

**Shape of the dataset after cleaning:** `(193, 24)`  

---

## Data Cleaning
1. Removed unnecessary columns: `symboling` and `normalized-losses`.  
2. Checked for duplicate rows; none were found.  
3. Converted missing values represented as `'?'` to `NaN` and dropped rows with missing values.  
4. Corrected data types for numeric columns:  
   - `bore` and `stroke` → `float64`  
   - `horsepower`, `peak-rpm`, and `price` → `int64`  
5. Corrected spelling errors in the `make` column:  
   - `'Alfa-Romero'` → `'Alfa-Romeo'`  
   - `'Peugot'` → `'Peugeot'`  
6. Identified 21 unique car manufacturers: Alfa-Romeo, Audi, BMW, Chevrolet, Dodge, Honda, Isuzu, Jaguar, Mazda, Mercedes-Benz, Mercury, Mitsubishi, Nissan, Peugeot, Plymouth, Porsche, Saab, Subaru, Toyota, Volkswagen, Volvo.  

**Missing data after cleaning:**  
- `num-of-doors` – 2 missing values  
- `bore` – 4 missing values  
- `stroke` – 4 missing values  
- `horsepower` – 2 missing values  
- `peak-rpm` – 2 missing values  
- `price` – 4 missing values  

After handling missing data, the dataset contains **193 complete observations**.  

---

## Key Questions Explored
1. **Which are the most expensive cars?**  
2. **How do the most expensive and cheapest cars compare?**  
3. **Which manufacturer builds the most fuel-efficient vehicles?**  
4. **Which vehicles have the largest engine capacity?**  
5. **Which manufacturer has the most car models in the dataset?**  

---

## Analysis & Insights

### Price Distribution
- The boxplot of prices shows a **right-skewed distribution**, with most cars priced in the low-to-mid range.  
- **Luxury brands** (Mercedes-Benz, Porsche, BMW, Jaguar) are the most expensive.  
- **Affordable brands** (Subaru, Chevrolet, Mazda, Toyota, Mitsubishi) have lower prices and higher fuel efficiency.  

### Engine Size and Horsepower
- Engine size is **positively correlated** with price (0.89) and horsepower (0.85).  
- Horsepower is also **positively correlated** with price (0.81).  
- High-end cars have larger engines and higher horsepower, while budget cars have smaller engines and lower horsepower.  

### Fuel Efficiency
- City and highway mpg are strongly correlated (0.97).  
- Fuel efficiency is **inversely related** to engine size and horsepower:  
  - Engine-size vs city-mpg: -0.72  
  - Engine-size vs highway-mpg: -0.74  
  - Horsepower vs city-mpg: -0.83  
  - Horsepower vs highway-mpg: -0.81  

### Curb Weight and Vehicle Dimensions
- **Curb-weight** strongly correlates with price (0.84).  
- Width (0.75) and length (0.70) also positively correlate with price.  
- Larger, heavier cars are generally more expensive and associated with high-end brands.  

### Manufacturer Analysis
- Most fuel-efficient manufacturer: **Chevrolet** (highest average mpg).  
- Largest engine capacity: **Jaguar** and other luxury brands.  
- Most models in the dataset: **Toyota** (wide range of car models).  

---

## Visualizations
The EDA includes the following visualizations:  
- **Bar plots:** Car counts by body style, average mpg by manufacturer, engine size by make, horsepower by make, curb weight by make.  
- **Boxplots:** Price distribution, engine size spread, horsepower spread, curb weight spread.  
- **Scatter plots:** Engine size vs horsepower with bubble size representing price.  
- **Heatmaps:** Correlation matrices for engine/fuel features and dimensions/layout features.  

---

## Key Conclusions
- **Luxury vs Budget:** High-end cars prioritize **performance and exclusivity**, while budget cars focus on **fuel efficiency and affordability**.  
- **Price Drivers:** Engine size, horsepower, and curb weight are the strongest factors influencing price.  
- **Consumer Choice:** Larger, heavier cars may be perceived as higher quality, while smaller cars appeal to cost-conscious and fuel-efficient buyers.  
- There is no universally “superior” car—choice depends on **desired features and price point**.  

---

## Tools & Libraries
- Python
- pandas, numpy – Data manipulation  
- seaborn, matplotlib – Visualization  
- missingno – Missing value analysis  

---

## How to Run
1. Clone the repository and ensure `automobile.txt` is in the working directory.  
2. Install dependencies:pip install pandas numpy seaborn matplotlib missingno

