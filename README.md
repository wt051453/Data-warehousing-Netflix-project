Data-warehousing-Netflix-project

The Business/Organization & Opportunity: <br/>
Netflix is a subscription-based streaming service that allows its members to watch tv shows and movies without commercials on an internet-connected device (ref. netflix.com). There is an opportunity to optimize the selection of tv shows and movies for the business to increase member subscriptions and/or stock prices by analyzing the current lists of shows/movies, list of Netflix original shows/movies, the IMDB scores of the shows/movies and the stock prices data.

Problem: <br/>
The system helps us to find out what the most popular genre of movies/shows are in the current Netflix shows/movies selection; whether the popular videos align with high IMDB scores; whether Netflix originals have higher IMDB scores; and if there is a positive relationship between high score movies/shows to the stock prices.

Dimensional Model: <br/>
https://github.com/wt051453/ETL-in-data-warehousing-project/blob/main/dimensional%20model.pdf

Architecture Diagram: <br/>
https://github.com/wt051453/ETL-in-data-warehousing-project/blob/main/Architeture%20diagram.pdf

Detailed Design: <br/>
The datasets we found from Kaggle.com allow us to analyze and study the relationships between Netflix’s movies and shows selection to IMDB scores and their stock prices. For ETL steps, we chose to use python because it is one of the popular general-purpose programming languages that is capable of performing the tasks and the team is familiar with. We chose to run our data warehouse on MySQL server because it is a popular relational database management system that provides secure and fast data storage, fast query speed and the team is also familiar with it. Finally, we chose Tableau to create visualizations because it is a powerful visualization tool that offers ease of use and many visualization possibilities. Any future members to the team may already have experiences using these technologies or can easily pick up how to use them because there are many instructions or documentations available for these technologies which will significantly reduce the training time and cost.

ETL: <br/>

Final Schema: <br/>

Dashboard Application: <br/>

Connect Tableau to MySQL: <br/>
![image](https://user-images.githubusercontent.com/27581761/115129574-36125480-9fb5-11eb-8947-9657a84c5e9f.png)
<br/>
The analytics/visualization in the dashboard help answer the questions in the Problem section.

What the most popular genre of movies/shows are in the current Netflix shows/movies selection and whether the popular videos align with high IMDB scores? The answer is no, the most popular shows on the left don’t always correspond to high IMDB scores on the right. 
![image](https://user-images.githubusercontent.com/27581761/115129569-23981b00-9fb5-11eb-8c87-17904dbfa8d4.png)<br/>

Settings to create the visualization: from facts_imdb_rating table, I put the ‘Listed in’ to Rows as ‘Dimension’ and put Counts of ‘Listed in’ and Average of ‘Rating’ to the Columns and finally displayed the data in bar graph.


Conclusion: <br/>
The analytics built in Tableau using data transformed by the data source helped answer the problems we identified during the planning section and learned from data analysis that there are room to improve the movie/show selections in genres that received high IMDB rating, produce more high quality Netflix original movies/shows and increase movies/shows from countries that have higher than average IMDB ratings to attract more and retain existing subscriptions. <br/>

During this assignment, I got the opportunity to work on tasks that are practical and identical to real life project and it was a tremendous and valuable experience. I have learned how to figure out what directions to seek answers when I was stuck, effectively ask and follow-up with questions, perform researches (mostly online) using keywords and quickly acquired the necessary skillsets to solve various problems I ran into. I believe this will be beneficial for me as a Data Analyst or any other positions in the future. If I had to do it all over again, I would still be proactively getting involved in as much of the project as I could, working diligently with and motivating all the stakeholders.  

