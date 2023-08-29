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
In Iowa, COVID restrictions were put in place from June 2020 to September 2021.<br>
Restaurants, bars, and businesses had to close due to increasing cases.<br>
We will take a look at data before and after those events to draw our conclusions.<br>

Our analysis will take a look at several features.<br>
The first step, segmentation, will help us draw a consistent consumer behavior.<br>

![image](https://github.com/Bruc3U/Iowa_liquor_sale_analysis/assets/142362478/96f09aa6-efe1-4161-a14d-e3da09ab49c1)

The top best-selling cities are Des Moines, Cedar Rapids, and Davenport. The rest of the towns are significantly selling less 
To have a better understanding let's look at those changes in percent.

![image](https://github.com/Bruc3U/Iowa_liquor_sale_analysis/assets/142362478/cbaa28d6-97c0-4df8-88e1-9ff98496ed0e)


Let's take a look at the biggest change in %. <br>
From what the data shows, it seems that the year 2019 through the year of 2020 were just the beginning of the pandemic for the liquor market.<br>
Most larger cities had subsequential growth.  

![image](https://github.com/Bruc3U/Iowa_liquor_sale_analysis/assets/142362478/618c5b37-9f69-48af-ac7f-d38208779429)

On the other hand, the changes observed between the years 2020 and 2021 are more illustrative of what happened globally during the pandemic.<br>
Most stores suffered from the restrictive aspect of the pandemic. A few cities were able to sustain positive growth.<br>

To have a better overview of the situation, let's look at the counties.

![image](https://github.com/Bruc3U/Iowa_liquor_sale_analysis/assets/142362478/67029079-47a2-4fac-9805-f1ecbff5938e)

As we can observe most counties suffered losses during the pandemic.<br>
With some exceptions, the overall negative situation remains.<br>

### 2/Consumption Habits Analysis

Consumption habits greatly differ based on a multitude of factors. Since our data does not have much information on the consumer's origins, age, or familial situation, our analysis is by definition limited.<br>
A useful feature that the dataset offers is location.<br>
By categorizing our population into rural and urban settings, we can attain a better understanding of the context.

| Rural | Urban |
|----------|----------|
| 5000 <=  | >= 25 000  |

The main difference between rural and urban areas is population density. 
Our segmentation will use the number of items as a primary indicator for status.<br>
For instance, we will apply the rural classifier when the count of items sold is below or equal to 5,000.<br>
We will get the data from the 2019 year only. Then we will follow the evolution of those countries over the next 4 years.<br
                                                                                                                          
List of the most successful Urban counties:

![image](https://github.com/Bruc3U/Iowa_liquor_sale_analysis/assets/142362478/6e5f4426-bac0-48a6-9db0-548684e5de1b)

List of the most successful Rural counties:

![image](https://github.com/Bruc3U/Iowa_liquor_sale_analysis/assets/142362478/5894c59c-7b06-4b3b-a9c3-2478859a7ad5)

Now that we have our market segmented, we must focus on the consumer pattern.<br>

To get a better understanding of the Iowa residents' behavior over the last 4 years, we have to ask several questions.<br>
- What is the top purchased item?
- What type of liquor is the most popular?
- What is the average quantity of liquor sold by liter?

# Conclusion

