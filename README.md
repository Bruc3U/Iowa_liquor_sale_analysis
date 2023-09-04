# 🍻 Iowa liquor sale analysis

![jon-parry-C8eSYwQkwHw-unsplash](https://github.com/Bruc3U/Iowa_liquor_sale_analysis/assets/142362478/c685fed2-641a-42b4-a3a4-8c66bc01c25f)



# Tool Used
- SQL
- Power BI
- Excel

## Objective

Our goal is to analyze the data from 2019 through 2022 to see the changes in purchasing behavior after the COVID-19 pandemic. 


## About the dataset

The dataset records all liquor purchases made in the state of Iowa between 2012 through 2021.<br>

Many factors were recorded:

- Date
- Location of Purchase
- Store name
- Type of product
- Liters sold
- Number of bottles per transaction

The dataset can be found [here](https://data.iowa.gov/Sales-Distribution/Iowa-Liquor-Sales/m3tr-qhgy)

# I/Defining the goal:

The recent events of 2020, made drastic changes to our society. Many businesses and jobs were affected. <br>
Individuals changed their behavior and formed new habits.<br>
The fallout of COVID made many people travel less, and participate in outdoor activities less frequently.

Distilled fermented grains are an important part of Western culture. Sudden recent changes could influence our way of viewing and interacting with it.<br>
Our mission will be to determine how COVID-19 changed Iowa's resident alcohol consumption and how it impacted their daily life.<br>

# II/Data Wrangling: 

The dataset is quite significant, with 27 million rows. Google Could's Big Query SQL seems a perfect tool to format and analyze big amounts of data.<br>
In the second part of our project, we will use Power BI to create an interactive dashboard to illustrate our insights.

Our first task is to reduce the number of rows. We will be filtering rows from January 1st, 2019 to December 31st, 2022. <br>

![image](https://github.com/Bruc3U/Iowa_liquor_sale_analysis/assets/142362478/878464bb-482b-4306-9e28-dcb00d7c5b5c)

To increase our processing power, we will separate each year into its own CSV file using Power Query.<br>
This will allow us to have a better computing performance in Power BI.  

# III/ Analysis:
### 1/Exploratory Data Analysis

In Iowa, COVID-19 restrictions were effective from June 2020 to September 2021. Restaurants, bars, and businesses had to close due to increasing cases.<br>
We will take a look at data before and after those events to draw our conclusions.<br>

Our analysis will take a look at several features.<br>

The amount of bottles sold per transaction will be used to construct our analysis. This will allow us to track the frequency of purchases, and the popularity of certain products.<br>
Our goal is to first draw a general trend and then isolate factors to follow with a focused view. 

![image](https://github.com/Bruc3U/Iowa_liquor_sale_analysis/assets/142362478/d4493b38-d89e-44e5-8860-a36f73da725f)

The top best-selling cities are Des Moines, Cedar Rapids, and Davenport. The rest of the towns are significantly selling less.<br>
To have a better understanding let's look at those changes in percent.

![image](https://github.com/Bruc3U/Iowa_liquor_sale_analysis/assets/142362478/f39e7258-b4e6-4202-90bf-ce202c7b78df)

From what the data shows, it seems that the year 2019 through the year of 2020 was just the beginning.<br>
We can observe DES MOINES was most affected by the pandemic, with several businesses closing, most individuals remained in the suburbs or outside of the city.<br>
For instance, WEST DES MOINES has seen the biggest increase yet, which validates the major population movement observed during the pandemic. 

![image](https://github.com/Bruc3U/Iowa_liquor_sale_analysis/assets/142362478/45459339-50ce-4d9f-b945-7161ffa9326e)

During the year 2020 through 2021, weaker growth is observed. <br>
DES MOINES recovered most of its pandemic losses, individuals moved back after many restrictions were removed. 

To have a better overview of the situation, let's look at the counties.

![image](https://github.com/Bruc3U/Iowa_liquor_sale_analysis/assets/142362478/d0976368-e7f1-423b-9da4-9f5ca78aa9ce)

As we can observe most counties suffered losses during the pandemic. POLK County (DES MOINES) remains sheltered from the aftermath.<br>
This enhances our first conclusion, most urban centers barely kept their initial growth.<br> 

Our overall analysis confirmed several trends during the pandemic. Many individuals moved out of city hubs and remained in the suburbs or smaller agglomerations.<br>
The county analysis showed us the decrease in overall liquor purchases in the state of Iowa.

Despite our analysis, the data does not differentiate between individuals and businesses. Our goal is to draw conclusions on the behavioral changes of Iowa residents, not businesses.<br>
In this case, we will need to restrict the data to avoid business transactions in order to focus on private individuals. 

### 2/Consumption Habits Analysis

Consumption habits greatly differ based on a multitude of factors. Since our data does not have much information on the consumer's origins, age, or familial situation, our analysis is by definition limited.<br>
A useful feature that the dataset offers is location.<br>
By categorizing our population into rural and urban settings, we can attain a better understanding of the context.

The main difference between rural and urban areas is population density. 
Our segmentation will use the number of bottles sold as a primary indicator for status.<br>

To further our market segmentation and to avoid outlier data, we will differentiate Business to Business activities and Business to Consumers activities.<br>
Since our analysis is focused on the average population, we will filter out all one-time sales that are above 500 USD.

Segmented counties: 

| Rural | Urban |
|----------|----------|
| Less than 35k sold a year | More than 200k item sold a year |
| ![image](https://github.com/Bruc3U/Iowa_liquor_sale_analysis/assets/142362478/ecf02836-9ec2-4981-8a03-08b7e2799647) |![image](https://github.com/Bruc3U/Iowa_liquor_sale_analysis/assets/142362478/3c79ce29-6607-4846-b856-8777ea3ad34a)|

Counties are classified by count of bottles sold.<br>
For instance, an agglomeration will be placed in the rural category when the count of bottles sold falls below or is equal to 100,000.<br>
To follow the evolution of those countries over the next 4 years, we will use the data from 2019. 
                                                                                                                          
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
Urban centers and rural areas have both strong liquor favorites. Fireball whiskey and Black Velvet whiskey.


Top 3 most popular liquor among urban counties by bottle sold (2020) : 

![image](https://github.com/Bruc3U/Iowa_liquor_sale_analysis/assets/142362478/05570f2c-fa44-4251-8b72-64b7fa719fca)


Regarding the pandemic, urban centers saw their taste widen in 2020 and shift from whiskeys to vodkas in 2021.<br>
The slow decline of Fireball whiskey will continue in 2021, and be finally replaced by Hawkeye vodka.<br>
The brand will however remain in the top 3 most purchased liquor but the 1.75 liter bottle will be replaced by the smaller and more affordable sizes. 

Top 3 most popular liquor among rural counties by bottle sold (2020) : 

![image](https://github.com/Bruc3U/Iowa_liquor_sale_analysis/assets/142362478/3ebc3afa-d579-4fff-a97a-29e9865e1c53)

Rural areas did share some similarities with larger counties. Nevertheless, those areas remain slightly different.<br>
Individuals did expand, at a slower pace, their taste by adding other brands of vodka and whiskey.<br>
Likewise, rural areas saw a shift of taste, from whiskey to vodka. 

Let's take a deeper look at the number of bottles sold and the average liter bought for both categories.<br>
We can observe a similar trend, both rural and urban consumed more liquor during COVID.<br>

![image](https://github.com/Bruc3U/Iowa_liquor_sale_analysis/assets/142362478/993bef8b-7832-4a78-b8a9-60e1c549f017)

Both categories did spend more on liquor but the quality and price per bottle decreased. Especially in urban centers.<br>
From 2019 to 2021, urban centers saw their average bottle price drop by 17%.<br>
On the other hand, rural areas saw a 14% drop.<br>

This indicates the loss of purchasing power in both categories.<br>
The change in taste could be explained by this loss of purchasing power, but also by several shortages experienced during the pandemic.<br>

![image](https://github.com/Bruc3U/Iowa_liquor_sale_analysis/assets/142362478/6376760c-2579-42ff-bcf5-24ad54d0a0fd)

The overall consumption of liters and bottles sold skyrocketed during those years.<br>
The pandemic changed several key behaviors in rural and urban populations.<br>
Both categories went through a similar scenario where consumption increased while tastes changed.<br>

# Conclusion

In conclusion, COVID-19 has deeply affected our society in a variety of ways.<br>
Despite differences, individuals reacted similarly to the pandemic and the market changed for a long time.<br>

The main challenge was the dataset size, many superficial data had to be analyzed and cleared before proceeding to any further actions.<br>
Segmentation was needed. By categorizing our data into several groups, and limiting analysis to private individuals we were able to increase the overall accuracy.<br>

Liquor is an everyday relaxant for many individuals, during troubled times, we often see its consumption increase.<br>
Iowa's rural and urban citizens did play according to this trend.<br>
We saw a tremendous increase in the amount purchased, with an overall taste change. A key influence for those transformations is purchasing power.<br>
As the pandemic spread, we saw a serious decline in the liquor budget while consumption increased.<br>
All-time favorites started to shift, for instance, vodka became the most popular drink in urban areas and ended 5 years of whiskey rein.<br>
On the other side, rural areas saw the same trend. Vodka consumption increased. 

We can draw several hypotheses for such change.<br>
The shift in taste could be explained by a lower budget for alcohol caused by a tightening of the job market. With less purchasing power, individuals resorted to cheaper liquor.<br>
The size of bottles also shrank, for instance in 2021, the famous 1.75-liter cinnamon whiskey bottles were exchanged for smaller versions. 

Overall the liquor market in Iowa reflected well what most people went through during the pandemic.<br>
A major decrease in purchasing power coupled with economic instability caused many individuals to lower their expenses.<br>
This event definitely shifted consumer behavior and encouraged individuals to drink in a greater amount and more frequently.<br>

# ANNEXES: 


Top 3 most popular liquor among rural counties by bottle sold (2021) : 

![image](https://github.com/Bruc3U/Iowa_liquor_sale_analysis/assets/142362478/67323145-14bc-46eb-98ce-28bc651afac8)


Top 3 most popular liquor among urban counties by bottle sold (2021) : 

![image](https://github.com/Bruc3U/Iowa_liquor_sale_analysis/assets/142362478/0dc9e2b7-cfe6-4c33-b696-cc20c54f1624)

