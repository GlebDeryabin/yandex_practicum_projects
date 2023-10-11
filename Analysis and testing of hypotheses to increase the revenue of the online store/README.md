# Analysis and testing of hypotheses to increase the revenue of the online store

**Description:** The project consists of two parts:
* prioritization of hypotheses prepared jointly with the marketing department using ICE and RICE methods;
* analysis of the results of the conducted A/B test.

**Objective:** select a hypothesis for testing and evaluate the test performed.

**Tasks:** 
* **Part 1**
0. Check the input data
1. Prioritization of hypotheses on ICE
2. Prioritization of RICE hypotheses
3. Analysis of the results
* **Part 2**
0. Check the input data
1. Build and analyze graphs of cumulative revenue, average receipt, relative change of cumulative average receipt, cf. number of orders per visitor, edit. cf. number of orders by groups and analyze them.
2. Build a dot graph of the number of orders by users.
3. Calculate percentiles and build graphs on the number of orders per user and their cost. Select boundaries to identify abnormal orders.
4. Calculate the statistical significance of differences in the average receipt and the number of orders per visitor based on raw and purified data. Analyze the results.
5. Make a decision based on the test results and give a recommendation to the business.

**Description of the source data:**
* The hypothesis.csv file contains a description of hypotheses and calculated parameters Reach, Impact, Confidence and Efforts to evaluate hypotheses.
* The orders.csv file contains information about online store orders: unique number, user number, date, revenue and A/B test group.
* The visitors.csv file contains information about the attracted users of the online store. It stores the date of engagement, the A/B test group and the number of users in this group on that day.

## Conclusions on Part 1

When using different methods of prioritization of hypotheses, the leaders for testing changed: compared to ICE, hypothesis 8 dropped out of the leaders, 7 went up, 0 remained, 2 entered the leaders. This was due to the fact that the RICE methodology takes into account the Reach parameter - user coverage. Hypothesis 8 "Launch a promotion that gives a discount on a product on a birthday" is good from the point of view of confidence in it and influence on users, but it covers a very small proportion of users and at the same time requires an average amount of resources, therefore, according to the RICE method, it came down from the top places. Hypothesis 7 took the first place, it was helped by the fact that its implementation will affect absolutely all users.

I would recommend checking hypothesis 7 first of all, "Add a subscription form to all the main pages in order to collect a customer base for email newsletters," since it is in the lead in both methods, and according to the RICE method, it is twice as far from the next one.

## Conclusions on Part 2

* There is a statistically significant difference between groups A and B in the average number of orders per visitors, the conversion from visitor to buyer for group B is 17% more. Confirmed on data before and after filtering
* There is no statistically significant difference between groups A and B on the average check. The p-value is significantly higher than the critical level on both raw and filtered data. According to the filtered data, the relative difference of the average check B to A is -2%, that is, almost 0.
* The graph of the relative change in the average number of orders of group B to A shows consistently better results of Group B.

Based on the facts described, I recommend stopping the A/B test and recognizing it as successful. As a result of testing the hypothesis, the average number of orders per user increased by 17%, and the average receipt remained approximately the same. If this was the purpose of the hypothesis, then it has been successfully tested and I recommend implementing it for all users.