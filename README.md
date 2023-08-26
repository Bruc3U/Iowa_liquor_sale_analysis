# 🍻 Iowa liquor sale analysis

![jon-parry-C8eSYwQkwHw-unsplash](https://github.com/Bruc3U/Iowa_liquor_sale_analysis/assets/142362478/c685fed2-641a-42b4-a3a4-8c66bc01c25f)



# Tool Used
- SQL
- Power BI

## Objective

Our goal is to analyze the data from 2019 through 2022 to see the changes in purchasing behavior after the COVID-19 pandemic. 


## About the dataset

The dataset records all liquor purchases made in the state of Iowa between 2012 through 2021.<br>
Many factors were recorded:

- Date
- Location of Purchase
- Type of product
- Liters sold

The dataset can be found [here](https://data.iowa.gov/Sales-Distribution/Iowa-Liquor-Sales/m3tr-qhgy)

# I/Defining the goal:

The recent events of 2020, made drastic changes to our society. Many businesses and jobs went remote. <br>
Individuals lost their habits of going out for a while and formed new habits.<br>
The fallout of COVID made many people travel less, and go out less frequently. Many habits were changed. 

Since alcohol is an important part of Western culture, the changes brought by such events would indeed reflect this aspect.<br>
Our focus will be to determine how COVID-19 changed individual habits of alcohol consumption.<br>
In order to do so, we will look at the sales, best-selling products, and time of purchase. 

# II/Data Wrangling: 

Since the dataset is quite significant, 27 million rows justify a 7 Go file. We will use Google Could's Big query SQL to format and analyze the data.<br>
In the second part of our project, we will use Power BI to create an interactive dashboard to illustrate our insights.

Our first task is to reduce the number of rows. We will be filtering rows from January 1st, 2019 to December 31st, 2022. <br>

![image](https://github.com/Bruc3U/Iowa_liquor_sale_analysis/assets/142362478/878464bb-482b-4306-9e28-dcb00d7c5b5c)

To increase our processing power, we will separate each year into its own CSV file.<br>
This will allow us to have a better computing performance in Power BI.  

# III/ Analysis:
### 1/Exploratory Data Analysis

The dataset records all of the transactions made between the year 2019 to 2022.<br>
In Iowa, major COVID restrictions were put in place from March 2020 to September 2021.<br>
We will take a look at data before and after those events to draw our conclusions.<br>

Our analysis will take a look at several features.<br>
The first step, segmentation, will help us draw a consistent consumer behavior.<br>

![image](https://github.com/Bruc3U/Iowa_liquor_sale_analysis/assets/142362478/96f09aa6-efe1-4161-a14d-e3da09ab49c1)

As we can see 


We will take a look at rural inhabitants versus city dwellers' behavior. 


# Conclusion

