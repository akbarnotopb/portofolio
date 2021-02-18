# Quick Overview of Covid Worldwide Vaccination
Here are some quick Covid-19 Worldwide Vaccination Exploratory Data Analysis. The datas used in this EDA are available [Online](https://www.kaggle.com/gpreda/covid-world-vaccination-progress, "Kaggle Covid 19 Wolrd Vaccination Progress"). The datasets itself are updated regularly. In our scenario, we will use the latest version ( 6 February 2021 ).

## About Vaccine
As per date, there are `8 vaccine types` used in `78 countries`. `Pfizer/BioNTech` is the most used wordwide followed by `Oxford/AstraZeneca` as shown in figure below.

![vaccine type](https://raw.githubusercontent.com/akbarnotopb/portofolio/main/Data%20Science/EDA/covid-resources/vaccine%20type%20used%20and%20its%20country%20count.PNG "Vaccination Type")

Most country only rely on one type but there is one country that is three types of vaccine, meanwhile the other are using 2 type of vaccines. More detail about how many vaccine used in 78 countries are shown below.

![vaccine type in hundred](https://github.com/akbarnotopb/portofolio/blob/main/Data%20Science/EDA/covid-resources/how%20many%20vaccine%20used%20in%20each%20country%20in%20hundred.PNG "Vaccination Type in Hundred")

## Vaccination Progres
### How vaccinations are progressing around the globe?
The vaccination progres of each country shown in figure below.

![skewed linechart](https://github.com/akbarnotopb/portofolio/blob/main/Data%20Science/EDA/covid-resources/uncleaned%20vaccination%20progress.PNG "Vaccination Progress")

As we can see that there are some missing values in datasets. Therefore, before plot the datas into time-series line chart, we need to clean the datas. In this case, to `predict` the missing values, we can interpolate the total number of vaccinated people of each country by the its defined time shown in Figure below.

![skewed linechart](https://github.com/akbarnotopb/portofolio/blob/main/Data%20Science/EDA/covid-resources/cleaned%20vaccination%20progress.PNG "Vaccination Progress")

From the chart above, we can infer that : 
1. There are 4 `highest number` vaccinated country that is visually distinct from others (people vaccinated). 
2. As per date ( 6 feb 2021 ), the highest number around 2.5M people, followed by two other country.
3. **Then, why are the progress of other country so slow? How can those 4 countries reach Millions Vaccinated people in just 2 months? How is their daily vaccination program?**

To answer those question, we need further processing such as `separation` as the are too many countries that had not reach 500K vaccinations. Let's take 10 highest and 10 lowest but excluding `zero` vaccinated country to see how are their progress (zero vaccinated country will always zero progress).

Here are the `10 highest` and `least 10` country. 

| No | 10 Highest |  10 Least |
| - | - | - |
| 1 | United States | Bangladesh |
| 2 | China | Andorra |
| 3 | United Kingdom | Greenland |
| 4 | England | Faeroe Islands |
| 5 | United Arab Emirates | Bermuda |
| 6 | Israel | Guernsey |
| 7 | Brazil |  Isle of Man |
| 8 | Germany | Jersey |
| 9 | France | Luxembourg |
| 10 | Italy | Iceland |


### How is their vaccination program? How is their daily number?
For simplicity, let's take 2 for each category. Highest 2 namely `United States` and `China` from `10 Highest` category and `Iceland`. Least 10 country `Luxembourg` from `10 Least` category. Their daily vaccination progress are shown in Figure below

![Vaccinations Progress](https://github.com/akbarnotopb/portofolio/blob/main/Data%20Science/EDA/covid-resources/daily%20vaccination%20number.PNG "10 Ranked Vaccination Progress")

From the chart above, we can infer that:
1. The 2 highest vaccinated country started its vaccinating program earlier, meanwhile `Luxembourg` and `Iceland` started at the end of 2020
2. Both `United States` and `China` vaccinating program increasing linearly, but `Luxembourg` and `Iceland` stuck at 1000 people each day and tends to slow down
3. All countries except `Luxembourg` uses 2 type of vaccines, and two vaccince type increase the daily vaccination number.

## Summary
Well yeah, there aren't much meaningful datas except how each country progress their vaccination based on this raw data. But here are some insight that can be infered from this quick analysis as per date ( 6 Feb 2021 data)

1. `United States` is the country that does the most vaccination, followed by `China`.
2.  Most country using only one type of vaccine so far (will be updated about the precentage of vaccine type used).
3. `Pfizer/BioNTech` is the most common vaccine type used, `61 out of 78` countries use this vaccine type.
4. Further Data Engineering and Data Analysis might be required to gain deeper knowledges, such as when each country will achieve herd immunity ( 70% people fully vaccinated ) 
