
-  Dear reader,

The goal of this assignment is to encapsulate our PostgreSQL database using Python, and we have made our best effort to achieve this. 

In the following analysis we aim to identify the determinants of movies' sales.
This research enhances the understanding of movie studios, distributors or marketers about when to release a movie in reality. Moreover, we aim to give  recommendation for developers in how they should schedule their new releases, improve on marketing strategies and above all greatly help reduce production costs.
Note: There is still little evidence on temporal effects in the film industry. 

The conducted research followed the objectives below:

- To analyze the impact of movie release dates on domestic box office revenue. 

- To identify the months that generate the highest average box office returns. 

- To assess the effect of holiday season releases on opening weekend performance. 

- To examine the relationship between user review scores and box office revenue across different release periods.

  In order to meet these objectives we came up withe the research question "How does the release date of the movie influences the domestic box office performance and reviews?" in divided it into subquestions amd formulated corresponding hypothesis:
1. Which release months generate the highest average box office revenue? - Hypothesis 1 (H1): Movies released during the holiday season generate higher average box office revenue than those released during non-holiday seasons.
2. How does releasing a movie during the holiday season impact its opening weekend performance? Hypothesis 2 (H2): Movies released during the holiday season achieve significantly higher opening weekend performance compared to non-holiday releases.
3. What is the correlation between user reviews (user scores) and box office revenue for movies released in various months?	Hypothesis 3 (H3): There is a positive correlation between higher user review scores and box office revenue for movies.
4. What is the correlation between metascore and box office?	Hypothesis 4 (H4): There is a positive correlation between expert review scores and box office revenue for movies.

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

Moreover, we carried out a series of linear regression studies to explore the impact of holiday season releases, ratings from user reviews, and evaluations from experts on the domestic box office earnings. The factors that were considered independent were the date a movie was released (during the holiday season versus outside of it), ratings from viewers, and assessments from critics. The domestic box office earnings were the factor that was measured as dependent.

 Summary of Findings
1.	Hypothesis 1 (H1): accepted. Movies released during the holiday season generated higher average box office revenue compared to those released in non-holiday periods.
2.	Hypothesis 2 (H2): Partially accepted. Some holiday releases outperformed non-peak releases in terms of opening weekend performance, but others did not.
3.	Hypothesis 3 (H3): Not accepted. There was no significant correlation between user review scores and box office revenue.
4.	Hypothesis 4 (H4): Not accepted. There was no significant correlation between expert review scores and box office revenue.

The regression analysis confirmed that holiday season releases, user reviews, and expert reviews were not significant predictors of box office performance when considered together.



