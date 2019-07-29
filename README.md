# Project-Forest-Fire-Prediction

Here "Project v2.ipynb" is main project file.

The objective of this project is to predict the probability of a forest area catching fire based on a number of meteorological factors such as temperature, wind speed, relative humility, FFMC, DMC, rainfall etc of the concerned area.
Every year, we lost at least 550 crores worth of resources due to unpredictable forest fires. This project aims at creating a Machine Learning model that shall be capable of improving its performance accuracy upon being provided with more experience in terms of new, relevant data.
The initial data is provided in the form of Forest Weather Index (FWI) which is made of surface observations at noon and represents fire danger at mid-afternoon. We see that FWI is composed of individual indexes that give information on specific details. The meaning of each sub-index is given as follows:
FFMC - This index classifies the moisture content of litter and other cured fine fuels, like needles or twigs less than 1 cm in diameter. FFMC is representative of the top litter layer 1-2 cm deep and has a short-term memory, only reflecting weather conditions that have occurred over the past three days. 
DMC - This index indicates the moisture content of loosely-compacted organic layers with a depth of 5-10 cm. DMC fuels have a slower drying rate than FFMC fuels and DMC may be used in predicting the probability of fire ignition by lightning. 
DC - This third moisture index reflects the moisture content of compact organic layers, 10-20 cm deep. DC is indicative of long-term moisture conditions and deep burning fires, being related to mop-up and patrol difficulties.
ISI - This index combines FFMC and wind speed, being a good indicator for fire spread. Moreover, if the topography is known, the slope effect on fire spread may be converted into a wind speed equivalent and added to the real wind speed.
BUI - This index is a weighted combination of the DMC and DC indexes and represents the total fuel available for the spreading of fire.

The data columns available to us while working on this project are as follows:
1.	X - x-axis spatial coordinate within the Montesinho Park map: 1 to 9
2.	Y - y-axis spatial coordinate within the Montesinho Park map: 2 to 9
3.	month - months of the year: "Jan" to "Dec" 
4.	day - days of the week: "Mon" to "Sun"
5.	FFMC - FFMC index from the FWI system: 18.7 to 96.20
6.	DMC - DMC index from the FWI system: 1.1 to 291.3 
7.	DC - DC index from the FWI system: 7.9 to 860.6 
8.	ISI - ISI index from the FWI system: 0.0 to 56.10
9.	temp - temperature in Celsius degrees: 2.2 to 33.30
10.	RH - relative humidity in %: 15.0 to 100
11.	wind - wind speed in km/h: 0.40 to 9.40 
12.	rain - outside rain in mm/m2 : 0.0 to 6.4 
13.	area - the burned area of the forest (in ha): 0.00 to 1090.84 (this output variable is very skewed towards 0.0, thus it may make sense to model with the logarithm transform)
Of the aforementioned variables, area i.e. the area affected by a past forest fire serves as the independent variable which is dependent on all variable expect X and Y which merely serve as a location indicator.

Based on this data, the steps taken for the successful completion of this project are:
1.	Cleaning of the available data, which includes:
a.	Identification and removal of all NaN values
b.	Removal of all outlaying values
2.	Removal of all non-contributing columns (here, X and Y)
3.	Creation of various models 
4.	Comparison of models to identify the best-fitting ML model
5.	Prediction on basis of new, foreign data

Citation: This dataset is public, available for research. The details are described in [Cortez and Morais, 2007]. 
P. Cortez and A. Morais. A Data Mining Approach to Predict Forest Fires using Meteorological Data. In J. Neves, M. F. Santos and J. Machado Eds., New Trends in Artificial Intelligence, Proceedings of the 13th EPIA 2007 - Portuguese Conference on Artificial Intelligence, December, Guimaraes, Portugal, pp. 512-523, 2007. APPIA, ISBN-13 978-989-95618-0-9. Available at: http://www.dsi.uminho.pt/~pcortez/fires.pdf
