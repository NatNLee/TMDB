# TMDB

Data Source: 
https://www.kaggle.com/c/tmdb-box-office-prediction/data

https://www.kaggle.com/stefanoleone992/imdb-extensive-dataset?select=IMDb+movies.csv


Presentation Slides:

https://www.canva.com/design/DAEJJKqAZhk/zigxyiVIs8-RbjAENXCT7w/view?utm_content=DAEJJKqAZhk&utm_campaign=designshare&utm_medium=link&utm_source=sharebutton

Notes:

1. Imported only the TMDB train data csv and used data cleaning and wrangling methods featured below to create dummy variable columns for collection, genre, production companies, spoken languages, keywords, cast, and crew from dictionaries in each row.: 

https://www.kaggle.com/artgor/eda-feature-engineering-and-model-interpretation

by Andrew Lukyanenko (https://www.kaggle.com/artgor) 

2. Joined IMDB ratings csv with updated TMDB csv from step 1. In Excel, updated last 10 rows with their correct release dates. Ordered data by ascending release date. Replace spaces in columns names with underscores (to avoid patsy errors).

3. Invesitgating what makes movies successful and defining success as high ratings and high revenue. Created 2 linear models (shuffle=False to avoid data leakage with time series data), one to predict ratings ("weighted average vote") and one to predict revenue. Tested a variety of variable combinations in the models to improve accuracy. 

Latest model for revenue included collection, budget, gender of cast, keyword suspense, keyword dystopia, genre Romance, genre Family, genre Animation, number of genres, keyword sequel, gender of crew, genre crime. 66% accuracy.

Latest model for ratings included collection, budget, runtime, genre Animation, genre Drama, genre Action,  genre Romance, genre Thriller, genre Adventure, number of genres, number of languages, keyword indepedent film, gender of crew, gender of cast, number of keywords. 30% accuracy.

4. EDA and all charts for presentation done in Tableau:
https://public.tableau.com/profile/natasha2059#!/vizhome/TMDB2/RevandRatvsBudget2

5. Conclusion: To maximize the potential success of a movie, it should have the following elements gathered from EDA in step 4 and the linear models in step 3. A budget of $2 million will garner the highest return on investment, runtime of 2 hours garners highest ratings, content of movie should include adventure, suspense, romance, animation, drama, independent film, and be apart of a series and use a lot of keywords in its description/marketing. The presentation features a hypothetical movie with these elements (hypothetically see it in theaters near you September 2021).



