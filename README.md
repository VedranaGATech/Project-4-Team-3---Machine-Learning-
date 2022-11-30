# Project 4: Machine Learning - Predicting NBA Finals Winner 

![Alt text](/Images/cover.png)


## Team 3:

    Emmanuel Yoacel Okecha
    Leon Lee
    John McMullan
    Lennox Nguyen
    Stephen Jackson
    Vedrana Basimamovic


## Final Project Requirements: Demystifying ML

### Find a problem worth solving, analyzing, or visualizing:
  Analyzing NBA data (teams and games) to predict the winner of the NBA Finals, by using machine learning (ML) with the technologies we’ve learned such as SQL, Python, Pandas, Matplotlib, and Tableau. We are also using Scikit-learn as our ML library. 
  
### Rationale
  The NBA Finals is the annual championship series of the National Basketball Association. The Eastern and Western Conference champions play a best-of-seven game series to determine the league champion. With the growing popularity of sports betting, we wanted to create a simulator that will predict the winner of the NBA Finals taking place in June so that potential sports bettors can place their bets with the help of a data model.
  
  ![Alt text](/Images/alt_cover.png)
  
### Sources:
  
    * Official NBA Stats API  | https://www.nba.com/stats 
    * NBA Team Stats |  www. hoopsstats.com
    * NBA Games Data | https://www.kaggle.com/datasets/nathanlauga/nba-games

### Project 4 Group Work

  The requirements for this project are broken into 5 categories:
   * Data and data delivery via Python and Pandas
   * Back end (ETL) via SQL
   * Visualizations via Tableau
   * Group presentations by all team members
   * Slide deck via Powerpoint

## Step 1 - Data Delivery via Python and Back End via SQL
  We connected to the NBA_API.Stats and pulled the team metics data for seasons from 2017 to 2022. We then averaged the team metrics for overall measures and exported as a CSV and into SQL to apply to the model.
    ![Picture2](https://user-images.githubusercontent.com/101353436/204672360-0fd888ed-8233-4054-90fb-ab8b7f40f535.png)
    ![Picture1](https://user-images.githubusercontent.com/101353436/204672226-68c3598b-c6bd-4a02-a7fa-45432cd36462.png)
  ![Alt text](/Images/1.png)
![Alt text](/Images/2.png)
## Step 2 - Build Function to Analyze Data
 Function needs to run through provided data easily and with reasonable success. First we need to pull the data from SQL and drop any unwanted columns.
  
 ![Alt text](/Images/1.png)
 
 We took these two new data frames and ran them through the following code to create two unique dictionaries to use:
 
 ![2022-11-27 14_19_20-Window](https://user-images.githubusercontent.com/100164773/204679791-84655a54-bc78-4638-bd76-e75752c20167.png)

In each dictionary there are 210 unique data frames for each match up.


Function:

![Picture4](https://user-images.githubusercontent.com/101353436/204678267-7aad1f8d-3179-437b-969c-ec0f3401addb.png)

This function will:

1. Find Home team and Away team
2. Set x and y values
3. Train those values
4. Fit those values to the pipeline created in the loop
5. Scale Values
6. Score Values
7. Use Predict to find win, loss, and percentage values
8. Append all data


## Step 3 - Run Data Through Function through results 
Take Clean Data and run it through the function to find results. It will produce the following dataframe:

![2022-11-27 14_44_57-Window](https://user-images.githubusercontent.com/100164773/204679480-10a2c74d-a0a7-44e4-a3a0-c6dc443f50a4.png)

Final Results:

![2022-11-27 14_54_02-Window](https://user-images.githubusercontent.com/100164773/204679464-c0cbdaed-9e70-4b4c-b0fc-f3c6264d2218.png)

## Step 4 - Visualization via Tableau 

![Alt text](/Images/l2.png)
![Alt text](/Images/leon.png)

<img src = "Images/Win Chance Maps.png" width = "700">

For the first visualization, we predicted the Boston Celtics’ chances of winning against each team in the East Conference. Based on internet predictions, the NBA favorite for the 2023 NBA East Conference title will be the Boston Celtics while the NBA favorite for the 2023 NBA West Conference title will be the Golden State Warriors. For example, if the Boston Celtics faced the Atlanta Hawks, the chance of the Boston Celtics losing against the Atlanta Hawks would be 25%. So far in the season, the Boston Celtics are winning most of their games, living up to their expectations for winning the NBA East Conference.

Then, for the second visualization, we predicted the Golden State Warriors’ chances of winning against each team in the West Conference. For example, if the Golden State Warriors faced the Los Angeles Clippers, the chance of the Golden State Warriors losing against the Los Angeles Clippers would be 45%. So far in the season, the Golden State Warriors are on a losing streak, not living up to their expectations for winning the NBA West Conference.

<img src = "Images/Heatmap Predictions.png" width = "700">

For the heatmap dashboard, we showed the chances of winning for the home teams against the versus teams. Each square in the heatmaps represents the percentage as its own dataset, based on the functions filtering and looping through all of the data. As shown, the varying intensity of color represents the measure of correlation between the teams’ chances of winning and losing.

<img src = "Images/Avg Net Graphs.png" width = "700">

For the average net rating dashboard, the x-axis is the average chance of winning while the y-axis is the average estimated net rating. The net rating is the offensive rating minus the defensive rating. For the East Conference, the r-squared correlation is 0.85, meaning that the net rating has a big impact on the basketball teams winning its games. However, for the west conference, the r-squared correlation is 0.59, meaning that the net rating has a decent impact on the basketball teams winning its games.

<img src = "Images/Avg Rebound Graphs.png" width = "700">

Finally, the average rebound dashboard is very similar to the previous dashboard. The only difference is that the East and West Conference did not have any impact on the basketball teams winning its games, in terms of rebounds, compared to the net rating in the previous dashboard.

