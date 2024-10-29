# Dynamic Pricing Model to Adjust Price based on Demand, Competitor Prices and Inventory Levels in E-commerce Emporium Applications.
This project was aimed at developing a Dynamic Pricing Model capable of adjusting prices in real-time for E-commerce applications. The model was designed to respond to changes in demand, competitor pricing, and inventory levels. Throughout the project, I utilized advanced data science techniques to understand data-driven pricing strategies and build predictive models. 
## Business Overview/Problem.
E-Commerce Emporium faces several critical challenges in the highly competitive e-commerce landscape:
1. **Price Competition:** E-Commerce Emporium competes with numerous other online retailers offering similar products. To attract and retain customers, they often engage in price wars, which can lead to reduced profit margins.
2.  **Inventory Management:** Managing inventory efficiently is crucial for this business. Overstocking results in increased holding costs, while understocking can lead to lost sales and dissatisfied customers.
3.   **Demand Fluctuations:** Customer demand for products can vary greatly, often due to external factors such as seasons, holidays, or market trends. The company needs to adapt to these fluctuations in real-time to maximize sales and revenue.
4.    **Competitor Pricing:** Monitoring and responding to competitor pricing changes is essential to stay competitive while maintaining profitability.
5. **Data Complexity:** E-Commerce Emporium deals with vast amounts of data, including customer behavior, product sales, competitor pricing, and inventory levels. Analyzing this data manually is time-consuming and error-prone.

## Rationale for the Project.
1. **Market Dynamics:** The e-commerce industry is highly dynamic, with prices and demand constantly changing. Implementing a dynamic pricing strategy will allow E-Commerce Emporium to respond quickly to market fluctuations, giving them a competitive edge.
2. **Profit Maximization:** By adjusting prices based on demand, inventory levels, and competitor pricing, the company can optimize profit margins, ensuring that prices are neither too high to deter customers nor too low to erode profits.
3. **Customer Experience:** Providing competitive prices and product availability improves the overall shopping experience for customers, fostering loyalty and repeat business.
4. **Real-time Decision Making:** Dynamic pricing allows for real-time decision-making, enabling the company to adapt quickly to changing market conditions.

## Aim of the Project.
The primary objectives of this project are as follows:
1. **Implement a Dynamic Pricing Model:** Develop a dynamic pricing model that considers demand, competitor prices, and inventory levels to adjust prices automatically.
2. **Optimize Profit Margins:** Ensure that the dynamic pricing strategy maximizes profit margins while remaining competitive in the market.
3. **Improve Inventory Management:** Reduce holding costs by optimizing inventory levels based on demand forecasts.
4. **Enhance Customer Experience:** Provide customers with competitive prices and product availability, resulting in increased customer satisfaction and loyalty.
5. **Monitor Competitor Pricing:** Continuously monitor competitor pricing and adjust prices accordingly to remain competitive.
## Project Scope. 
- **Data Preprocessing:** Clean and transform the data to make it more suitable for modelling.
- **Exploratory Data Analysis:** Perform EDA to gain insights into data patterns, correlations & anomalies.
- **Model Evaluation:** Assess model performance using multiple metrics.
- **Model Development:** Build predictive models using different ML techniques.
- **Feature Engineering:** Create relevant feature.
## Tech Stack Used.
Python was be used alongside the libraries below:
- Pandas,NumPy,Matplotlib,Seaborn,Statsmodels,Scipy,Sklearn.
## Key Skills Utilised.
- Python
- Data Preprocessing
- Feature Engineering
- Model Building
- Model Evaluation
- Demand Forecasting
- Price Optimization
# Steps I used To Complete the project.
# 1. Importing Libraries
Here, I import all of the Python Libraries I will be needing for this entire project.
<img width="693" alt="Packages Imported" src="https://github.com/user-attachments/assets/cf3a8871-f18c-4581-be4c-b3896f6d16e9">


# 2. Understanding the Dataset
In this section, the aim is to look at the dataset and get a very brief overview of the features of the dataset. Here, I will:
- Load the dataset into the Python environment,
- View the dataset,
- Get a good description/understanding of what the features in the dataset are,
- See a brief statistic of the features of the dataset.
Let's begin by loading the dataset, saved as `Dataset.csv` into the Python environment.

Now, that we have brought the dataset into Python, we can now view the dataset to see the first few rows of the data.
<img width="821" alt="Viewing Dataset" src="https://github.com/user-attachments/assets/c97c0c49-0ec9-4ce1-b999-9430df9f4029">

The next step here, is to now see a brief statistic of the numerical variables of the dataset. We aim to see the minimum, maximum, mean, and other statistical values for the numerical columns of the dataset.
<img width="836" alt="Viewing Statistical characteristic of Dataset" src="https://github.com/user-attachments/assets/caa56265-d981-471b-80c6-3833a2224809">
As seen from `count`, we have **109,768** rows in the dataset.
# 3. Data Preprocessing

With data processing, I aim to fix any underlying issues with our dataset. These issues include:
- **Missing values**: 
- **Duplicate values**:
  
I will check for these, and fix them if they are present in the dataset.
Let's begin by checking each of the columns for missing values.

<img width="593" alt="Checking for missing Values" src="https://github.com/user-attachments/assets/3fa023a6-e56f-403d-a736-4f48fb389df0">

As seen from the result above, there are no missing values in the dataset, because the returned results were all `False`.

I will then move on to check for duplicate rows in the dataset. Specifically, I am going to check if any row of the dataset appears twice or more.

<img width="718" alt="Checking for duplicates" src="https://github.com/user-attachments/assets/38c52bfe-e210-485e-989e-ea29a2844939">

The `False` result given above, indicates that no row is duplicated in the dataset.
## 4. Exploratory Data Analysis.
Here, I aim to properly look at the dataset to idetify the distribution, frequency, and range of paramters in the features of the dataset.I will plot visuals, and properly understand what is in the dataset.I will also look at the relationships between some of the different paramters in the dataset. This analysis will be done in steps, with:
- **Univariate Analysis**: Looking at individual parameters one at a time.
- **Bivariate Analysis**: Looking at pairs of variables together.
- **Profit Margin Analysis**: Understanding the profit margin per product category.
- **Temporal Analysis**: Looking at how some of the variables change with time.

### 4.1. Univariate Analysis

As desribed before, we will look at the individual features of the dataset one after the other, individually in order to understand what they contain. We will be performing this univariate analysis in two steps:
- Univariate Analysis of Numerical Variables,
- Univariate Analysis of Categorical Variables.
#### 4.1.1. Univariate Analysis: Numerical Variables

I will be analysing the numerical variables here.

<img width="881" alt="Univariate Analysis _Numerical Variables" src="https://github.com/user-attachments/assets/02318cca-c2c0-4a0c-b0c1-afdfb5c185ed">

From the univariate distribution seen above, a few things can be noted:
- **Distribution of** `Demand`: For most of the sales made, the demand was usually lower. More customers demanded smaller quantities of the products, mostly in the range of 300 to 800. Only very few demands were as high as 1000.
- **Distribution of** `Inventory_Levels`: For most products, the inventory level was usually between 500 and 1,500. There were very few times where the inventory level for a particular product was as high as 2,500.
- **Distribution of** `Cost_Prices`: The cost price of most of the products are in th range of 0 to 2,500.
- **Distribution of** `Selling_Prices`: The selling prices of the products were usually within the range of 0 to around 2,400, almost as if it is spread evenly within this range.
- **Distribution of** `Competitor_Prices`: The Competitor prices for the products seem to have an even distribution all across. With the prices ranging from 0 to 3,000.
- **Distribution of** `Product_Ratings`: The product ratings for the products mostly fell within 3.0 and 4.0. A few of the other ratings were on 2.0 and 5.0. Ratings of 1.0 were the lowest.
- **Distribution of** `Days_Since_Product_Listing`: There is an even distribution for this paramters. The days since product listing for the products, fell between 0 days and around 350 days.
- **Distribution of** `Product_Age`: A lot of products had their ages around 4, 8 and 11. While a bulk of other products had their  product age around 0, 2, 5, 6, 9 and 12.
- **Distribution of** `Website_Traffic`: Website traffic fell within 8,050 and 8,400.
- **Distribution of** `Conversion_Rates`: The conversion rate of customers fell within 10.05% and 10.35%.
- **Distribution of** `Number_Of_Reviews`: The number of reviews given for each product as at the time of purchase was within the range of 0 to 100.
- **Distribution of** `Lead_Times`: The lead times in days, was concentrated around 0 to 10.

#### 4.1.2. Univariate Analysis: Categorical Variables

This next step from here, is to now look at the categorical variables, and try to understand them and how the parameters within them are distributed. This will help us understand how these parameters affect sales frequency.

<img width="862" alt="Univariate Analysis_categorical variables4" src="https://github.com/user-attachments/assets/5faff53c-36f1-4bec-96ec-4a85beb62913">
<img width="860" alt="Univariate Analysis_categorical variables3" src="https://github.com/user-attachments/assets/d21f2585-09ae-489a-812f-a0158b59835d">
<img width="863" alt="Univariate Analysis_categorical variables2" src="https://github.com/user-attachments/assets/5f8a88bb-cc5e-48bb-9ec6-afbc7a5e565e">
<img width="838" alt="Univariate Analysis-categorical Values" src="https://github.com/user-attachments/assets/6ea66055-e5b1-48c7-b23f-c18e97ecf6b6">

- **Distribution of** `Product_Categories`: The most frequently sold products, were in the the `Electronics` and - **Distribution of** `Clothing` category.
- **Distribution of** `Product_Conditions`: `New` products were the most frequently sold, while `Used` products followed. `Refurbished` products had the least frequency.
- **Distribution of** `Customer_Locations`: Customers in the `USA` made the most frequent purchases, than customers in the `UK` or `Canada`.
- **Distribution of** `Customer_Genders`: Gender did not seem to have any correlation with sales frequency.
- **Distribution of** `Competitor_Strategies`: The competitor stratagies at the current time was mostly `Discounts`. `Price Matching` and `Bundle Offers` were the least frequently used strategy by the competitor.
- **Distribution of** `Marketing_Campaigns`: This was mostly done with `Social Media Ads`. `TV Ads` and `Email Campaign` were the least.
- **Distribution of** `Supplier_Terms`: The supplier terms for supplying the goods mostly fell within `Net 30`.
- **Distribution of** `New_Product_Releases`: Most of the products that were sold didn't have any new releases.

### 4.2. Bivariate Analysis

As desribed before, we will look at pairs of features of the dataset. The main goal here is to identify relationships between multiple pairs of variables, and see if there are relationships between them. We will approach these in multiple steps,
- Bivariate Analysis of Pairs of Numerical Variables,
- Bivariate Analysis of Pairs of Categorical Variables,
- Bivariate Analysis of Pairs of Numerical and Categorical Variables.

#### 4.2.1. Bivariate Analysis: Pairs of Numerical Variables

We will be analysing pairs of numerical variables here.

We will begin by looking at the numerical parameters that are highly related to demand and sales. We are going to be making a pairplot of these parameters. These variables include:
- `Demand`,
- `Inventory_Levels`,
- `Cost_Prices`,
- `Selling_Prices`,
- `Competitor_Prices`,
- `Website_Traffic`.

<img width="770" alt="Bivariate Analysis_Pairs of Numerical Variables" src="https://github.com/user-attachments/assets/5911f0ca-1254-4e35-b6c3-790d29dfca21">

From the pairplot, we can see that:
There is a highly linear relationship between:
- `Selling_Prices` and `Cost_Prices`: This expected, as te price you sell is going to be highly dependent on the price at which you buy your products.
- `Competitor_Prices` and `Cost_Prices`: This is also expected as the competitor prices will also have a linear relationship with the cost price of the company.
- `Competitor_Prices` and `Selling_Prices`: The competitor prices and the selling prices of the company is expected to be linear becuase one can assume that they buy their products almost at the same price range.
- `Website_Traffic` and `Demand`: This relationship seems to indicate that traffic drives the demand of products.

The next thing I am going to look at now is the correlation between these numerical variables. We would like to see just how much correlation exists between them.

<img width="562" alt="Numerical Variables Corellation" src="https://github.com/user-attachments/assets/fba257eb-07e3-43a3-8b39-055aced6ec0a">

From this, we can easily see that:
- There's very high correlation (0.99-1.00) between `Selling_Prices`, `Competitor_Prices` and `Cost_Prices`. This should be so, because the price at which a product is sold is heavily determined by the price at which it was acquired.
- There is some high correlation (0.9) between `Demand` and the other variables `Website_Traffic`, `Conversion_Rates`, `Number_Of_Reviews`.
- There is some moderate correlation (0.29-0.32) between `Inventor_Levels` and other variables `Demand`, `Cost_Prices`, `Selling_Prices`, `Competitor_Prices`, `Website_Traffic`, `Conversion_Rates`, `Number_Of_Reviews`.
- There is some moderate inverse correlation (-0.51) between `Demand` and the other variables `Selling_Prices`, `Competitor_Prices` and `Cost_Prices`. This indicates that cheaper products tend to have the highest demands.

#### 4.2.2. Bivariate Analysis: Pairs of Categorical Variables

I will be analysing pairs of categorical variables here.

Some of the categorical variables I will be working with here will include:
- `Product_Categories`,
- `Product_Conditions`,
- `Customer_Locations`,
- `Customer_Genders`,
- `Competitor_Strategies`,
- `Marketing_Campaigns`,
- `New_Product_Releases`.
<img width="833" alt="Bivariant analysis for categorical varibales2" src="https://github.com/user-attachments/assets/52c056f3-c9a2-4425-8aed-d16059d1d3c4">
<img width="834" alt="Bivariant Analysis for categorical variables" src="https://github.com/user-attachments/assets/6ee7d5bb-3008-4ec1-827c-cbd04a813627">

From he above plots, we see that:
- For `Product_Categories` and `Product_Conditions`:
    - A majority of the product are new products, with most of the new products being `Clothing` and `Electronics`.
    - Used products had the second higest sales frequency, with products in `Clothing` and `Electronics` taking the higest frequency.
    - `Refurbished` products had the least frequency.
- For `Product_Categories` and `Customer_Genders`:
    - There were no significant differences between sales frequency for `Male` and `Female`.
    - Products in `Electronics` and `Clothing` still had the highest sales frequency.
- For `Customer_Locations` and `Marketing_Campaigns`:
    - `Social Media Ads` was the most frequent form of marketing. `Email Campaign` and `TV Ads` had the lowest frequency of the three marketing strategies.
    - Customers in `USA` were targeted the most. Customers in the `UK` and `Canada` were targeted fairly equally.
- For `Customer_Strategies` and `New_Product_Releases`:
    - Giving `Discounts` was the most frequent strategy employed by competitors, with `Price Matching` and `Bundle Offers` coming in second and third.
    - Most of the products were not new releases.

### 4.3. Profit Margin Analysis

Here, I just want to briefly look at the profit distribution for each sale.
<img width="853" alt="Profit Distribution per each sale" src="https://github.com/user-attachments/assets/2175724a-4a90-49fc-8a91-a9170678f56b">

From the plot:
- Total revenue on goods is lowest for goods in the `Home & Garden` category. The other categories have almost equal profit margins.
- Average revenue on goods is almost equal for all product categories.

### 4.4. Temporal Analysis

Here, we will be briefly looking at how some of the parameters in the dataset change with time. The parameters we will be looking at includes:
- `Demand`,
- `Inventory_Levels`,
- `Selling_Prices`,
- `Competitor_Prices`.

  <img width="828" alt="Parameters change with time" src="https://github.com/user-attachments/assets/eb4111bc-f6fb-4f3d-899a-b0884512e489">

  From the plots above,
- There is no observable weekly pattern in `Demand`, `Inventory_Levels` and `Selling_Prices`.
- However, it is observed that the competitor pricing was always higher than the selling price of our company, as seen from the negative values in the difference in selling prices and competitor prices.

## 5. Feature Engineering

Since we are going to be building models for demand forecasting and price optimization, we will need to prepare the dataset. And that is what we are going to be doing in this section. We will basically be splitting our data into train and test sets, and then visualize this split. We will train with the data for years below 2023, and then evaluate on data from the year 2023.
## 6. Demand Forecasting

Here, Am going to first build a model that can estimate future demand of the products. Am going to build individual models for each of the product categories; `Electronics`, `Clothing`, `Home & Garden`. And and what we're going to do is make estimates for future sales on a **weekly basis**. We will build an Exponential Smoothing model.

The model I will be building will be evaluated with three metrics:
- Root Mean Squared Error (RMSE),
- Mean Absolute Error (MAE),
- Mean Absolute Percentage Error (MAPE).

I will now build an Exponential Smoothing model to predict future demands on the train dataset, evaluate the model on our test dataset, and visualize the results.
## 7. Price Optimization

Since we already have our demand forecasting model, we will now go ahead to implement a solution for optimizing price of products over time in order to **Maximize Profits**, and improve **Market Competitiveness**.

Am going to do this in such a way that, if we are given the previous trading data for all other products, we should be able to optimize the new pricing of the products restocked for the new week. Hence, we are only going to go as far as the new week.

We will begin by writing two functions:
- `profit_objective` that will be the objective function to maximize the profit.
- `find_optimal_price` this function will calculate the optimal price of the products.

  Before we get to the next steps, we first have to split the data into **previous data** and **future data**.
- `previous_data` will be all data before 2023. This the data we assume we have, and the only data we are assuming the business has knowledge of.
- `future_data` will be all data from 2023 and above. In the business sense, we assume that the only thing the business knows from this data is the **cost price** and **product ID**.

**Why?**

For every new week, we are assuming the company has to restock. We are defining restocking here as buying of new products to sell, and for this reason we assume that the only knowledge the company has about the new week is the **cost price** of the product it bought (this cost price will be from the `future_data` for our analysis) for each product ID. Every other info like competitor pricing for every day of the week, demand, and all other things has to be estimated from previous data prior to that week (`previous_data` in our case).

Am going to model this problem in a proper business scenerio.

Next, I get the data we need to make predictions on the optimization work for every new week.
Now that I have gotten our data, I will now go ahead to estimate an optimal pricing for the products for each week in the test dataset.
I get to join the original data and our estimated pricing together, so that I can move forward later on with evaluating our approach.

I will now visualize the results on the test dataset.

<img width="833" alt="usual vs optimal price" src="https://github.com/user-attachments/assets/af034b60-7978-47ca-9161-b49f9d45629a">
<img width="845" alt="weekly comparison of usual and optimal profit margin nad price difference by category" src="https://github.com/user-attachments/assets/cd4f49c3-8db4-4549-ba9c-6d5bd811e24d">
As seen for the first four plots, we can obviously see that the prifit margins increase for Electronics, Clothing and Home & Garden as well as the total profit margin in all. This is visible because the orange lines are above the blue lines. 

Also, from the last four plots, we can see the difference between competitor prices and selling prices (using the old approach), and competitor prices and optimal price (using the new approach). The optimial difference (orange line) is now lower, meaning our pricing is now better in this case.
