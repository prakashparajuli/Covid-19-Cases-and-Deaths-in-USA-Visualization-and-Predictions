# Predicting-Covid-19-Cases-and-Deaths-in-USA
![covid](https://user-images.githubusercontent.com/66859479/123895655-c78f3280-d925-11eb-877f-4f43ab72baa0.png)
## Objective
Coronavirus disease 2019 (COVID-19) is an infectious disease caused by severe acute respiratory syndrome coronavirus 2 (SARS-CoV-2). It was first identified in December 2019 in Wuhan, China, and has resulted in an ongoing pandemic till date. Some early reports suggested that virus may have been transmitted from animal to person, however the extent and modes of transmission are not completely understood yet. Since the beginning of 2020, the world is going through a difficult time and fighting with this deadly virus, almost all the regions of the world have been shut down for numerous months and among all, USA is the hardest hit country. As a result of scientific advancement, we are able to develop a vaccine within a year of start of a pandemic, however the various aspects of the virus such as the extent and means of transmission, effect on the human health, immunity developed on the humans after the infection and many more are still unclear. Hence, as a data scientist, I aim to explore the available data (confirmed cases and death) of the covid-19 and their relationship to the additional aspects of the virus transmission such as population density of the area, mass gatherings (holidays celebration and protests) and the effectiveness of the various mitigation efforts implemented by the administration such as stay at home order and shutdowns of the restaurants and bars.
In particular, I will analyze the county-level data of Illinois state since outbreak to Jan 31, 2021 and build a robust model to predict the new cases and deaths in the particular county for the future 14 days (Feb 1 to Feb 14).  
## Who Might Be Benefitted
These predictions will guide the corresponding authorities in advance to prepare early and deploy the appropriate health care services to the area to save the lives. Hence, all the national and international regulatory agencies such as WHO, CDC, United States Department of Health and Human services are directly benefitted. Indirectly all the businessman and general public will be benefitted as these predictions help to plan the activities in advance.

## Datasets
In this project, I am using multiple datasets related to Covid-19, namely:
1. **Covid-19 Cases and Deaths** obtained from _The New York Times_ Github page.
2. **Climate Data** obtained from _National Center for Environmental Information_.
3. **People's Mobility Data** obtained from _U.S. Department of Transportation_.
4. **Public holidays, Various events and Covid-19 mitigation efforts** obtained from _Various federal and state regulatory bodies_.   

## Summary
Data was cleaned, outliers and missing values were imputed by 7 day moving average. 3-day moving average were used for modelling to remove the high noises. All the datasets were merged and additional features such as whether the day was a public holiday, travel banned or not, Days since events and many more. Performed various inferential statistics to check whether the various events has ciontributed for the surge in cases or not. Finally, various supervised machine learning algorithms: ARIMA, SARIMAX, LSTM, Prophet,XgBoost,and LGBM were tested and final model was obtained after hyperparameter tuning. Both XgBoost and ARIMA model perormed well having mape < 0.15, I choose XgBoost considering it's high performance in capturing the trends.
### Key Findings:
1. All the sources of data contributed to the predictive power of the model; top factors affecting the cases are Days since outbreak, lag_14 cases and whether or not stay home order is inmplemented.
2. Among the various supervised models, XgBoost performed well.
3. Inferential analysis shows that the some of the public events/gatherings contributed for the case surge, however this surge is partly linked with the natural spread of the virus as well.
4.   As illustrated below result shows that the cases and deaths are not declining rather slightly increasing for the next 14 days, hence precautionary measures should be adopted.

![Forecast_cases](https://user-images.githubusercontent.com/66859479/121266623-7341e700-c880-11eb-8b98-7d2893047120.JPG)


## Further Readings
[Full Project Report](https://drive.google.com/file/d/1aPhnixqb1y4sKsbKOMXArOQ48s1he9w2/view?usp=sharing)



