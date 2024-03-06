# [Bellabeat Analisys Analysis Case Study](https://www.kaggle.com/code/bryana/bellabeat-analisys)

In this case study, perform many real-life tasks of a junior data analyst. Bellabeat, a high-tech manufacturer of women's health-focused products. To answer the company's key questions, I followed the steps of the data analysis process: ask, prepare, process, analyze, share and act.

# Scenario

You are a junior data analyst working on the marketing analyst team at Bellabeat, a high-tech manufacturer of health-focused products for women. Bellabeat is a successful small company, but they have the potential to become a larger player in the global smart device market. Urška Sršen, cofounder and Chief Creative Officer of Bellabeat, believes that analyzing smart device fitness data could help unlock new growth opportunities for the company. You have been asked to focus on one of Bellabeat’s products and analyze smart device data to gain insight into how consumers are using their smart devices. The insights you discover will then help guide marketing strategy for the company. You will present your analysis to the Bellabeat executive team along with your high-level recommendations for Bellabeat’s marketing strategy.

# Characters and products

## Characters

- **Urška Sršen**: Bellabeat’s cofounder and Chief Creative Officer
- **Sando Mur**: Mathematician and Bellabeat’s cofounder; key member of the Bellabeat executive team
- **Bellabeat marketing analytics team**: A team of data analysts responsible for collecting, analyzing, and reporting data that helps guide Bellabeat’s marketing strategy.

## Products

- **Bellabeat app**: The Bellabeat app provides users with health data related to their activity, sleep, stress, menstrual cycle, and mindfulness habits. This data can help users better understand their current habits and make healthy decisions. The Bellabeat app connects to their line of smart wellness products.
- **Leaf**: Bellabeat’s classic wellness tracker can be worn as a bracelet, necklace, or clip. The Leaf tracker connects to the Bellabeat app to track activity, sleep, and stress.
- **Time**: This wellness watch combines the timeless look of a classic timepiece with smart technology to track user activity, sleep, and stress. The Time watch connects to the Bellabeat app to provide you with insights into your daily wellness.
- **Spring**: This is a water bottle that tracks daily water intake using smart technology to ensure that you are appropriately hydrated throughout the day. The Spring bottle connects to the Bellabeat app to track your hydration levels.
- **Bellabeat membership**: Bellabeat also offers a subscription-based membership program for users. Membership gives users 24/7 access to fully personalized guidance on nutrition, activity, sleep, health and beauty, and mindfulness based on their lifestyle and goals.

# About the company

Urška Sršen and Sando Mur founded Bellabeat, a high-tech company that manufactures health-focused smart products. Sršen used her background as an artist to develop beautifully designed technology that informs and inspires women around the world. Collecting data on activity, sleep, stress, and reproductive health has allowed Bellabeat to empower women with knowledge about their own health and habits. Since it was founded in 2013, Bellabeat has grown rapidly and quickly positioned itself as a tech-driven wellness company for women.

By 2016, Bellabeat had opened offices around the world and launched multiple products. Bellabeat products became available through a growing number of online retailers in addition to their own e-commerce channel on their website. The company has invested in traditional advertising media, such as radio, out-of-home billboards, print, and television, but focuses on digital marketing extensively. Bellabeat invests year-round in Google Search, maintaining active Facebook and Instagram pages, and consistently engages consumers on Twitter. Additionally, Bellabeat runs video ads on Youtube and display ads on the Google Display Network to support campaigns around key marketing dates.

Sršen knows that an analysis of Bellabeat’s available consumer data would reveal more opportunities for growth. She has asked the marketing analytics team to focus on a Bellabeat product and analyze smart device usage data in order to gain insight into how people are already using their smart devices. Then, using this information, she would like high-level recommendations for how these trends can inform Bellabeat marketing strategy.

---

# Ask phase

Sršen asks you to analyze smart device usage data in order to gain insight into how consumers use non-Bellabeat smart devices. She then wants you to select one Bellabeat product to apply these insights to in your presentation. These questions will guide your analysis:

1. What are some trends in smart device usage?
2. How could these trends apply to Bellabeat customers?
3. How could these trends help influence Bellabeat marketing strategy?

Analyzing trends in smart device usage provides valuable insights that can help Bellabeat better understand its customers, optimize its marketing strategies, and drive continued innovation in its product offerings.

## What is the problem I'm trying to solve?

Bellabeat aims to leverage data analysis to understand trends in smart device usage and their potential implications for Bellabeat customers and marketing strategies. The company seeks to explore how these trends can be analyzed and applied to enhance customer engagement and drive business growth.

## Insights Driving Business Decisions

**1. Understanding Smart Device Usage Trends**: Analyzing trends in smart device usage can provide insights into consumer behavior, preferences, and adoption patterns.

**2. Customer-Centric Approach**: Identifying how these trends apply to Bellabeat customers can help tailor product offerings, features, and services to meet their evolving needs and expectations.

**3. Marketing Strategy Optimization**: Leveraging insights from smart device usage trends can inform targeted marketing campaigns, messaging, and channel selection to effectively reach and engage Bellabeat's target audience.

**4. Competitive Advantage**: Staying ahead of industry trends and consumer preferences can position Bellabeat as a leader in the wellness technology market and drive competitive advantage.

## Consider key stakeholders

- **Urška Sršen**: Cofounder and Chief Creative Officer of Bellabeat, responsible for product innovation and brand strategy.
- **Sando Mur**: Cofounder of Bellabeat and key member of the executive team, involved in strategic decision-making and business planning.
- **Bellabeat Marketing Analytics Team**: Responsible for analyzing data and providing insights to support marketing initiatives and business growth.
- **Bellabeat Customers**: End-users of Bellabeat products whose preferences and behavior are crucial in shaping product development and marketing strategies.

## A clear statement of the business task

Analyze trends in smart device usage, explore their applicability to Bellabeat customers, and identify opportunities to enhance marketing strategies and drive business growth based on these insights.

---

# Prepare phase

It is going to use public data that explores the daily habits of smart device users. [FitBit Fitness Tracker Data](https://www.kaggle.com/datasets/arashnic/fitbit): This Kaggle data set contains personal fitness tracker from thirty fitbit users. Thirty eligible Fitbit users consented to the submission of personal tracker data, including minute-level output for physical activity, heart rate, and sleep monitoring. It includes information about daily activity, steps, and heart rate that can be used to explore users’ habits.

This data is public domain, open-source data and free to use.

> This dataset generated by respondents to a distributed survey via Amazon Mechanical Turk between 03.12.2016-05.12.2016. Thirty eligible Fitbit users consented to the submission of personal tracker data, including minute-level output for physical activity, heart rate, and sleep monitoring. Individual reports can be parsed by export session ID (column A) or timestamp (column B). Variation between output represents use of different types of Fitbit trackers and individual tracking behaviors / preferences.

## How is the data organized? Is it in long or wide format?

The provided Kaggle dataset comprises personal fitness tracker data from thirty-three Fitbit users. These users have consented to submit their personal tracker data, which includes minute-level records of physical activity, heart rate, and sleep monitoring. The dataset encompasses details about daily activity, steps taken, and heart rate measurements, facilitating an exploration of users' habits. The dataset consists of 29 CSV files, each describing the aforementioned information at various levels of granularity. These data were collected from March 12, 2016, to May 12, 2016, spanning a period of two months.

| File Name | Description |
|--------|----------|
| **dailyActivity_merged** | Daily tracking over 31 days for 33 users of steps, distance travelled, tracker distance, logged activities distance, intensity of activity in terms of distance and minutes, and calories burned   |
| **dailyCalories_merged** | Daily calories burned over 31 days for 33 users |
| **dailyIntensities_merged** | Daily intensity tracked over 31 days for 33 users. Intensity was measured as minutes spent being sedentary, lightly active, fairly active, and very active and distance travelled when sedentary, lightly active, fairly active, and very active |
| **dailySteps_merged** | Daily steps over 31 days for 33 users |
| **heartrate_seconds_merged** | Heartrate of 14 users at each second of the day |
| **hourlyCalories_merged** | Calories burned by hour over 31 days for 33 users |
| **hourlyIntensities_merged** | Total and average intensity of activity by hour over 31 days for 33 users |
| **hourlySteps_merged** | Total steps by hour over 31 days for 33 users |
| **minuteCaloriesNarrow_merged** | Calories burned by minute over 31 days for 33 users |
| **minuteCaloriesWide_merged** | Calories burned by minute over 31 days for 33 users |
| **minuteIntensitiesNarrow_merged** | Intensity of activity by minute over 31 days for 33 users |
| **minuteIntensitiesWide_merged** | Intensity of activity by minute over 31 days for 33 users |
| **minuteMETsNarrow_merged** | MET (metabolic equivalent of a task) score by minute over 31 days for 33 users |
| **minuteSleep_merged** | Sleep and log value by minute over 31 days for 24 users |
| **minuteStepsNarrow_merged** | Steps by minute over 31 days for 33 users |
| **minuteStepsWide_merged** | Steps by minute over 31 days for 33 users |
| **sleepDay_merged** | Daily tracking over 31 days for 24 users of sleep count, minutes spent asleep and minutes spent in bed |
| **weightLogInfo_merged** | Daily weight (in kg and lbs), fat and BMI over 30 days for 8 users |

## Are there issues with bias or credibility in this data? Does your data ROCCC?

- **Unreliable**: The potential for sampling bias exists due to the limited sample size.
- **Incomplete**: The study lacks comprehensive demographic information on its anonymous participants, particularly regarding the usage patterns of the target demographic (women) with this product. Demographic information, such as gender, age, and health status, is unavailable. Given that Bellabeat’s target audience is women, having data focused specifically on this demographic would be optimal. However, it’s important to note that the absence of this demographic data may introduce a potential sampling bias
- **Outdated**: The dataset is time-constrained and not undergoing current updates. Consequently, the trends observed in the dataset may not accurately reflect current user behavior.

## How did you verify the data’s integrity?

I have been able to verify the integrity of the data by performing the following validations:

- **Visual check**: downloading, unzipping and seeing if the CSV files are complete and correctly formatted. This has allowed me to identify problems such as missing data and null values.
- **Size Check**: I have verified that the size of the files is significant. And I have noticed that CSV files with incomplete data have abnormally small file sizes.
- **Record comparison**: I have been able to observe that the CSV files have the expected format and generally contain the same data.
- **Checking Headers and Data Types**: I have ensured that the column headers are consistent across all files and that the column data types are as expected.

## How does it help you answer your question?

The provided dataset contains a wide range of variables related to users' daily activities, calories burned, intensities of activity, heart rate, steps taken, sleep patterns, and weight-related information. This dataset will be instrumental in answering the questions posed during the data analysis process.

### Trends in Smart Device Usage:

- **dailyActivity_merged**: This dataset provides insights into users' daily activities, including steps taken, distance traveled, and intensity of activity. Analyzing trends in these variables can help identify patterns in users' physical activity levels and how they utilize smart devices for tracking their daily fitness.
- **dailyCalories_merged**: Examining daily calories burned can reveal trends in users' overall energy expenditure and activity levels over the 31-day period, shedding light on their engagement with fitness tracking devices and their adherence to wellness goals.
- **dailyIntensities_merged**: This dataset offers detailed information on users' intensity of activity, categorized by levels of sedentary behavior, light activity, moderate activity, and vigorous activity. Understanding these patterns can elucidate how users distribute their physical activity throughout the day and how they utilize smart devices to monitor and manage their activity levels.
- **hourlyCalories_merged, hourlyIntensities_merged, hourlySteps_merged**: These datasets provide hourly insights into users' calorie expenditure, intensity of activity, and steps taken. Analyzing hourly trends can reveal patterns in users' activity levels and energy expenditure throughout the day, offering valuable insights into their behavior and engagement with smart devices.

### Application to Bellabeat Customers

- By analyzing the provided datasets, Bellabeat can gain a comprehensive understanding of how customers interact with their smart wellness products, including the Leaf tracker, Time watch, and Spring water bottle. Insights into users' activity levels, calories burned, sleep patterns, and weight-related information can help Bellabeat tailor its products and services to better meet the needs and preferences of its customers.
- Understanding trends in smart device usage among Bellabeat customers can also inform the development of new features, functionalities, and personalized recommendations within the Bellabeat app and other wellness products, enhancing the overall user experience and driving customer satisfaction and loyalty.

### Influence on Bellabeat Marketing Strategy

- Leveraging insights from the provided datasets, Bellabeat can refine its marketing strategy to effectively communicate the value proposition of its smart wellness products to target customers. For example, trends indicating increased engagement with fitness tracking features or improved sleep quality can be highlighted in marketing campaigns to emphasize the benefits of using Bellabeat products for holistic health and well-being.
- Tailoring marketing messages and content based on users' activity levels, calorie expenditure, and sleep patterns can help Bellabeat resonate with its target audience and drive customer acquisition and retention efforts.

## Are there any problems with the data?

The data was collected six years ago (outdated) with data collected for over two months and the sample size is insufficient, leading to an irrelevant and unreliable source to know the true population of users habits wearing smart devices. So this case study will be helpful as a quantitative exploratory study or analysis to provide preliminary trends in smart device usage habits.

---

# Process Phase

...
