# Questions and Answers

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
