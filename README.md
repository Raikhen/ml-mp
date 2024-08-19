# Exploring what makes rock climbing routes good or bad

This project attempts to figure out what makes a climb good or bad. It considers several factors
- Length of the climb
- Difficulty of the climb
- Number of pitches
- The style of the climb

and then fits linear regression models and computes the R^2 for each factor individually.

This project was done by Dylan Fridman in the context of Professor Schwarze's Mathematics and AI course at Dartmouth College during the Boreal Summer of 2024. The data was scraped from [Mountain Project](https://www.mountainproject.com/) and uploaded to a MongoDB database. Only a subset of the routes uploaded to Mountain Project were scraped due to time constraints: only 9421 routes were taken into consideration for this analysis. Reach out to me for access to the MongoDB database.