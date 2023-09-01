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
| Less than 35k sold a year | More than 200k item sold a year |
| ![image](https://github.com/Bruc3U/Iowa_liquor_sale_analysis/assets/142362478/ecf02836-9ec2-4981-8a03-08b7e2799647) |![image](https://github.com/Bruc3U/Iowa_liquor_sale_analysis/assets/142362478/3c79ce29-6607-4846-b856-8777ea3ad34a)|

For instance, we will put an agglomeration in the rural class when the count of bottles sold falls below or equal to 100,000.<br>
We will get the data from the 2019 year. Then we will follow the evolution of those countries over the next 4 years.

To further our market segmentation and to avoid outlier data, we will differentiate B to B and B to C transactions.<br>
Since our analysis is focused on the average population, we will cut out all one-time sales that are above 500 USD. 
                                                                                                                          
Now that we have our market segmented, we must focus on the consumer pattern.<br>

To get a better understanding of the Iowa residents' behavior over the last 4 years, we have to ask several questions.<br>
- What is the top purchased item?
- What type of liquor is the most popular?
- What is the average quantity of liquor sold by liter?

Top 3 most popular liquor among rural counties by bottle sold (2019) : 

![image](https://github.com/Bruc3U/Iowa_liquor_sale_analysis/assets/142362478/6eb5c45f-cd2f-4351-87e2-47e5eb173124)


The most popular liquor is by far whiskey, in this case, black velvet is an imported Canadian whiskey.<br>
The brand has the most bottles sold and the average.<br>
The second most popular liquor is vodka. Both best-sellers are the 1.75-liter version. 

Top 3 most popular liquor among urban counties by bottle sold (2019) : 

![image](https://github.com/Bruc3U/Iowa_liquor_sale_analysis/assets/142362478/8b6047eb-30d2-47ae-b87e-0791742036f6)

Surprisingly, the urban taste in liquor is a little bit different.
Fireball is by far the most popular item in Urban centers. The small bottles are the most popular.<br>
Coming up for second place, we have Hawkeye vodka.

For the year 2019, rural and urban appear to have slightly different tastes and budgets. <br>

The average price for bottles in rural areas is 11.27 USD. Meanwhile, in urban areas, the average is 17.71 USD.<br> 
Another difference between urban and rural would be the diversity of their choice of liquor.<br>
As we can observe, the different type of liquor is between 3 to 5 for rural communities, while in the urban center will be between 6 and 7.<br>


Top 3 most popular liquor among urban counties by bottle sold (2020) : 

![image](https://github.com/Bruc3U/Iowa_liquor_sale_analysis/assets/142362478/05570f2c-fa44-4251-8b72-64b7fa719fca)


Regarding the pandemic, urban centers saw their taste widen in 2020 and shift from whiskeys to vodkas in 2021.<br>
Favorite day to purchase liquor 


urban Monday Sunday Friday
rural Tuesday Friday Wednesday 


Top 3 most popular liquor among rural counties by bottle sold (2020) : 

![image](https://github.com/Bruc3U/Iowa_liquor_sale_analysis/assets/142362478/3ebc3afa-d579-4fff-a97a-29e9865e1c53)


On the other hand, rural areas went through the 

Top 3 most popular liquor among rural counties by bottle sold (2021) : 

![image](https://github.com/Bruc3U/Iowa_liquor_sale_analysis/assets/142362478/67323145-14bc-46eb-98ce-28bc651afac8)


Top 3 most popular liquor among urban counties by bottle sold (2021) : 

![image](https://github.com/Bruc3U/Iowa_liquor_sale_analysis/assets/142362478/0dc9e2b7-cfe6-4c33-b696-cc20c54f1624)


The overall consumption of liters and bottles sold skyrocketed during those years.<br>
We also observe the average cost per bottle budget. 

Compared to the state average, 


# Conclusion

| Rural | Urban |
|----------|----------|
| Years | 
|2019|  | |
|2020| | |
|2021| | |

| State | 
|---------|
| Years | 

Recap table and state trends 

