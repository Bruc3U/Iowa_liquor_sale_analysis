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
The fallout of COVID made many people travel less, and go out less frequently.

Since alcohol is an important part of Western culture, the changes brought by such events would indeed reflect this aspect.<br>
Our focus will be to determine how COVID-19 changed individual habits of alcohol consumption.<br>
In order to do so, we will look at the sales, best-selling products, and time of purchase. 

# II/Data Wrangling: 

Since the dataset is quite significant, 27 million rows justify a 7 Go file. We will use Google Could's Big query SQL to format and analyze the data.<br>
In the second part of our project, we will use Power BI to create an interactive dashboard to illustrate our insights.

Our first task is to reduce the number of rows. We will be filtering rows from January 1st, 2019 to December 31st, 2022. <br>

![image](https://github.com/Bruc3U/Iowa_liquor_sale_analysis/assets/142362478/878464bb-482b-4306-9e28-dcb00d7c5b5c)

To increase our processing power, we will separate each year into its own CSV file using Power Query.<br>
This will allow us to have a better computing performance in Power BI.  

# III/ Analysis:
### 1/Exploratory Data Analysis

The dataset records all of the transactions made between the year 2019 to 2022.<br>

In Iowa, COVID restrictions were put in place from June 2020 to September 2021.<br>
Restaurants, bars, and businesses had to close due to increasing cases.<br>
We will take a look at data before and after those events to draw our conclusions.<br>

Our analysis will take a look at several features.<br>
The amount of bottles sold per transaction will be used to construct our analysis.<br>
This will allow us to track the frequency of purchases, and the popularity of certain products.<br>
We will later, add the number of liters sold and, the total in dollars for each sale.

![image](https://github.com/Bruc3U/Iowa_liquor_sale_analysis/assets/142362478/d4493b38-d89e-44e5-8860-a36f73da725f)


The top best-selling cities are Des Moines, Cedar Rapids, and Davenport. The rest of the towns are significantly selling less 
To have a better understanding let's look at those changes in percent.

![image](https://github.com/Bruc3U/Iowa_liquor_sale_analysis/assets/142362478/f39e7258-b4e6-4202-90bf-ce202c7b78df)

From what the data shows, it seems that the year 2019 through the year of 2020 were just the beginning of the pandemic for the liquor market.<br>
We can observe DES MOINES was most affected by the pandemic, with several businesses closing, most individuals remained in the suburbs or outside of the city.<br>
For instance, WEST DES MOINES has seen the biggest increase yet, which validates the major population movement observed during the pandemic. 

![image](https://github.com/Bruc3U/Iowa_liquor_sale_analysis/assets/142362478/45459339-50ce-4d9f-b945-7161ffa9326e)

During the year 2020 through 2021, weaker growth is observed. <br>
DES MOINES recovered most of its pandemic losses, individuals moved back after many restrictions were removed. 

To have a better overview of the situation, let's look at the counties.

![image](https://github.com/Bruc3U/Iowa_liquor_sale_analysis/assets/142362478/d0976368-e7f1-423b-9da4-9f5ca78aa9ce)

As we can observe most counties suffered losses during the pandemic.<br>
POLK County (DES MOINES) remains sheltered from the aftermath.<br>
This enhances our first conclusion, most urban centers barely kept their initial growth.<br> 
Moreover, looking at counties expanded our vision on the matter.

Our overall analysis confirmed several trends during the pandemic.<br>
Many individuals moved out of city hubs and remained in the suburbs or smaller agglomerations.<br>
The county analysis showed us the decrease in overall liquor purchases in the state of Iowa.<br>

To complete our hypothesis, we will need to look at individual behavior. 

### 2/Consumption Habits Analysis

Consumption habits greatly differ based on a multitude of factors. Since our data does not have much information on the consumer's origins, age, or familial situation, our analysis is by definition limited.<br>
A useful feature that the dataset offers is location.<br>
By categorizing our population into rural and urban settings, we can attain a better understanding of the context.

The main difference between rural and urban areas is population density. 
Our segmentation will use the number of bottles sold as a primary indicator for status.<br>

| Rural | Urban |
|----------|----------|
| Less than 100k sold a year | More than 250k item sold a year |
| ![image](https://github.com/Bruc3U/Iowa_liquor_sale_analysis/assets/142362478/34553ef4-fc79-447d-a36b-056ecfbae24d)|![image](https://github.com/Bruc3U/Iowa_liquor_sale_analysis/assets/142362478/b3653639-97ae-4eb7-83c0-c1d7d0d49aab)|

For instance, we will put an agglomeration in the rural class when the count of bottles sold falls below or equal to 100,000.<br>
We will get the data from the 2019 year. Then we will follow the evolution of those countries over the next 4 years.
                                                                                                                          
Now that we have our market segmented, we must focus on the consumer pattern.<br>

To get a better understanding of the Iowa residents' behavior over the last 4 years, we have to ask several questions.<br>
- What is the top purchased item?
- What type of liquor is the most popular?
- What is the average quantity of liquor sold by liter?

Year 2019:
Urban:

![image](https://github.com/Bruc3U/Iowa_liquor_sale_analysis/assets/142362478/c2c59c04-b0f1-496d-95ed-cf4fc0a9a63e)

Rural:

![image](https://github.com/Bruc3U/Iowa_liquor_sale_analysis/assets/142362478/e18edd72-9940-466d-bb8a-a63e4d9237c8)

Year 2020:
Urban:

![image](https://github.com/Bruc3U/Iowa_liquor_sale_analysis/assets/142362478/cac7c6cc-474b-4edf-a9e3-b11c1c512db3)


Rural:

![image](https://github.com/Bruc3U/Iowa_liquor_sale_analysis/assets/142362478/cb641ac3-da18-4867-b6c4-54047e22c4c6)

Year 2021:
Urban:

![image](https://github.com/Bruc3U/Iowa_liquor_sale_analysis/assets/142362478/c13e5d2b-62ec-4a57-8f88-bd4dbbba38eb)


Rural:

![image](https://github.com/Bruc3U/Iowa_liquor_sale_analysis/assets/142362478/ed8014fb-035a-4785-a858-2e8d8c77dd6f)




# Conclusion

