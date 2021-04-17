Data-warehousing-Netflix-project

The Business/Organization & Opportunity: <br/>
Netflix is a subscription-based streaming service that allows its members to watch tv shows and movies without commercials on an internet-connected device (ref. netflix.com). There is an opportunity to optimize the selection of tv shows and movies for the business to increase member subscriptions and/or stock prices by analyzing the current lists of shows/movies, list of Netflix original shows/movies, the IMDB scores of the shows/movies and the stock prices data.

Problem: <br/>
The system helps us to find out what the most popular genre of movies/shows are in the current Netflix shows/movies selection; whether the popular videos align with high IMDB scores; whether Netflix originals have higher IMDB scores; and if there is a positive relationship between high score movies/shows to the stock prices.

Dimensional Model: <br/>
![image](https://user-images.githubusercontent.com/27581761/115129594-6b1ea700-9fb5-11eb-958a-c92318085de0.png)

https://github.com/wt051453/ETL-in-data-warehousing-project/blob/main/dimensional%20model.pdf

Architecture Diagram: <br/>
![image](https://user-images.githubusercontent.com/27581761/115129595-71ad1e80-9fb5-11eb-8e70-2616bc22088c.png)

https://github.com/wt051453/ETL-in-data-warehousing-project/blob/main/Architeture%20diagram.pdf

Detailed Design: <br/>
The datasets we found from Kaggle.com allow us to analyze and study the relationships between Netflix’s movies and shows selection to IMDB scores and their stock prices. For ETL steps, we chose to use python because it is one of the popular general-purpose programming languages that is capable of performing the tasks and the team is familiar with. We chose to run our data warehouse on MySQL server because it is a popular relational database management system that provides secure and fast data storage, fast query speed and the team is also familiar with it. Finally, we chose Tableau to create visualizations because it is a powerful visualization tool that offers ease of use and many visualization possibilities. Any future members to the team may already have experiences using these technologies or can easily pick up how to use them because there are many instructions or documentations available for these technologies which will significantly reduce the training time and cost.

ETL: <br/>
![image](https://user-images.githubusercontent.com/27581761/115129599-7c67b380-9fb5-11eb-90ea-bbc4f069d5d5.png)
https://github.com/wt051453/ETL-in-data-warehousing-project/ETL <br/>

Final Schema: <br/>
![image](https://user-images.githubusercontent.com/27581761/115129748-dd43bb80-9fb6-11eb-80a4-631949edc47a.png)

![image](https://user-images.githubusercontent.com/27581761/115129752-e3399c80-9fb6-11eb-95f8-6035664ae834.png)

![image](https://user-images.githubusercontent.com/27581761/115129755-e765ba00-9fb6-11eb-81f8-322757edc8a3.png)

![image](https://user-images.githubusercontent.com/27581761/115129757-eb91d780-9fb6-11eb-812c-38d15b54c278.png)

![image](https://user-images.githubusercontent.com/27581761/115129760-f0ef2200-9fb6-11eb-86b5-5d6d19f816d2.png)

![image](https://user-images.githubusercontent.com/27581761/115129762-f5b3d600-9fb6-11eb-8c43-45570ed76794.png)

The final schema for our project is a Star schema which contains two fact tables and four dimensional tables. <br/>

Dashboard Application: <br/>
![image](https://user-images.githubusercontent.com/27581761/115129628-aa4cf800-9fb5-11eb-81f4-86571a2118e2.png)
Use MySQL workbench to monitor performance <br/>

Connect Tableau to MySQL: <br/>
![image](https://user-images.githubusercontent.com/27581761/115129574-36125480-9fb5-11eb-8947-9657a84c5e9f.png)

The analytics/visualization in the dashboard help answer the questions in the Problem section.

What the most popular genre of movies/shows are in the current Netflix shows/movies selection and whether the popular videos align with high IMDB scores? The answer is no, the most popular shows on the left don’t always correspond to high IMDB scores on the right. <br/>
![image](https://user-images.githubusercontent.com/27581761/115129569-23981b00-9fb5-11eb-8c87-17904dbfa8d4.png) 

Settings to create the visualization: from facts_imdb_rating table, I put the ‘Listed in’ to Rows as ‘Dimension’ and put Counts of ‘Listed in’ and Average of ‘Rating’ to the Columns and finally displayed the data in bar graph.

Do Netflix originals have higher IMDB scores? The answer is yes. The originals have slightly lower max score (9.5 vs 9.7) than not originals but have higher 75th percentile, median, 25th percentile and mix score than not originals. <br/>

![image](https://user-images.githubusercontent.com/27581761/115129665-fd26af80-9fb5-11eb-82f9-3a45422b4e3b.png)

Settings to create the visualization: from facts_imdb_rating table, I put the ‘Rating’ to the Rows and put ‘Original Title’ as the filters (selecting all except null) to create the boxplot. <br/>

![image](https://user-images.githubusercontent.com/27581761/115129673-116aac80-9fb6-11eb-9e79-430bf3353aab.png)

Settings to create the visualization: from facts_imdb_rating table, I put the ‘Rating’ to the Rows and put ‘Title’ (selecting all) and ‘Original Title’ (selecting null only) as the filters so the data only reflects non Netflix originals to create the boxplot. <br/>

Is there a positive relationship between high score movies/shows to the stock prices? The answer is no, there is no positive correlation between the average IMDB scores to stock prices by year. <br/>

![image](https://user-images.githubusercontent.com/27581761/115129686-26dfd680-9fb6-11eb-94f1-a28edb59c176.png)

Settings to create the visualization: from facts_imdb_rating table, I put the  Average ‘Rating’ to the Rows, from facts_stock_prices table, I put the Sum ‘Adj Close’ to the Rows, and from date_dim table, I put ‘Year’ to the Columns to create the dual Y-axis graph to show average rating and total of adjusted closing prices by year. <br/>

A map to show the average IMDB scores by country. <br/>

![image](https://user-images.githubusercontent.com/27581761/115129692-38c17980-9fb6-11eb-8ce0-9db935c7eaf1.png)

Settings to create visualization: I put the Tableau auto generated Longitude and Latitude to Columns and Rows respectively and put Average ‘Rating’ in 'Color', Counts ‘Rating’ (facts_imdb_rating) and Country (show_dim) as ‘Dimension’ in the Detail to display the world map showing average IMDB rating by country. <br/>

Conclusion: <br/>
The analytics built in Tableau using data transformed by the data source helped answer the problems we identified during the planning section and learned from data analysis that there are room to improve the movie/show selections in genres that received high IMDB rating, produce more high quality Netflix original movies/shows and increase movies/shows from countries that have higher than average IMDB ratings to attract more and retain existing subscriptions. <br/>

During this assignment, I got the opportunity to work on tasks that are practical and identical to real life project and it was a tremendous and valuable experience. I have learned how to figure out what directions to seek answers when I was stuck, effectively ask and follow-up with questions, perform researches (mostly online) using keywords and quickly acquired the necessary skillsets to solve various problems I ran into. I believe this will be beneficial for me as a Data Analyst or any other positions in the future. If I had to do it all over again, I would still be proactively getting involved in as much of the project as I could, working diligently with and motivating all the stakeholders.  

