
<img width="1000" alt="image" src="https://github.com/rindangchi/Python-Practice/assets/10241058/de9b0e85-7f96-4a6c-9943-c18a8bd010e2">

# EDA Global Superstore

## Project Summary 
- The purpose of this analysis is to understand the current sales data in Global Superstore and to find any meanigful insight that can be used to improve business peerformance
  
- The analysis firstly conducted by understanding the data, including its variables, data types, the uniques values of each variable, and missing values. After that analysis is continued by explaining the statistical description of the data, such as mean, median, mode, and the distribution of the data.
  
- Analysis then divided into two sections based on the variable type, analysis is conducted separately between the numerical and categorical variable. It is followed by data visualization to make it easier to understand. Several type of graphs such as bar chart, correlation map, boxplot, and map are used to visualize the data. Under each visualization, explained the findings and some insights that can be used for the future project or analysis.

- From ths EDA process several insights are found and further can be used to make a better business decision. This analysis provides useful information for business user to increase profit, gain more customers, designing purchasing strategy, opening new branch, and many more. 
  
- The next analytical projects can be conducted using this data, for example market basket analysis, customer segmentation, prediction and many more.


## Background
Global superstore is a hypermart store that doing sales business for various customers both the company and personal customer. They also sells various stuffs range from office supplies, furniture, and technology. They have a lot of sales data and they want to use the sales data to understand their current sales better to improve and maximize their sales performance. As a data analyst in the global superstore company I am assigned to analyze and get insight about their current sales data by using exploratory data analysis.
In EDA I will try to understand the data, such as the variables, its data types, null value, and  performing descriptive statistics. EDA is important because it helps us to decide what the next things we need to do before performing data analysis or creating a new model. 

## Business Understanding
In this section I will breakdown the problems, goal, and objectives

### 1. Problem Statements
There are several problem statements that can be listed, stated as below:
- What is the most and least purchased product ?
- What is the most and least purchased product category ?
- Which state has the most and least purchased product ?
- Which product has the most and least profit value ?
- Which category has the most and least profit value ?
- Is there any correlation between variables, such as product, product category with profit value and number of purchased product?

### 2. Goal
Understanding and representing the current sales data in Global Superstore and  utilizing statictical method as well as data visualization to better understand the given dataset. 

### 3. Objectives
- Do exploratory data analysis to understand the current dataset
- Help business to uncover trends and any meaningful findings that can be used to improve business decision

### 3. Exploratory Data Analysis 
In this part I will explain the result of the exploratory data analysis that has been done. For full code can be accessed here : 
 1. [Github](https://github.com/rindangchi/Python-Practice/blob/main/EDA%20Superstore/3_Exploratory_Data_Analysis_Sample_Global_Superstore.ipynb)
 2. [Google Colabs](https://colab.research.google.com/drive/1lt6DFEKMWPJwrvfTQQJqOGGXxsvob504?usp=sharing)

### 5.1. About the Dataset

Using shape and info function from pandas, found the charateristics of each variable as stated in the picture below, including the existance of null value, the column names, and the data types.

<img width="208" alt="image" src="https://github.com/rindangchi/Python-Practice/assets/10241058/0e4a6f5e-fbe0-4d8e-ba49-c67d7402a6f9">

In the dataset description, for postal code columns, its data type is still int, so that i change the datatype into object to make the dataset valid. 
Below are the details of each column after I change the data type for postal code column.

<img width="208" alt="image" src="https://github.com/rindangchi/Python-Practice/assets/10241058/946bd90c-b89b-4c46-8abf-b1a966710c96">

<br>

- The data set contains 9993 rows and 13 columns. And there is no null values for all variables or columns.
- The data set contains 13 columns, which includes both categorical and numerical variables.
- The categorical variables are indicated with Object data type and the numerical variable is indicated with the int64 data type.


#### Understanding the given variables
Variables stated in the datasest is divided into two categories, there are numerical and categorical variables. 

##### Categorical variables:
**Ship Mode**: delivery mode chosen by customer       
**Segment**: customer segment who purchase the product          
**Country**: country where customers located          
**City**: City where customers located             
**State**: State where customers located         
**Postal Code**: Postal code where customers located     
**Region**: Region where customers located          
**Category**: Product category purchased by customer        
**Sub-Category**: Product sub-category purchased by customer  

#### Numerical VariableS:
**Sales**: Sales value of each transaction, measured in USD         
**Quantity**: Quantity of product purchased per transaction        
**Discount**: Discount given to customers for each transaction     
**Profit**: Profit generated for each transaction, measured in USD       


### 5.2. Analysis of Categorical Variable 
From the dataset, I did analysis separately for categorical and numerical variables. In this section I will explain my finding on categorical variables.  
Using the describe function, it can be seen some information as stated in the picture below:

<img width="600" alt="image" src="https://github.com/rindangchi/Python-Practice/assets/10241058/16bb7120-04fe-4442-a71d-75e3ee3bf6d3">

<br></br>
Using barchart dataset is visualized to rank the most and the least frequency for each variable.
<br></br>
<img width="477" alt="image" src="https://github.com/rindangchi/Python-Practice/assets/10241058/095a1334-ddb9-479d-bfaa-e61f27311a14">
<br></br>
<img width="500" alt="image" src="https://github.com/rindangchi/Python-Practice/assets/10241058/beb2005b-85d5-40ec-ac60-e94e1b0fbb99">
<br></br>
<img width="477" alt="image" src="https://github.com/rindangchi/Python-Practice/assets/10241058/e620e01e-15ab-4bda-8423-85663545207a">

<br></br>
**Findings and Observation**
1. Standard class is the most chosen shipment mode and same day is the least used mode
2. Looking at the customer segment, the most segment did the transaction is consumer segment and the segment did the least transaction is home office
3. Most transaction came from West and the least came from South
4. Most purchased product category is office supplies and the least is technology
5. Most purchased product sub-category is office supplies and the least is copiers
6. Most customer who did transactions came from California and the least transaction came from Wyoming.

Further analysis then conducted to get deeper insight from the dataset.
- For the Region, West is region with the highest frequency of buying. From this point we can analyze whether cities with top buying frequency is located in the West region or not and is there any West city having small frequency of buying. By analyzing this, we know that West region is having a lot of potential buyer and we can develop strategy on how to improve buying frequency in the West region cities.


- For the state and city with the lowest purchasing frequency, further analysis can be done to find out what products and categories are purchased most in that cities. The marketing team can push more promotion regarding the products to the buyer resided in those cities.  

#### Finding Correlation between categorical variable 

For correlation between catgeorical variable I use Cramers V method. The charmer's v method should be use because of following reason:
1. To know the relationship between two variables
2. Variables are categorical
3. Variables have two or more unique values

<img width="337" alt="image" src="https://github.com/rindangchi/Python-Practice/assets/10241058/a8c0cfc7-9fe0-4aab-909c-245de339f155">
<br>
According to the result, some variables that have same characteristics or exact pattern like city, state, region postal code, category and sub-category have strong correlation. It also can be stated that the dataset is good and valid. In the other hand other variables with different characteristics have very weak correlation.

### 5.2. Analysis of Numerical Variables
In this section I will explain the finding for numerical variables. 

### Descriptive Statitics
Using describe function in python, here I can find the descriptive statistics for each numerical variable. 

<img width="279" alt="image" src="https://github.com/rindangchi/Python-Practice/assets/10241058/0886400b-b18d-4583-b5ff-3a32295173e7">

The statistics descriptive above can be explained below:
<br></br>
**Sales**
1. The average sales value is USD 229.85
2. The standard deviation of the sales value is USD 623.27, meaning that the variation of the data is quite high
3. The minimum sales value is USD 0,44 it indicates that they are several transaction that are very low, business can analyze which product that has low transaction and define some promotion program. In the other hand the maximum sales amount recorded is USD 22638, it is quite high, using this finding business can analyze what customer doing this high transaction and attract them to stay loyal with the company, business also can analyze which product that has this high value of sales and improve the transaction to gain more profit.
4. The 25% percentile of sales is USD 17.28, it means that 1/4 of sales has maximum value of USD 17,28.
5. The 50% percentile is USD 54.48 meaning that half of the sales have no value more than USD 54.48, it is a low value.
6. The 75% of sales is USD 209, this value indicates that 75% of sales transaction is no more than USD 209, this value also quite low. It means that most transactions have very low total amount.
<br></br>
**Quantity**
1. The average quantity is 3.7, indicating that customers tend to buy few items per transaction.
2. The standard deviation is 2.2, it is not too different with the mean, indicating that the data has low variation
3. The minimum qty bought by customer is 1 and the maximum is 14, indicating that some transaction is just single item and in the other hand it is a transaction with high quanity. Targeting and understanding the characteristics and preferences of customers who make larger purchases can help increase sales and customer satisfaction.
4. The 25% percentile is 2, meaning that 1/4 transaction has item less than 2. The 50% is 3, meaning that half transaction do not have more than 5 items per transaction. While the 75% is 5, it means most transactions still have very low quantity.
<br></br>
**Discount**
1. The average discount is 0.15 and its standard deviation is 0.2
2. The 25% is 0 means that 1/4 transaction data do not have any discount applied. 50% and 75% precentile is 0.2 means that most transactions have discount less than 20%. It means that bsuiness do not give many discounts. Business my analyze whether discount will affect on sales and profit.
<br></br>
**Profit**
1. The average profit per transaction is USD 28.65 with standard deviation value USD 234, since the difference between standard deviation and mean is relatively high, it indicates that data has high variation of profit value
2. The 25 percentile is USD 1.7, 50 perecntile is USD 8.6, and 75 percentile is USD 29, it indicates that 75% of the transaction has profit less than USD 29, this value is still quite low.
3. The highest profit recorded is USD 8399, it indicates that certain transaction is highly profitable, in the other hand the minimum value is USD -6599 it is also indicate that certain transaction has a very high loss.







