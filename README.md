# Project-3_Gaming-Analysis_ML

The goal of this project was to develop a dashboard tool for gaming information.  Our data sources included PC games data from Steam (via api and website scraping) and console game data from Microsoft (by scraping their most played games by country websites.)   

Our github repository is located at:
https://github.com/cbragg3136/Final_Project-Gaming_ML.git 

The Heroku app allows you to selectively display the following:
https://gaming-ml.herokuapp.com/

MS console web pages:
Top 50 Most played games by Country table: 
    - ability to query most played games by country (will show the top 50 games in that country)
    - ability to display the rank of popularity for a game in all countries (ex. Fortnite is the 1st most popular game in US, 2nd in UK, ...)
    - ability to display a table of the Xth ranked game in all countries (ex. show the 5th most popular game in each country)
MS Games Map - graph of the world showing the countries we scrapped data for, and the most popular game in each country
MS Detail Games- a table showing the game detail information for the top 50 games in the US

PC Games web pages:
TOP PC Games - ability to create a table pulling from all games on Steam (takes about 10 secs per query...), query by category, genre, or game name
STEAM Top 100 - ability to see the top 100 games on Steam in the present moment based on concurrent players.
STEAM PLayer Data - the ability to graph games from the top 100 based on concurrent players from the last 5 days (you can pick multiple games and compare them).
STEAM Player Data - In addition we show a vertical bar chart highlighting the top 5 games and their player size and a donut chart highlighting the volume of players publicly reporting location by continent

Several machine learning models were created to predict game success as measured by Max Concurrant Users (MCUs) based on player generated game tags. The game tags are game descriptors that relate to genre, game features, graphics style etc. To determine the success of our models we primarily used two measures, F1 scores and AUROC scores. F1 scores measure predictive ability but do not account for overfitting, AUROC scores (Area Under the Curve of Receiver Operator Characteristc) delineate true vs false positives at different decision thresholds and therefore is not as influenced by overfitting.
