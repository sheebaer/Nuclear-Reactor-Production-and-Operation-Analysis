# Nuclear-Reactor-Production-and-Operation-Analysis-

This is an analysis of data on Nuclear Reactors in USA. 
The data was taken from [data.gov][1]

[1]: https://www.data.gov/

## Objective

The aim is to analyse the said data and see if there is any interesting relationship between the production and duration of operation of nuclear power plants in the years for which data is available. Since data is available for 2008 and 2009, the effect of the recession on production in these years is also analysed.

## Data Preprocessing

First, all the variables that contained either redundant data or data that isn't very important were removed. 
Next the data was converted to a processable form.
  * All variables of type `datetime` were reduced to only the year since that is the most critical part of the date (for this purpose).
  * All categorical variables were converted to numbers using **Integer Encoding**.
  * Since the range of order of the numeric data was large, it was scaled to make sure that the analysis is not skewed. All the data was proportionally reduced to make sure all the values fall between 0 and 1.
  
## Data Visualisation and Analysis

First a **correlation matrix** was obtained for the data. This was analysed and the inference was noted. Some variables had very strong correlation. These variables have not been dropped, but can be dropped based on the nature of analysis.

Next, to analyse the relation between *Production* and *Duration of Operation* of the plants, a scatter plot was generated using the `seaborn` library between production in each of the years for which data was available and the duration of operation of the plant.
This led to insights on the effect of production during the recession years (2008-09) and some interesting observations.
  
  
