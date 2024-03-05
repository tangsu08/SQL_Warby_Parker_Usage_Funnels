# Questions and Answers

## Part 1: Quiz Funnel 

### 1. First, let's get an idea of what response choices there are for each question in the survey. 
![alt text](/images/sql_script/1.response_choices_per_survey_question.png)

##### Result: 
<img src=images/sql_solutions/2.unique_responses_per_question.png width="400" height="350">

### 2. Users may "give up" at different points in the survey. Let's analyze how many users move from Question 1 to Question 2, etc. What is the number of responses for each question?
![alt text](/images/sql_script/2.survey_funnel_conversion.png)

##### Result: 
<img src=images/sql_solutions/1.funnelgroups.png width="400" height="125">

### 3. Calculate the percentage of users who answer each question (i.e., what is the completion rate as we move through the survey questions?). Which questions have a lower completion rate, and what may be the reason(s)? 
![alt text](/images/sql_script/2b.completion_rate_persurveyq.png)

##### Result: 
<img src=images/sql_solutions/3.completion_rate_persurveyq.png width="525" height="105">

**Question three and question five have lower completion rates.** Question three asks respondents which shapes (of glasses) they like. One reason for a lower completion rate is **cultural/demographic factors**: preferences for shapes could vary based on cultural or demographic factors and if the options provided do not resonate with certain groups of users, it could lead to lower completion rates. Another reason could be **privacy concerns**: some respondents may feel uncomfortable sharing their preferences for shapes, especially if they perceive the information as potentially revealing or sensitive in some way. This could lead them to skip the question.  

Question five asks respondents when their last eye exam was. One reason could be due to **fatigue/disenagement**: respondents may lose interest as they progress through the survey, resulting in lower completion rates for questions toward the end of the survey. Another reason may be due to **embarrassment**: some respondents may feel embarrassed disclosing the length of time since their last eye exam, especially if it has been a long time.

### 4. What are the most common result(s) of the style quiz overall? By question? 
#### Overall

![alt text](/images/sql_script/7.most_common_results_of_style_quiz.png)

##### Result: 
<img src=images/sql_solutions/8.common_quizresponses_across_board.png width="500" height="180">

The most common survey response was men's style glasses with a narrow fit, in a rectangular shape and tortoise color. Interestingly enough, following were similar results but for women's style glasses - narrow fit, in a rectangular shape, and either tortoise or black color.

#### By question

![alt text](/images/sql_script/8.most_common_results_of_quiz_byquestion.png)

##### Result: 
<img src=images/sql_solutions/8b.most_common_response_byquestion.png width="450" height="300">

Looking at the most common response per question, a similar amount of respondents were seeking for women's styles and men's styles. Narrow fit is the most popular fit choice, and rectangular the most preferred shape. Tortoise was the most popular color choice, though followed closely by black. 

## Part 2: Purchase Funnel

### Now let's shift our attention away from Warby's quiz funnel and towards their purchase funnel. Warby's purchase funnel consists of: Take the style quiz > Home try-on > Purchase the perfect pair of glasses. During the Home try-on stage, we will be conducting an A/B Test:  
* #### a. 50% of users will get _3_ pairs to try on
* #### b. 50% of users will get _5_ pairs to try on

### Are users who get more pairs to try on at home more likely to make a purchase?    

### 1. First create a table where we can see each user's purchase funnel. We want to understand whether or not the user tried on a pair of glasses at home, how many number of pairs they tried on, and whether or not they purchased the glasses. Limit to the first 10 rows. 
![alt text](/images/sql_script/3.purchase_funnel_by_user.png)

##### Result: 
<img src=images/sql_solutions/4.purchase_funnel_per_user.png width="500" height="200">

### 2. Calculate overall conversion rate (e.g., what percent of respondents completed all steps of the funnel?). 
![alt text](/images/sql_script/4.overall_conversionrate_purchasefunnel.png)

##### Result: 
<img src=images/sql_solutions/5.overall_conversionrate_purchasefunnel.png width="600" height="50">

### 3. Calculate conversion rates for each step of the purchase funnel, and compare conversions. 
![alt text](/images/sql_script/5.conversions_across_funnelsteps.png)

##### Result: 
<img src=images/sql_solutions/6.conversion_rate_across_funnelstep.png width="830" height="40">

As we move down the purchase funnel, conversion rates slightly drop. 75% move on from the style quiz to home try on, though this drops to 66% who move from home-try-on to purchasing glasses. 

### 4. What are the conclusions of the A/B test? Were users who got more pairs of glasses to try on at home more likely to make a purchase? Calculate the difference in purchase rates between those who got three vs. five pairs of glasses to try on. 
![alt text](/images/sql_script/6.comparing_purchase_rates_abtest.png)

##### Result: 
<img src=images/sql_solutions/7.abtest_purchase_conversion_comparison.png width="850" height="65">

Users who received more pairs of glasses to try on at home were more likely to make a purchase than those received fewer pairs (79% vs. 53%, respectively) - a 26% difference! 

### 5. How many purchase options are there? What are the different purchase combinations? 
#### Number of purchase options
![alt text](/images/sql_script/12.total_purchase_combinations.png)

##### Result: 
![alt text](/images/sql_solutions/10._unique_purchaseoptions.png)

#### Purchase Combinations
![alt text](/images/sql_script/13.purchase_combinations.png)

##### Result: 
<img src=images/sql_solutions/10b.unique_purchase_optionlist.png width="650" height="280">

### 6. What were the most common types of purchases made overall? By women's styles vs. men's styles? 
#### Overall 
![alt text](/images/sql_script/9.most_common_purchases_made_overall.png)

##### Result: 
<img src=images/sql_solutions/9.common_purchases_made.png width="650" height="280">

#### By Women's Styles 
![alt text](/images/sql_script/11._common_purchases_made_by_women.png)

##### Result: 
<img src=images/sql_solutions/9c.common_purchases_women.png width="620" height="150">

#### By Men's Styles
![alt text](/images/sql_script/10.common_purchases_made_by_men.png)

##### Result: 
<img src=images/sql_solutions/9b.common_purchases_men.png width="600" height="180">

### 7. How accurate was the style quiz in determining a user's purchase? In other words, did the answers that users selected in the style quiz align with what they ended up buying (or not buying)? 
