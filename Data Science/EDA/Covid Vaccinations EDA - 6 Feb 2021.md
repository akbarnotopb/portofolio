# Quick Overview of Covid Worldwide Vaccination
Here are some quick Covid-19 Worldwide Vaccination Exploratory Data Analysis. The datas used in this EDA are available [Online](https://www.kaggle.com/gpreda/covid-world-vaccination-progress, "Kaggle Covid 19 Wolrd Vaccination Progress"). The datasets itself are updated regularly. In our scenario, we will use the latest version ( 6 February 2021 ).

## Data Description
As per date, there are `8 vaccine types` used in `78 countries`. Some country only rely on one type but there is one country that is three types of vaccine. `Pfizer/BioNTech` is the most used wordwide followed by `Oxford/AstraZeneca` as shown in figure below.

![vaccine type](https://github.com/akbarnotopb/portofolio/blob/main/Data%20Science/EDA/covid-resources/vaccine%20type%20used%20and%20its%20country%20count.PNG "Vaccination Type")


## Vaccination Progres
### How vaccinations are progressing around the globe?
The vaccination progres of each country shown in figure below.

![skewed linechart](https://github.com/akbarnotopb/portofolio/blob/main/Data%20Science/EDA/covid-resources/uncleaned%20vaccination%20progress.PNG "Vaccination Progress")

As we can see that there are some missing values in datasets. Therefore, before plot the datas into time-series line chart, we need to clean the datas. In this case, to `predict` the missing values, we can interpolate the total number of vaccinated people of each country by the its defined time shown in Figure below.

![skewed linechart](https://github.com/akbarnotopb/portofolio/blob/main/Data%20Science/EDA/covid-resources/cleaned%20vaccination%20progress.PNG "Vaccination Progress")

From the chart above, we can infer that : 
1. There are 4 `highest number` vaccinated country that is visually distinct from others. 
2. As per date ( 6 feb 2021 ), the highest number around 2.5M people, followed by two other country.
3. **Then, why are the progress of other country so slow? How can those 4 countries reach Millions Vaccinated people in just 2 months? How is their daily vaccination program?**

To answer those question, we need further processing such as `separation` as the are too many countries that had not reach 500K vaccinations. Here are the `10 highest` and `least 10` country. 

![10 Highest ranked linechart](https://github.com/akbarnotopb/portofolio/blob/main/Data%20Science/EDA/covid-resources/top%2010%20cleaned%20vaccination%20progress.PNG "10 Ranked Vaccination Progress")

![10 Lowes ranked linechart](https://github.com/akbarnotopb/portofolio/blob/main/Data%20Science/EDA/covid-resources/least%2010%20cleaned%20vaccination%20progress.PNG "10 Ranked Vaccination Progress")

### How is their vaccination program? How is their daily number?
