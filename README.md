# euros-WebScraping

![Euros Banner](./graphics/euros_banner.jpg)

Football is the sport of life and the running Euros competition has been celebrating the culture since the 1960s. With the most recent rendition (as of the making of this repository) being UEFA's Euro 2024 competition, excitement draws near to crown a new European Nation within the sport. 

This repository is a mixed project and self-assigned teaching to the principles of web scraping and machine learning advantaging of past football performances of National Teams to predict the Euro 2024 winner. 

The purpose of this is to learn the fundamentals of Data Science by familiarizing myself with the relevant tools (in this project, python and relevant packages) and practically put these tools to use with relevant real-world scenarios within the sport of football.

## Methods 

Python packages used within this project 

* requests
* beautifulsoup
* pandas
* io
* scikit-learn
* matplotlib

The first four packages were deployed to scrape web-page data from [Terrikon](https://terrikon.com/en/), a football database containing all the past Euros outcomes. With them, I then formed a database containing each team's performance against another team and at what stage in the competition. 

scikit-learn was employed for the RandomForestClassifier that acted as my machine-learning algorithm to predict the results of fixtures in the Euros competition. 

### Metrics

To train the RandomForestClassifier, we needed to set the relevant deciding factors of a game. For my model, I chose the following:  

* Team
* Opponent
* Stage of Competition
* Match Type

## Results

The model hovered between a 55-73% accuracy rate, with projecting the least confidence in correctly predicting a draw. There is further room for error when deciding the missing spots for the Round of 16. The UEFA page saves three spaces in the Knockout Round for Third-place finisher. The metric I decided was complete random draw. A consequent re-run of the program might produce a new winner based on the outcome of the draw. 

With my first model, here is the Euros 2024 Knockout Round fully predicted!
<img src="./graphics/bracket_view.png" width=60% height=60%> 

And the crowned winner in . . . <br> 
<img src="./graphics/spain_flag.png" width=40% height=40%>

Spain!

## Performance  

The competition was split into two phases: the Group and Knockout Stages. Each team was guaranteed in the group stage to play three times; one match against each of their three group-mates. These matches I could then predict and accurately compare the prediction to the real results.

However, there is a caveat to the second phase. Placement of teams paired head-to-head for the Round of 16 was entirely dependent on their performance in the group stage. My algorithm expectedly predicted false results, making the Group Stage placements reflect differently than they actually turned out. This meant the margin of error was amplified moving into the Knockout Stage where teams were placed against one another without the match ever having taken place in real life.

For example, takea loot at this cell instance in [trial one](./predictions/match_preds/t1_euros2024.csv) produced by my model: 

| 	  | stage		 | team_a	| res_a  | res_b | team_b  | date       |
| --- | ------------ | -------- | ------ | ----- | ------- | ---------- |
| 42  | Round of 16  | Portugal | W	     | L	 | Hungary | 2024-07-01 | 

This matchup never occured, but it's placement was a result of group stage performances. Then it became clear that I could only perform anaylsis on the peroframnce of the model based on known matchups in the group stage. Here are the metrics: 

|     | Accuracy | Win Precision | Draw Precision | Loss Precision | 
| --- | -------- | ------------- | -------------- | -------------- |
|     | 44%      |  33%          | 43%            | 57%            |

Or, graphed out:

<img src="./graphics/e_perforamnce.png" width=40% height=40%>

Then, with less than 50% accuracy and less than 50% precision (for most predictions), it is safe to say this model wasn't the best performer. Flipping a coin would produce better accuracy. 

This isn't, however, nothing to learn from. The metrics that decided the model's predictions could have been expanded to more nuanced details. The largest basis of decision for the model was purely the name of the countries playing and at what stage. It did not take a look at the current roster of each team and how that roster has been performing in recent time. 

Although simple, through this model I gained a deeper understanding in the fundamentals of machine learning. However, although its accuracy did not shine, it did strike the right answer. Through multiple trials, it consistently (through random Knockout placements) placed Germany or Italy as the eventual winner, with the very first trial I ran being the only one (so far) to predict the eventual winner, **Spain**

## Take-aways 

From this project, I learned how to wrangle with online databases and manipulate relevant html tags to format a DataFrame with the desired data for my RandomForestClassifier model. I am more confident in my Python skills as I had to clean data that was formatted not so friendly in awkward html tables or creviced in odd html tags. As well, I have a greater understanding in the purpose of the packages I used within this project. 

This project was a fun demonstration and learning moment for what my possible work will look like as a Data Scientist post-graduation. As my first practical experience, this was a great teaching moment. A lot of the code was redundant and repeated but I am preserving the nature of the Notebooks to show the progression of my understanding. 

From this point, I trust this project will serve as a great basis to my future endeavors and be crucial to my understandings of finding relevant data and modeling them practically.

## Crediting 

This project was aided with the teaching from package documentations and the following YouTube videos: 

>[Normalized Nerd's Decision Tree Classification](https://www.youtube.com/watch?v=ZVR2Way4nwQ) <br> 
>[Data Quest's Predict Football Match Winners](https://www.youtube.com/watch?v=0irmDBWLrco)

## License 

[MIT](https://choosealicense.com/licenses/mit/)