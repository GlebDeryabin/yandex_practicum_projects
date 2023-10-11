# A/B testing

**Project Description:** Using data on marketing companies, conducted tests, users and logs to investigate the a/b test associated with the implementation of an improved recommendation system of the store, and test the working hypothesis.

**Purpose:** To evaluate the correctness of the test according to the TOR and analyze its results.

**Tasks:**
- Explore the data:
    - Is type conversion required?
    - Describe the nature of the missing values and duplicates, if any.
- Evaluate the correctness of the test
    - Compliance of the data with the requirements of the terms of reference.
    - The time of the test.
    - Test audience. 
- Conduct a research analysis of the data:
    - Are the number of events per user equally distributed in the samples?
    - How is the number of events in the samples distributed by day?
    - How does the conversion rate in the funnel change in the samples at different stages?
    - What features of the data should be taken into account before starting A B-testing?
- Evaluate the results of A/B testing
- What can we say about the results of A/B testing?
    - Check the statistical difference between the fractions by the z-criterion.
- Describe the conclusions on EDA and A/B testing. Make a general conclusion about the correctness of the test.

**Initial data:**
- ab_project_marketing_events.csv — calendar of marketing events for 2020
- final_ab_new_users.csv — users registered from December 7 to December 21, 2020
- final_ab_events.csv — actions of new users in the period from December 7, 2020 to January 4, 2021
- final_ab_participants.csv — table of test participants.

**Terms of Reference**
- Test name: `recommender_system_test`;
- groups: A — control, B — new payment funnel;
- launch date: 2020-12-07;
- date of stopping the recruitment of new users: 2020-12-21;
- stop date: 2021-01-04;
- audience: 15% of new users from the EU region;
- purpose of the test: testing of changes related to the implementation of an improved recommendation system;
- expected number of test participants: 6000.
- expected effect: in 14 days from the moment of registration, users will show an improvement in each metric by at least 10%:
- conversions to viewing product cards — the `product_page` event,
    - basket views — `product_cart`,
    - purchases — `purchase'.

# General conclusions

As a result of working on the project:
1. The initial test data is checked for compliance with the technical task. The basic requirements are met, but:
    * users who participated in other tests have been detected
    * marketing activities were carried out during the test
    * a significant discrepancy was found in the number of average actions per person between subgroups in favor of group A
2. A research analysis of the data was carried out, which showed the uneven distribution of the absolute number of actions between groups A and B, as well as by day (due to the uneven influx of users into the test). Funnels for groups A and B are constructed. In group B, the conversion of logins to product views decreased, the level of payments from product views remained the same. The conversion of active users to buyers has also decreased.
3. Hypotheses about equality or growth of conversions of active users in product views, shopping carts and purchases have been tested:
    * Conversion to viewing products in Group B decreased by 9%, and this is statistically significant.
    * The change in conversions to shopping cart views and purchases between groups is not statistically significant.
The effect of the introduction of the recommendation system turned out to be negative.
4. There are many questions about the test data, research on them can lead to incorrect conclusions.

Recommended:
1. Postpone the introduction of the recommendation system.
2. Conduct the test again with a period that does not overlap with seasonal phenomena, holidays and marketing activities. Follow the similarity of the participating users.