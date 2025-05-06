# 2025_ia651_chigome_kurira
# Analysis of Factors Influencing Laptop Prices In The Consumer Market.


## Project Overview
This project analyzes the key factors influencing laptop prices in the Indian consumer market through statistical analysis and machine learning techniques. Using a comprehensive dataset of 1,273 laptop models with 13 distinct features, we aim to identify which specifications and characteristics have the most significant impact on pricing. Our analysis quantifies the relative importance of hardware components (such as RAM, storage capacity, and processor brands), physical attributes (weight, screen resolution), and additional features (touchscreen capability, display technology). The findings from this research provide valuable insights for both consumers making informed purchasing decisions and manufacturers optimizing their product pricing strategies in a competitive marketplace.

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
Our exploratory data analysis revealed several interesting patterns in the laptop dataset of 1,273 models and 13 variables. Price is our (Y) target variable. We examined the distribution of prices and found significant variations across different manufacturers, with premium brands commanding higher price points regardless of specifications. Correlation analysis showed that RAM capacity, SSD storage size, and screen resolution (PPI) had the strongest positive correlations with price. Visual examinations through histograms identified several outliers in the premium segment. These initial findings guided our feature engineering process and helped us formulate hypotheses about the most influential price determinants.
![image](https://github.com/user-attachments/assets/f834587f-c857-4c77-a193-7f787af8f049)
![image](https://github.com/user-attachments/assets/e8fbdba7-13b8-47df-8f95-9a4d04f105b0)
![image](https://github.com/user-attachments/assets/0dff5f16-73ff-4a93-81b5-156175024239)


## Correlation Analysis
The correlation matrix reveals RAM (0.68) and SSD storage (0.66) have the strongest positive correlations with laptop price, indicating these are likely primary drivers of cost in the consumer market. Interestingly, PPI (screen resolution density) shows a moderate positive correlation (0.48) with price, while traditional HDD storage shows a slight negative correlation (-0.10), reflecting the market's shift toward valuing higher resolution displays and faster storage technologies. Weight demonstrates minimal correlation with price (0.15), suggesting consumers prioritize performance specifications over physical attributes when evaluating laptop value.
![image](https://github.com/user-attachments/assets/bb66525a-ba4f-40a1-9e82-b261881c924e)


## Feature Relationship Analysis
The scatter plots reveal distinct patterns between laptop specifications and pricing. RAM shows a clear stepped relationship with price, where higher RAM values consistently correspond to higher price points, supporting its strong correlation coefficient. SSD storage similarly displays a positive trend with price, though with more variability within each storage tier. In contrast, Weight shows a weak positive relationship with price, contradicting expectations that lighter laptops command premium prices. The PPI (screen resolution) plot demonstrates clusters around specific resolution standards rather than a continuous relationship. HDD storage shows an interesting pattern where both zero and higher storage capacities appear in higher-priced models, suggesting traditional storage is not a primary price driver in modern laptops.
![image](https://github.com/user-attachments/assets/165bc22e-af82-41de-8444-d327d521af26)

## Brand and Component Analysis
The bar charts reveal distinct pricing patterns across laptop brands and components. Razer commands the highest average prices, followed closely by LG and MSI, while Xiaomi offers the most affordable options among major manufacturers. For processors, Intel Core i7 chips are associated with the highest average prices, with a clear price hierarchy descending through Core i5, Core i3, and AMD processors. Nvidia GPUs correlate with slightly higher average prices than either Intel or AMD graphics solutions, suggesting a premium for dedicated graphics performance. Operating system comparison shows Mac OS commands the highest average price point, followed by Windows, with other operating systems (likely Chrome OS and Linux) associated with more budget-friendly laptop options.
![image](https://github.com/user-attachments/assets/2a166d5b-8a95-44fe-aa3b-9dd692a53235)

## Feature Importance Analysis
The visualizations provide clear evidence of the most significant predictors of laptop prices in the consumer market. RAM shows the strongest positive linear relationship with price (visible in the clear upward trend line), confirming its role as a primary price determinant across all laptop categories. SSD storage similarly demonstrates a strong positive correlation (0.66), with increasing capacity consistently associated with higher price points. The box plots reveal substantial price variations by laptop type, with Workstations commanding the highest median prices, followed by Ultrabooks, while Netbooks occupy the budget segment. Processor brand exhibits a clear hierarchy, with Intel Core i7 associated with premium pricing. Among operating systems, Mac commands the highest price premium, while GPU analysis shows Nvidia graphics correlating with higher-priced models compared to Intel or AMD alternatives. These findings suggest that RAM, SSD capacity, laptop type, and processor tier are the most influential factors in determining laptop pricing.
![image](https://github.com/user-attachments/assets/c58173d6-6d1d-41f4-b412-65080cc41885)

![image](https://github.com/user-attachments/assets/74bd0742-172d-4499-95d7-af5defd06515)

![image](https://github.com/user-attachments/assets/38af314e-8a3b-4666-ad5b-6e809fb62ff4)

## Principal Component Analysis 
We conducted Principal Component Analysis for this laptop price analysis project to address the complexity and potential multicollinearity in our dataset. With 13 different variables potentially influencing laptop prices, many features likely have correlations with each other (such as RAM and storage capacities often increasing together in higher-end models). PCA transforms these potentially correlated features into a set of linearly uncorrelated variables called principal components, making the data structure more interpretable. This dimensionality reduction technique allowed us to identify the underlying patterns driving price variations without losing significant information. By compressing our dataset into fewer dimensions ( we combined HHD and SSD to create a new variable - Total_Storage), PCA also helped visualize complex relationships between features and laptop prices that would be difficult to observe in the original high-dimensional space.
![image](https://github.com/user-attachments/assets/f0918644-d113-4986-930e-ac282006738b)
![image](https://github.com/user-attachments/assets/f50c2415-2e8c-476b-a0f4-944107f7d114)

## Principal Component Correlation Analysis After PCA
The heatmap reveals the relationship between original features and principal components, providing insight into what each Principal Component represents in the laptop dataset. PC1 shows strong positive correlations with Weight (0.59) and TotalStorage (0.49), while having negative correlations with TouchScreen and PPI (both -0.42), suggesting this component primarily distinguishes between heavier laptops with more storage versus lighter laptops with premium displays. PC2 correlates substantially with RAM (0.60), PPI (0.47), and IPS display (0.42), indicating it captures high-performance premium specifications. PC3 has a remarkably strong correlation with IPS display technology (0.84), suggesting this component specifically isolates display quality from other features. PC4 shows interesting contrasts, with a strong positive correlation to TouchScreen (0.60) but negative correlation to RAM (-0.50), potentially identifying budget touchscreen devices with lower performance specifications. This analysis confirms the PCA has effectively separated distinct aspects of laptop characteristics into interpretable components.
![image](https://github.com/user-attachments/assets/acefe3a2-ffc4-41f3-bfac-e1b099043354)

# Regression Analysis Approach
For our laptop price prediction project, we implemented multiple regression techniques to evaluate which models best capture the complex relationships between laptop specifications and price. We started with linear regression as a baseline, then progressed to more sophisticated models like Ridge, Lasso, and Random Forest regression. This multi-model approach is essential because laptop pricing likely involves both linear and non-linear relationships between features. Some specifications may have straightforward linear effects on price (like RAM or storage capacity), while others might interact in complex ways or have diminishing returns (like the relationship between premium components and ultra-high-end pricing). By comparing different regression models, we can identify which approach best captures these market dynamics and provides the most accurate and interpretable predictions of laptop pricing factors.

# Regression Models to Implement
Linear Regression: To establish a baseline model and identify initial linear relationships

Ridge Regression: To handle potential multicollinearity among laptop specifications

Lasso Regression: To perform feature selection and identify the most critical price determinants

Random Forest Regression: To capture non-linear relationships and feature interactions

Gradient Boosting: To potentially improve predictive accuracy through ensemble methods













