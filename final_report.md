# Final Report

## Introduction

This project attempts to figure out what makes a rock climbing route good or bad, awful or amazing. In order to do so, we use data from [Mountain Project](https://www.mountainproject.com/), a web/mobile application that lots of American and Canandians use to find useful info about a climb they want to do. Each climbing route uploaded to Mountain Project has a rating, ranging from 0 to 4 stars. 0 stars means that the climb was terrible and is not worth repeating, while 4 stars means that you won't stop smiling after climbing it.

We try to see how much other features of a climb correlate with its star rating. We consider:
- Length of the climb (for single pitch climbs)
- Difficulty of the climb (as given by its Hueco or YDS grade)
- Number of pitches
- The "style" of the climb

The reason for style to be inside quotation marks is that we use it in a very broad sense. The presence of a particular kind of hold or even the quality of the rock are considered part of its style. The way this is implemented has a "bag-of-words" flavor: for every keyword such as "choss", "offwidth", "jugs", or "slab", we do a linear regression to see how well the presence of that particular keyword in the description helps predict its rating.

## Results

### Difficulty

The first factor we considered was difficulty as given by its YDS or Hueco grade. We splitted the data into boulders and lead climbs. After doing a linear regression, we found a positive correlation in both cases. For lead climbs, the R^2 was of 0.175 and for boulders it was 0.135.

### Length (for single pitches)

Interestingly enough, difficulty proved to be more significant that the length of a single-pitch climb since after doing a linear regression on the height, although there was a slight positive correlation, it had a weak slope and a R^2 value of 0.04.

### Number of pitches (for multi-pitch climbs)

Contrary to what one might intuitively expect, number of pitches didn't correlate that well with the star rating of a climb with tiny positive correlation and a R^2 of 0.005. That said, only 576 routes could be considered for this regression so it would be interesting to do with more data.

### Style

Unfortunately, similar to the previous case, no correlation seemed particularly strong but also N was very small for these cases since, for any given keyword, most route descriptions don't contain them.

## Insights

This project made me realize how hard it is to obtain good predictors in the social sciences.

## Appendix

In case that some of the climbing jargon was confusing, refer to [this glossary](https://www.rei.com/learn/expert-advice/rock-climbing-glossary.html).