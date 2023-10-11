# Formation of a mobile game monetization model

# Materials

[Link](https://drive.google.com/file/d/1KJy2YXMHvb_pCWTs41xrZ_cp_LbCd6l0/view?usp=share_link) to the presentation with research conclusion

[Link](https://public.tableau.com/views/Book3_16801811305550/sheet2?:language=en-US&publish=yes&:display_count=n&:origin=viz_share_link) to the dashboard

**Project Description:** Developers have launched a mobile game "Space Brothers". In it, users build their space program and try to succeed in the difficult task of colonizing the galaxy. The first users are already playing, and their involvement is working. However, the main monetization of the game has not yet been implemented: it is assumed that this will be an ad display on one of the screens. There is a contradiction in such mechanics: if you show ads early, the user may get angry and leave, if it's late, the fewer players will remain and will bring developers less money. The analyst is faced with the task of choosing the optimal time for displaying ads. Solution requirements: advertising should pay for attracting users after they reach the first level, the amount of advertising should be minimal.

**Objective:** based on the minimum payback of attracting players, determine the optimal time to display in-game advertising.

**Hypotheses:**
1. The time of passing a level between players who implement a project or defeat a player to move to the next level is equal or different
2. The number of buildings does not depend on the style of the game, which means that builders and warriors will see the same amount of advertising

**Tasks:**
1. Upload and pre-process data
    1. Data types
    2. Duplicates
    3. Omissions
    4. Anomalies
    5. The horizon of analysis (leave up-to-date data)
6. Correction of the date of purchase of advertising (purchase is a day ahead of attraction)
2. Conduct a research analysis of the data
    1. What affects the target event "The player has moved to a new level"?
        1. Connection of the transition to a new level and the date of user engagement
        2. Connection of the transition to a new level and the channel of user engagement
        3. The connection between the transition to a new level and the number of objects built
        4. Connection of transition to a new level and types of constructed objects
        5. The connection of the transition to a new level and the type of game - builder or warrior
2. Which event should I choose to display ads?
        1. calculation of the cost of attracting users by cohorts
        2. the number of events in the dataset, broken down by different users and cohorts
        3. calculation of the estimated revenue from ad impressions at the rate of 0.07 yandex units per impression
        4. selecting events to display ads
3. Test statistical hypotheses
    1. Prepare the data
    2. Choose the right test and check if an amendment is needed
4. Formulate conclusions and recommendations, prepare a presentation

**Initial data:** The source data is provided by the developers and contains 3 tables:
* game_actions.csv with logs of in-game events about buildings, projects and level completions, types of buildings
* ad_costs.csv with information about advertising activities: day, traffic source, cost of clicks
* user_source.csv with information about users and sources of their attraction

**Form of presentation of results:** based on the results of the study, prepare a presentation justifying the choice of the optimal monetization model of the game in pdf format

# General conclusions

As a result of working on the project:
1. The factors accompanying the achievement of the target event - the passage of the first level are investigated:
    1. On average, the passage of the level takes 11 days, the proportion of players who have completed the level is 0.42. It is recommended to compare the duration of passing the level with other mobile games
    2. With an increase in the date of attracting users, the proportion of those who have completed the level decreases. The budget is unevenly distributed, and perhaps new players have no one to play with. It is recommended to check that the type of attracted users has not changed.
    3. The completion time of the level and the percentage of completed players does not depend on the attraction channel. The number of buildings and their types also differs slightly.
    4. Warriors complete the level faster (11 days) and have fewer buildings (9.4) than builders (almost 14 days and 12.6 buildings).
2. A basic monetization model is proposed: Advertising on the screen of all buildings, except the first one for each player. With this model, the users who participated in the study pay off and make a profit of 403.02 cu.
3. Two hypotheses have been tested and refuted, in fact:
    1. The time of passing the level by warrior players and builder players differs
2. The average number of buildings between warrior players and builder players differs

Recommended:
1. Estimate the average time to complete a level and compare it with other games
2. Check that the parameters of the attracted people have not changed and the decrease in the share of past levels is due to the number of players.
3. Imitatively deploy the basic model for a part of users (not to show ads, but to calculate revenue). With the actual implementation of the model, it is necessary to take into account the possible drop in user retention.