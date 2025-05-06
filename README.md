# 2025_ia651_chigome_kurira
# Analysis of Factors Influencing Laptop Prices In The Consumer Market.


## Project Overview
Through our analysis, we aim to identify the most significant factors determining laptop prices and quantify their influence.

## Dataset
The dataset for this project captures key hardware specifications and features that potentially impact the pricing of laptops in the consumer market. It was sourced from Kaggle, has 1,273 laptop models with 13 variables and they are as follows:

Company: Manufacturer of the laptop (Dell, HP, Apple)
TypeName: Model name/series of the laptop
Ram: Random Access Memory in GB
Weight: Weight of the laptop in kg
Price: Price of the laptop (target variable)
TouchScreen: Binary indicator (1 = has touch screen, 0 = no touch screen)
Ips: Binary indicator for IPS display technology (1 = has IPS, 0 = no IPS)
Ppi: Pixels per inch, measuring screen resolution density
Cpu_brand: Processor manufacturer (e.g., Intel, AMD)
HDD: Hard Disk Drive storage in GB
SSD: Solid State Drive storage in GB
Gpu_brand: Graphics processing unit manufacturer
Os: Operating system installed on the laptop

## Process Overview
The analysis of laptop price determinants began with extensive data preprocessing on our dataset of 1,273 laptop models. We first performed exploratory data analysis to understand variable distributions and relationships with price. This revealed initial patterns in how specifications like RAM, processor brands, and storage options correlate with pricing. We then cleaned the data by handling missing values, removing outliers, and encoding categorical variables like Company, CPU brand, and GPU brand to prepare for modeling.
The modeling phase employed multiple regression techniques(like Lasso, Ridge regression) to quantify the impact of each feature on laptop prices. We evaluated different models using cross-validation to ensure reliability and used feature importance metrics to identify the key drivers of price variation. The most influential factors were isolated and visualized to demonstrate their relative impact on pricing decisions in the consumer laptop market. These findings provide valuable insights for both manufacturers and consumers to understand the value proposition of different laptop specifications.

## Exploratory Data Analysis
Our exploratory data analysis revealed several interesting patterns in the laptop dataset of 1,273 models and 13 variables. Price is our (Y) target variable. We examined the distribution of prices and found significant variations across different manufacturers, with premium brands commanding higher price points regardless of specifications. Correlation analysis showed that RAM capacity, SSD storage size, and screen resolution (PPI) had the strongest positive correlations with price. Visual examinations through histograms and scatter plots identified several outliers in the premium segment, while box plots demonstrated how the presence of features like touchscreens and IPS displays consistently increased median prices across all categories. These initial findings guided our feature engineering process and helped us formulate hypotheses about the most influential price determinants.
![image](https://github.com/user-attachments/assets/f834587f-c857-4c77-a193-7f787af8f049)
![image](https://github.com/user-attachments/assets/e8fbdba7-13b8-47df-8f95-9a4d04f105b0)
![image](https://github.com/user-attachments/assets/0dff5f16-73ff-4a93-81b5-156175024239)




## Dataset






