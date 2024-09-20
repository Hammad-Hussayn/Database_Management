Dear reader,

The goal of this assignment is not only to encapsulate our PostgreSQL database using Python but by also using postgresql and python to provide visual statistic representation of the variables and the relationship both independent variable (release date) have on independent variable (box office performance and reviews) they have with one another and understand what the results of the data entails, and believe we have made our best effort to achieve this. 

In the following analysis we aim to identify the determinants of movies' sales.
This research enhances the understanding of movie studios, distributors or marketers about when to release a movie in reality. Moreover, we aim to give  recommendation for developers in how they should schedule their new releases, improve on marketing strategies and above all greatly help reduce production costs.
Note: There is still little evidence on temporal effects in the film industry. 

The conducted research followed the objectives below:
- To analyze the impact of movie release dates on domestic box office revenue. 
- To identify the months that generate the highest average box office returns. 
- To assess the effect of holiday season releases on opening weekend performance. 
- To examine the relationship between user review scores and box office revenue across different release periods.

In order to meet these objectives we came up withe the research question "How does the release date of the movie influences the domestic box office performance and reviews?" in divided it into subquestions amd formulated corresponding hypothesis:
1. Which release months generate the highest average box office revenue in peak seasons? - Hypothesis 1 (H1): Movies released during the holiday season(such as valentines, christmas and halloween generate higher average box office revenue than those released during non-holiday seasons.
2. How does releasing a movie during the holiday season impact its opening weekend performance? Hypothesis 2 (H2): Movies released during the holiday season achieve significantly higher opening weekend performance compared to non-holiday releases.
3. What is the correlation between user reviews user scores and box office revenue for movies released in various months?	Hypothesis 3 (H3): There is a positive correlation between higher user review scores and box office revenue for movies.
4. What is the correlation between metascore and box office?	Hypothesis 4 (H4): There is a positive correlation between expert review scores and box office revenue for movies.

DATA ANALYSIS
Next step was testing the hypothesis.
•Test 1 (t-test average box office earnings during holiday vs. non-holiday periods) 
Hypothesis 1 (H1): Movies released during the holiday season (e.g., December: 7,531,973) exceeded the average earnings of films released during the non-peak season (6,797,050) H1: The evidence suggests that films released during the holiday season generate the highest box office earnings.
![image](https://github.com/user-attachments/assets/aacf68ee-3758-4715-ad2c-94392677ed5a):

Conclusion: this diagram shows that December during the peak period of 21-30th generates the most average domestic box office revenue.

H2 Hypothesis 2 (H2) The performance of films on their opening weekend was varied. However, February still achieved higher average opening weekend earnings (2,012,258) compared to films released during non-peak periods (1,979,325), while December and October saw lower average earnings (1,833,857 and 1,227,013, respectively). Therefore, it partially supports hypothesis 2.

![image](https://github.com/user-attachments/assets/388a2a5f-ea8d-4246-ab66-c1a202772999): 
Conclusion: The data suggests that February, the Non-Peak Season, and December are relatively strong periods for opening weekend revenue, while October may not be as lucrative for movie releases. Studios might consider avoiding October or using stronger marketing strategies to boost performance during this period.

Pearson correlation coefficients were used to assess Hypothesis 3 (H3) and Hypothesis 4 (H4):
Hypothesis 3 (H3): The correlation between user review scores and box office revenue was -0.00035, showing no significant positive relationship. H3 is not supported.

![image](https://github.com/user-attachments/assets/939fb9ae-69df-409b-9816-0c748e0edeb0): 
Conclusion: The data suggests that UserScore alone does not strongly predict Domestic Box Office revenue. Other factors beyond audience ratings likely play a more significant role in determining box office performance.

Hypothesis 4 (H4): The correlation between expert review scores and box office revenue was -0.017, which was also insignificant. H4 is not supported
![image](https://github.com/user-attachments/assets/3b9150c9-0670-48dc-b07f-c5ff77aca152): 
Conclusion: this diagram shows that December during the peak period of 21-30th generates the most average domestic box office revenue.

Moreover, we carried out a series of linear regression studies to explore the impact of holiday season releases, from user reviews, and evaluations from experts on the domestic box office earnings. The factors that were considered independent were the date a movie was released (during the holiday season versus outside of it), ratings from viewers, and assessments from critics. The domestic box office earnings were the factor that was measured as dependent.
 
REGRESSION ANALYSIS 
The regression analysis confirmed that holiday season releases, user reviews, and expert reviews were not significant predictors of box office performance when considered together.
Variables         	Coefficient  	Standard Error  	t-Statistic	p-value  
Intercept  	        6.191e+06	         1.08e+06        5.720    	0.000
Holiday Season    	1.952e+05	         1.17e+06	       0.167	    0.867
User Review Score  	2.298e+04	         9.45e+04	       0.243	   0.808
Expert Review Score|-3.09e+04   	     1.68e+04	      -1.843	   0.065

![image](https://github.com/user-attachments/assets/ac3d6a55-0073-4da0-adc4-01b8e5f07191)
Plot 1: Holiday Season vs Domestic Box Office
	• This diagram shows a scatter plot of movies released during holiday seasons (represented by 1) and non-holiday seasons (represented by 0) against the domestic box office revenue.
	•	Regression Line: The red line in the graph is essentially flat and close to zero, indicating that the variable holiday_season has little to no linear relationship with box office revenue. This suggests that the timing of movie releases during holiday seasons, at least in this analysis, does not predictably result in higher box office revenue.
	•	Conclusion: There is no significant difference in box office performance between holiday and non-holiday releases. Holiday releases alone are not a strong predictor of box office success.
 
 Plot 2: User Score vs Domestic Box Office
	•	This scatter plot visualizes the relationship between user review scores and domestic box office revenue.
	•	Regression Line: The green line is also nearly flat, indicating that there is no strong linear relationship between userscore and domestic_box_office. The data points are spread out, showing that movies with a wide range of user scores have variable box office revenues.
	•	Conclusion: Userscores do not appear to have a significant impact on box office revenue. Even movies with high user ratings can have low or high box office revenue, suggesting other factors are likely influencing box office performance.

Plot 3: Metascore vs Domestic Box Office
	•	The scatter plot illustrates the relationship between the critic metascore and the domestic box office revenue.
	•	Regression Line: Similar to the other plots, the blue line is close to zero, indicating no significant linear relationship between metascore and domestic_box_office. Movies with metascores across the spectrum (from low to high) have varying box office performances, further emphasizing the weak connection between critic scores and revenue.
	•	Conclusion: The metascore has minimal impact on predicting box office revenue. Even critically acclaimed movies (with higher metascores) do not necessarily generate more revenue than movies with lower metascores.


