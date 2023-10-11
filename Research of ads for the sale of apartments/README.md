# Research of ads for the sale of apartments

Archive of ads for the sale of apartments in St. Petersburg and neighboring settlements for several years. The task is to study the parameters that determine the cost of the object. 

Two types of data are available for each apartment for sale. The first ones are entered by the user, the second ones are obtained automatically based on cartographic data. For example, the distance to the center, airport, nearest park and reservoir.

# General conclusions

The purpose of the study of ads for the sale of apartments in St. Petersburg and other cities is to establish parameters for an automated system for assessing market value, detecting anomalies and preventing fraud.

There are 23699 rows in the provided dataset, of which about 5000 are missing. The data needed preprocessing: missing values were partially filled in, data types were changed, duplicates and anomalies were excluded. The conclusions for each of the actions and the possible reasons for the omissions are indicated in the interim conclusions.

New parameters have been added to investigate the data:the price of one square meter, the day of the week, month and year of publication of the ad, the type of floor of the apartment, the distance to the city center in kilometers.

The main characteristics of housing and their distribution are studied. The most common object: an apartment of up to 75 sq.m., worth about 5 million rubles, 1-2 rooms, ceiling height - 2.6 m, located not on the extreme floors, located 10-20 km from the center and 20 from the airport. The announcement is published on weekdays.

The speed of the sale of the object has been studied. The average time of sale is 180 days, the median is 95 days. A quick sale can be considered a time of up to 4 weeks, a protracted one - from six months. 

It has been studied how some parameters affect the cost of an apartment. The data confirmed the obvious statement that cost is a complex complex parameter that is simultaneously influenced by various factors. There is a direct linear dependence of the average crowding (k=0.6-0.76) between the cost and the area, it does not depend on the n.p. or the distance to the center. There is a direct relationship between the number of rooms (up to 7) and the cost. Apartments on the 1st floor are significantly cheaper. The cost almost does not depend on the day and month of placement. There is a dependence on the year, but not obvious.

The average cost of sq.m. 10 n.p. with the largest number of ads is determined. The most expensive meter in St. Petersburg and Pushkin, the most affordable - in Vyborg and Vsevolozhsk.

The price of sq. m. in St. Petersburg is investigated depending on the distance from the center. Obviously, the most expensive apartments are in the center, while the cost within 8 km does not depend on the distance. From 9 to 29 km, the cost of sq.m. is evenly reduced.

To create an automated system, you can use the established average values and normal ranges of parameters, the following parameters should be used together to estimate the cost: total area, number of rooms, n.p., distance from the center, floor. To create a more accurate model, I would recommend adding information to the data about: type of house, year of construction, distance to infrastructure facilities (school, metro, parking, ...), area, repair, type of property. 

To improve the data collection system: make the fields mandatory, select the address of the object by specifying the structure on the map (or confirm in this way). Check the work of the automated cartographic part - a lot of omissions.