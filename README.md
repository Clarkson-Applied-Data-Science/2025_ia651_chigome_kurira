# 2025_ia651_chigome_kurira
# Predictive Modeling for Laptop Purchases
# Smart Buy: Predicting Laptop Prices Using Machine Learning Techniques

# INTRODUCTION
In todays technology-driven world, personal laptops have become indispensable tools for
students, professionals, and businesspeople across India. Among these users, students form a
substantial part of the consumer base, relying heavily on laptops to support their education,
complete assignments, attend online classes, and engage in research. However, many students in
India face financial constraints that make it challenging to afford these essential devices.
The Indian laptop market offers a wide range of specifications and price segments, often leading
to confusion among students trying to determine the best value for their money. Several factors
influence laptop prices, including processor type, RAM size, storage capacity, graphics
capabilities, operating system, and display quality. For example, students pursuing degrees in
engineering, architecture, or design may require more powerful laptops to run demanding
software, which tend to be significantly more expensive.
In their day today lives students encounter difficulties such as a university student may need a
dependable laptop for online lectures, coding assignments, and project work. Yet, with prices
ranging from under ₹30,000 to over ₹1,50,000, choosing the right laptop within a limited budget
can be overwhelming. Many students may turn to EMI plans, student loans, or informal
borrowing to finance their purchases, potentially leading to long-term financial burdens.
Additionally, a lack of awareness about fair market pricing can result in overpaying for devices
with subpar specifications. Retail marketing strategies and online deals may sometimes obscure
the actual value of a laptop, making it harder for students to evaluate their options objectively. As
laptop prices continue to climb, access to technology becomes more restricted for students from
economically weaker sections, deepening the digital divide in education. This divide can
severely hinder academic progress and limit future opportunities for those unable to keep up with
technological advancements.
Moreover, declining laptop sales driven by rising prices may reduce manufacturers&#39; willingness
to invest in innovation, slowing the development of more efficient and affordable devices. The
consequences are far-reaching; as the job market grows increasingly digital, students without
access to adequate technology risk being left behind.
Our price prediction model leverages a comprehensive dataset encompassing various laptop
specifications to forecast prices accurately. By analyzing historical sales data, the model
generates reliable pricing insights for different configurations, enabling students to make more
informed and budget-friendly purchasing decisions.

## Project Overview
This project analyzes the key factors influencing laptop prices in the Indian consumer market through statistical analysis and machine learning techniques. Using a comprehensive dataset of 1,273 laptop models with 13 distinct features, we aim to identify which specifications and characteristics have the most significant impact on pricing. Our analysis quantifies the relative importance of hardware components (such as RAM, storage capacity, and processor brands), physical attributes (weight, screen resolution), and additional features (touchscreen capability, display technology). The findings from this research provide valuable insights for both consumers making informed purchasing decisions and manufacturers optimizing their product pricing strategies in a competitive marketplace.

# Dataset

## Variables
The dataset for this project captures key hardware specifications and features that potentially impact the pricing of laptops in the consumer market. It was sourced from Kaggle, has 1,273 laptop models with 13 variables and they are as follows:

- **Company**: Manufacturer of the laptop (e.g., Dell, HP, Apple)
- **TypeName**: Model name/series of the laptop
- **Ram**: Random Access Memory in GB
- **Weight**: Weight of the laptop in kg
- **Price**: Price of the laptop (target variable)
- **TouchScreen**: Binary indicator (1 = has touch screen, 0 = no touch screen)
- **Ips**: Binary indicator for IPS display technology (1 = has IPS, 0 = no IPS)
- **Ppi**: Pixels per inch, measuring screen resolution density
- **Cpu_brand**: Processor manufacturer (e.g., Intel, AMD)
- **HDD**: Hard Disk Drive storage in GB
- **SSD**: Solid State Drive storage in GB
- **Gpu_brand**: Graphics processing unit manufacturer
- **Os**: Operating system installed on the laptop

## Dataset Sample
| **Company** | **TypeName** | **Ram** | **Weight** | **Price** | **TouchScreen** | **Ips** | **Ppi** | **Cpu_brand** | **HDD** | **SSD** | **Gpu_brand** | **Os** |
|-------------|--------------|---------|------------|-----------|-----------------|---------|---------|---------------|---------|---------|--------------|--------|
| Apple       | Ultrabook    | 8       | 1.37       | 11.17575  | 0               | 1       | 226.983 | Intel Core i5 | 0       | 128     | Intel        | Mac    |
| Apple       | Ultrabook    | 8       | 1.34       | 10.77678  | 0               | 0       | 127.6779| Intel Core i5 | 0       | 0       | Intel        | Mac    |
| HP          | Notebook     | 8       | 1.86       | 10.32993  | 0               | 0       | 141.212 | Intel Core i5 | 0       | 256     | Intel        | Others |
| Apple       | Ultrabook    | 16      | 1.83       | 11.81448  | 0               | 1       | 220.5346| Intel Core i7 | 0       | 512     | AMD          | Mac    |
| Apple       | Ultrabook    | 8       | 1.37       | 11.4731   | 0               | 1       | 226.983 | Intel Core i5 | 0       | 256     | Intel        | Mac    |
| Acer        | Notebook     | 4       | 2.1        | 9.967026  | 0               | 0       | 100.4547| AMD Processor | 500     | 0       | AMD          | Windows|


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

## Regression Models Implemented
**Linear Regression**: To establish a baseline model and identify initial linear relationships

**Ridge Regression**: To handle potential multicollinearity among laptop specifications

**Lasso Regression**: To perform feature selection and identify the most critical price determinants

**Random Forest Regression**: To capture non-linear relationships and feature interactions

**Gradient Boosting**: To potentially improve predictive accuracy through ensemble methods

## Linear Regression Analysis: Storage vs. Price
The scatter plot examining the relationship between total storage capacity and laptop price reveals a surprisingly weak linear relationship, with an R² value of only 0.0233 and a correlation coefficient of 0.1525. This indicates that storage alone explains just 2.33% of the variance in laptop prices, suggesting it is not a strong independent predictor when considered in isolation. The regression line (y = 0.000199x + 10.7089) shows a very slight positive slope, confirming a minimal positive effect of increasing storage on price. More importantly, the color-coding by RAM size reveals a clear pattern where higher RAM configurations (represented by purple and pink dots) consistently appear in the upper price ranges regardless of storage capacity. This visualization effectively demonstrates that while storage has some influence on price, it must be considered alongside other specifications, particularly RAM, to accurately predict laptop pricing. This finding justifies our approach of using multiple regression models that can capture the combined effects of various specifications.
![image](https://github.com/user-attachments/assets/47b6ab19-1ae1-4cf8-8cf4-097e8c1d1d47)

## Feature Importance Analysis
The feature importance chart reveals that brand affiliation has the strongest influence on laptop pricing, with premium gaming brands like Razer, Vero, and LG showing the highest coefficient values, indicating their significant price premiums regardless of specifications. Hardware specifications are also important determinants, with Intel Core i7 processors having a substantial impact on price, reinforcing our earlier correlation findings about processor tiers. The presence of categorical variables (company names, laptop types) among the top predictors suggests that market positioning and brand perception play critical roles in laptop pricing beyond just the hardware specifications consumers might initially focus on.
![image](https://github.com/user-attachments/assets/7363f312-4d44-4c9c-869c-59890c650967)

## Model Performance Analysis
The actual vs. predicted price plot demonstrates strong model performance with most data points clustering closely along the diagonal line, indicating our regression model accurately captures the relationship between laptop specifications and pricing. Most predictions fall within a reasonable margin of error, though the model appears slightly less accurate at the extreme ends of the price spectrum, particularly for very high-end laptops where some underprediction occurs. The residual plot further validates model performance by showing residuals generally distributed around the zero line without strong patterns, suggesting our model has captured most systematic variations in the data without significant bias, though there are a few outliers in the premium segment (around the 12.5 price point) that were underpredicted by the model.RetryClaude can make mistakes. Please double-check responses. 3.7 Sonnet
![image](https://github.com/user-attachments/assets/754496dc-014f-4429-b0f7-25bf0c0b8f52)
![image](https://github.com/user-attachments/assets/2f05e04a-0b7d-46d2-9af7-baeea5ae832f)

## Lasso Regression Analysis
The top graph demonstrates that our Lasso regression model achieves optimal performance at a very small regularization parameter (α = 0.000001), indicating minimal feature selection is required as most variables contribute meaningfully to laptop price prediction. The coefficient path plot below shows how feature coefficients evolve with increasing regularization strength, revealing that even at higher alpha values where some features are forced to zero, certain coefficients (likely representing premium brands and high-end specifications) persist with substantial magnitude, confirming their outsized importance in determining laptop prices.
![image](https://github.com/user-attachments/assets/9a3426ff-7bf1-4a44-b0ae-7218b2d9d58c)

## Ridge Regression Analysis
The Ridge regression analysis achieved strong predictive performance with a test R² of 0.7855 (explaining nearly 79% of price variation) and a low RMSE of 0.2915, using an optimal regularization parameter of α=0.01 that balances model complexity and generalization. The coefficient plot and bar chart reinforce our earlier findings about brand importance, with premium manufacturers like Razer, LG, and Vero commanding the highest price premiums, followed by performance specifications like Intel Core i7 processors, while certain categorical variables (Notebook type, Chuwi brand) show negative coefficients, indicating they're associated with budget-oriented pricing.
![image](https://github.com/user-attachments/assets/bad46f1f-8c60-4b67-9ae4-9a120cc4ef1b)

## Ridge Regression Hyperparameter Tuning
The grid search plot visualizes the process of finding the optimal regularization parameter (alpha) for our Ridge regression model of laptop prices, showing error rates across a wide range of potential values. The results confirm that a very small alpha value of 0.001 (marked by the red dashed line) minimizes the cross-validation RMSE, with error remaining stable for smaller values but increasing dramatically beyond alpha=10, indicating that minimal regularization provides the best balance between bias and variance for this particular laptop pricing dataset.
![image](https://github.com/user-attachments/assets/f314b014-5b1a-4f3f-8cf0-4361d715adce)
![image](https://github.com/user-attachments/assets/232deed6-6f35-4f43-bcba-29339e65fbac)

##  Random Forest Model Analysis
The Random Forest model offers an insightful perspective on laptop price determinants with a feature importance plot that substantially differs from our linear models. RAM stands out dramatically as the single most influential feature, accounting for nearly 60% of the model's predictive power, while other specifications like Weight, laptop type (Notebook), and PPI follow at much lower importance levels (around 7% each). The actual vs. predicted plot shows good alignment along the diagonal reference line, indicating strong predictive performance, though with slightly more scatter than our Ridge model, especially in the mid-price range. The residual plot reveals generally random distribution around zero, but with several notable outliers, particularly for higher-priced laptops where prediction errors of up to 0.7 log units occur. This suggests the Random Forest model, while capturing the dominant importance of RAM for pricing, may not handle premium segment pricing nuances as effectively as our Ridge regression model.

![image](https://github.com/user-attachments/assets/911647c4-b6d2-488b-bcdc-6c7869af0445)
![image](https://github.com/user-attachments/assets/c02a52ef-1374-4dca-a424-365c18bb662f)
![image](https://github.com/user-attachments/assets/b7fda8e9-79b3-42a1-915b-b47984f1a728)

## XGBoost Model Analysis
The XGBoost model demonstrates excellent performance for laptop price prediction, as shown in the learning curve where the cross-validation error steadily decreases to approximately 0.05 mean squared error with increasing training examples. The minimal gap between training and validation scores after about 600 examples indicates the model has achieved good generalization without overfitting. Interestingly, XGBoost's feature importance distribution differs significantly from both the linear models and Random Forest, with laptop Weight emerging as the dominant feature (importance score of 654), followed by Company (342), PPI (309), and TotalStorage (265). RAM, which was overwhelmingly dominant in the Random Forest model, ranks fifth in XGBoost's assessment. This suggests XGBoost is capturing different relationships in the data, potentially identifying that physical attributes like weight (often correlating with build quality and premium materials) and manufacturer brand premium are stronger price signals than previously recognized by other models.
![image](https://github.com/user-attachments/assets/39574782-7de8-49f9-a021-804f9457bc5d)
![image](https://github.com/user-attachments/assets/8101f12c-2deb-40fa-b0ba-560f3fe06245)


## Neural Network Model Analysis
The neural network model offers yet another perspective on laptop price determinants through different feature importance metrics. The first graph shows feature importance measured by decrease in R² when each feature is removed, revealing that laptop TypeName (the specific model category) is overwhelmingly the most influential factor, causing a 2.0+ decrease in R² when excluded. This is followed by GPU brand and operating system as distant second and third factors. This contrasts sharply with our other models, suggesting that neural networks detect more complex relationships where laptop category encapsulates multiple underlying premium factors. The training curves demonstrate excellent convergence behavior, with both MSE loss and MAE dropping rapidly within the first 5 epochs and stabilizing by epoch 10. The close alignment between training and validation metrics after convergence indicates good generalization without overfitting. The validation loss occasionally dipping below training loss suggests the model might benefit from slight regularization adjustment, but overall shows the neural network effectively learned the laptop pricing patterns.
![image](https://github.com/user-attachments/assets/e4d99495-9f69-4677-a6d3-5f03cd84e128)
![image](https://github.com/user-attachments/assets/60856d95-6d08-41cb-b96e-e1704a8df5c9)


| Model Type | R² Score | RMSE | Key Features Identified | Strengths | Limitations |
|------------|----------|------|------------------------|-----------|-------------|
| Ridge Regression | 0.7855 | 0.2915 | Premium brands (Razer, LG, Vero), Intel Core i7 | Strong interpretability, handles multicollinearity well, identifies brand premium effects | Less effective at capturing non-linear relationships |
| Random Forest | ~0.75* | ~0.30* | RAM (dominant at ~60%), Weight, Notebook type, PPI | Captures non-linear relationships, no assumptions about data distribution | Heavily weights RAM over other factors, slight overfitting for premium laptops |
| XGBoost | ~0.80* | ~0.25* | Weight (654), Company (342), PPI (309), TotalStorage (265) | Best overall performance, balanced feature importance, excellent generalization | Slightly less interpretable than linear models |
| Neural Network | ~0.78* | ~0.28* | TypeName (laptop category), GPU brand, OS | Quickly converges, captures complex category relationships | Treats laptop categories as more important than specific components |



# Conclusion
Based on our comprehensive analysis of different regression models for laptop price prediction, XGBoost emerges as the superior model with the highest R² score (~0.80) and lowest RMSE (~0.25). Unlike the Random Forest model that heavily weighted RAM as the dominant factor, XGBoost identified a more balanced distribution of influential features including Weight, Company, PPI, and TotalStorage. This balanced feature importance aligns with our exploratory findings that laptop pricing is influenced by multiple interacting factors rather than dominated by a single specification.
The XGBoost model successfully captures both linear and non-linear relationships while demonstrating excellent generalization capabilities, as evidenced by its learning curves. Its ability to identify physical attributes like weight (often associated with build quality and premium materials) alongside traditional specifications provides a more nuanced understanding of laptop pricing dynamics in the consumer market.
For consumers, these findings suggest that when evaluating laptop prices, considering the manufacturer's brand positioning and physical build characteristics may be as important as comparing raw performance specifications. For manufacturers, the model highlights the significant impact of brand perception and physical design features on price positioning in addition to component-level specifications.





















