<img width="158" alt="image" src="https://github.com/rindangchi/Python-Practice/assets/10241058/b7f17dff-91f4-40b6-8ca5-b0a459308428">
<img width="1000" alt="image" src="https://github.com/rindangchi/Python-Practice/assets/10241058/de9b0e85-7f96-4a6c-9943-c18a8bd010e2">

# EDA Global Superstore

## Project Summary 
- The purpose of this analysis is to understand the current sales data in Global Superstore and to find any meanigful insight that can be used to improve business peerformance
  
- The analysis firstly conducted by understanding the data, including its variables, data types, the uniques values of each variable, and missing values. After that analysis is continued by explaining the statistical description of the data, such as mean, median, mode, and the distribution of the data.
  
- Analysis then divided into two sections based on the variable type, analysis is conducted separately between the continous and categprical variable. It is followed by data visualization to make it easier to understand. Several type of graphs such as bar chart, correlation map, boxplot, and map are used to visualize the data. Under each visualization, explained the findings and some insights that can be used for the future project or analysis.

- From ths EDA process several insights are found and further can be used to make a better business decision. This analysis provides useful information for business user to increase profit, gain more customers, designing purchasing strategy, opening new branch, and many more. 
  
- The next analytical projects can be conducted using this data, for example market basket analysis, customer segmentation, prediction and many more.


## Background
Global superstore is a unreal store that doing sales business for various customers both the company and personal customer. They also sells various stuffs range from office supplies, furniture, and technology. They have a lot of sales data and they want to use the sales data to understand their current sales better to improve and maximize their sales performance. As a data analyst in the global superstore company I am assigned to analyze and get insight about their current sales data by using exploratory data analysis.
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
- Is there any correlation between variables, such as location, product, or product category with profit value and number of purchased product?
- How are the distribution of 

### 2. Goal
Understanding and representing the current sales data in Global Superstore and  utilizing statictical method as well as data visualization to better understand the given dataset. 

### 3. Objectives
- Do exploratory data analysis to understand the current dataset
- Help business to uncover trends and any meaningful findings that can be used to improve business decision

### 3. Exploratory Data Analysis 
In this part I will explain the result of the exploratory data analysis that has been done. For full code can be accessed here : 
 1. [Github](https://github.com/rindangchi/Python-Practice/blob/main/EDA%20Superstore/3_Exploratory_Data_Analysis_Sample_Global_Superstore.ipynb)
 2. [Google Colabs](https://colab.research.google.com/drive/1lt6DFEKMWPJwrvfTQQJqOGGXxsvob504?usp=sharing])

### 5.1. About the Dataset

Using shape and info function from pandas, found the charateristics of each variable as stated in the picture below, including the existance of null value, the column names, and the data types.

<img width="208" alt="image" src="https://github.com/rindangchi/Python-Practice/assets/10241058/0e4a6f5e-fbe0-4d8e-ba49-c67d7402a6f9">

In the dataset description, for postal code columns, its data type is still int, so that i change the datatype into object to make the dataset valid. 
Below are the details of each column after I change the data type for postal code column.

<img width="208" alt="image" src="https://github.com/rindangchi/Python-Practice/assets/10241058/946bd90c-b89b-4c46-8abf-b1a966710c96">

<br>

- The data set contains 9993 rows and 113 columns. And there is no null values for all variables or columns.
- The data set contains 13 columns, which includes both categorical and continous variables.
- The categorical variables are indicated with Object data type and the continous variable is indicated with the int64 data type.
- There is no null values in the data set.

#### Understanding the given variables
Variables stated in the datasest is divided into two categories, there are continous and categorical variables. 

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

#### Continous VariableS:
**Sales**: Sales value of each transaction, measured in USD         
**Quantity**: Quantity of product purchased per transaction        
**Discount**: Discount given to customers for each transaction     
**Profit**: Profit generated for each transaction, measured in USD       


### 5.2. Analysis of Categorical Variable 
From the dataset, I did analysis separately for categorical and continous variables. In this section I will explain my finding on categorical variables.  
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
- For the State, West is state with the highest frequency of buying. From this point we can analyze whether cities with top buying frequency is located in the West region or not and is there any West city having small frequency of buying. By analyzing this, we know that West region is having a lot of potential buyer and we can develop strategy on how to improve buying frequency in the West region cities.
- For the state and city with the lowest purchasing frequency, further analysis can be done to find out what products and categories are purchased most in that cities. The marketing team can push more promotion regarding the products to the buyer resided in those cities.  










