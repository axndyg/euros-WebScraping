# euros-WebScraping

![Euros Banner](./graphics/euros_banner.jpg)

Football is the sport of life and the running Euro's compeititon has been celebrating the culture since the 1960's. With the most recent rendition (as of the making of this repository) being UEFA's Euro 2024 compeittion, exictement draws near to crown a new European Nation within the sport.  

This repository is a mixed project and self-assigned teaching to the principles of web scraping and machine learning advantaging of past football perforamcnes of National Teams to predict the Euro 2024 winner.

The purpose of this is to learn the fundamentals of Data Science by familizaring myself with the relevant tools (in this project, python and relevant packages) and practiaclly put these tools to use with relevant real-world scenarios within the sport of football. 

## Methods 

Python packages used within this project 

* requests
* beautifulsoup
* pandas
* io
* scikit-learn

The first four packages were deployed to scrape web-page data from [Terrikon](https://terrikon.com/en/), a football database containing all the past Euro's outcomes. With them, I then formed a database containing each team's performance against another team and at what stage in the competition. 

scikit-learn was employed for the RandomForestClassifier that acted as my machine-learning algorithm to predict the results of fixtures in the Euros competition. 

### Metrics

To train the RandomForestClassifier, we needed to set the relevant deciding factors of a game. For my model, I chose the following:  

* Team
* Opponent
* Stage of Competition
* Match Type 

## Take-aways 

A lot ot the code is redunant, or at least could of been fashioned more efficiently. I am keeping the code in its original form as I work on code needed to address how prior code produced data that didn't come out as we needed it later on. The purpose of keeping old code and writing new code to ammend it is to show progress of my understanding with webscraping and formatting it in a desired manner. As well, the practice of ammending the old code is beneficial to continue to learn how to manipualte data through python and it's 

## Crediting 

This project was aided with the teaching from the following YouTube videos and package documentations 

>[Normalized Nerd](https://www.youtube.com/watch?v=ZVR2Way4nwQ)
>[Data Quest](https://www.youtube.com/watch?v=0irmDBWLrco&t=2048s)

## License 

[MIT](https://choosealicense.com/licenses/mit/)