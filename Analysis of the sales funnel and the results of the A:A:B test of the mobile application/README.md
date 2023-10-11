# Analysis of the sales funnel and the results of the A/A/B test of the mobile application for the sale of food

**Project Description:** using the data of event logs to build a sales funnel and determine the conversion between stages, identify the most problematic. Using the results of the A/A/B test to determine the results of testing the hypothesis about changing fonts in the application.

**Goal:** Find problem areas in the sales funnel and give a recommendation on the use of fonts based on A/A/B test.

**Tasks:**
1. Prepare the data for analysis
2. Examine and verify the data
3. Build and study the funnel of events
4. Study the results of the experiment

****Description of the source data:** the log_exp.csv dataset contains information about user actions - the name of the event, the user ID, the Time of the event and the experiment group.

# Conclusions

**During the implementation of the project:**
* The initial data were processed. Duplicates and an irrelevant time period were found. Their number was insignificant and bad data was deleted
* An event funnel has been built for the application. The conversion of users by MainScreenAppear -> OffersScreenAppear -> CartScreenAppear -> PaymentScreenSuccessful events is defined as 0.61, 0.81, 0.95.
* An A/A/B experiment was analyzed to test the hypothesis of the introduction of a new font. Groups A/A are recognized as identical, and the test was successful. Group B was compared by the proportion of unique users who reached the event with each group A and with the combined group AA. In all cases, the p-value was higher than the selected significance level and the hypothesis about the difference in the proportions could not be rejected.

**The main conclusions are formulated:**
* 47% of users who see the home screen reach a successful purchase.
* A bottleneck was found in the funnel of the application: a screen with suggestions. Only 0.62 users view it and continue to move towards a successful purchase. The conversion rate on the remaining steps is much higher.
* As a result of the analysis of the recognized A/A/B test, it was determined that there are no statistically significant differences in the proportion of unique users who reached the event between the groups. The font does not affect the reach of users to any of the stages in any way.

**Recommendations:**
* It is recommended to increase the conversion rate of the OffersScreenAppear event. Fix technical problems or make the action to call the screen more clear and explicit.
* It is recommended to leave the font as original and proceed to testing the following hypotheses.