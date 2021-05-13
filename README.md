# autolib_coreweek4
autolib is an electric sharing company. there are bluecats, utilib and itilib_14 vehicles in 860 stations and 4,400 parking spaces. users can pick or drop of the available 3000 cars. the Bollore gropu wishes to expand the european market. this brings up the need to verify the measures and conditions put in place in paris for even distribution of all the cars, stations and parking spots are effecive before moving on to other regions. research and feedback on the following will allow the group to make informed choices;

on any given weekday, the aveage number of vehicles taken is more than the average number of vehicles returned

on any weekday, the number of bluecars taken is more than the total number of both utilib and utilib/-14 ars taken

the number of cars taken from postal code 75015 is eqyal to the number of cars taken from 75017

##importing libraries, loading and describing our data
import pandas as pd
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt
from scipy import stats

url = 'http://bit.ly/DSCoreAutolibDataset'
df = pd.read_csv(url)
df.head(1)

df = pd.read_csv(url)
print("The data set has {}rows and {}columns".format(df.shape[0], df.shape[1]))
display(df.describe())
display(df.head(2))
display(df.dtypes.value_counts())

##data cleaning
###finding and removing any null values
df.isnull()
df.dropna(inplace=True)
###removing any duplicates
###findig and dealing with outliers

##univariate analysis
histogram for distribtuion of blue cars taken
histogram of nlue cars returned
histogram of utilib cars taken and returned
barcahrt for utilib_14 cars taken and returned

##bivariate analysis
"number of blue cars, utilib and utilib_14 cars taken" chart
scatter plot for all cars taken

##hypothesis testing
###hypothesis 1: on any weekday, the average number of bluecars, utilib and utilib_14 cars taken is higher than the average number returned
###hypothesis 2: on any weeday, the number of bluecars taken is more than the total number of utilib nad utilib_14 cars
###hypothesis 3: number of vehicles taken in postal code 75015 is equal to the number of cars taken from postal code 75017
