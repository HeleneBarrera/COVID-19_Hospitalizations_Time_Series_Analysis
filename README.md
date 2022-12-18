# COVID-19_Hospitalizations_Time_Series_Analysis

The focus of this study is inpatient beds utilized daily in Texas during the Covid-19 pandemic (Jan 2021 - May 2022). The goal was to predict bed utilization taking patterns of Covid-19 into account through time series analysis. Ideally, a model such as this could be used for capacity planning in hospitals, to improve patient care and outcomes. 

The data consists of public datasets from heathcare.gov and the CDC. Variables such as deaths_from_covid and daily_vaccinations were explored. 

In total, 5 models were explored, starting with simple ARMA and ARIMA univariate models. The third model was a multivariate model with a leading variable. The added variables were Covid-19 beds utilized and Covid-19 vaccinations, with vaccinations as a leading variable and lagged by 16 days to account for the time needed to take effect and impact covid bed utilization. This type of model that takes the effect each variable has on the others into effect is called Vector Auto Regression (VAR). This model provided strong weekly seasonality and an overall shape to the model. 

The fourth model utilized a type of neural network called Multilayer Perceptron (MLP). The forecast did capture the overall shape of the data better than any other model, but failed to capture the strong seasonality of the other models. 

For the fifth model, I averaged the MLP and VAR models to form an ensemble model that combined strong points of both. The resulting model had the strong seasonality present in the original data, and larger trend line was accurate. 

