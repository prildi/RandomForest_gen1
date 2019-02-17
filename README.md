# RandomForest_gen1
A simple random forest weather generator in R

## What is a Weather Generator?

With a Weather Generator you can generate synthetic time series of a particular site. If you run the generator twice, you will get different time series but with the same statistical characteristics. For more information  see  <https://www.ipcc-data.org/guidelines/pages/weather_generators.html>.

## What is this Weather Generator about?

This is the first part of the development of a Weather Generator in R. It focuses just on the temperature values.

For second part, combining different meteorological parameters, see :

For third part, applying a detrending and trending, see:

For forth part, adding the multi site component, see here:


Presumed, we have a time series of temperature values of a particular site. There are many applications, like impact modelling, we cannot trust or rely on a relativly short time series of like 30 or 50 years. Maybe we need 100 or 1,000 or even more years, to make sure for instance a building or tree to built or construct resists the climatic conditions. At this point, Weather Generators enter the game.


## A simple random Forest weather generator 1st gen

At first, we need read to the data, which I prefer to do with the data.table library:

```{r read data}
library(data.table)
temp<-setDF(fread("https://raw.githubusercontent.com/rkronen/Brook90_R/master/Input_data/fixed.txt"))
```


