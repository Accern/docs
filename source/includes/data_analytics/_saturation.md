##Saturation (story_saturation)

The online exposure of the story i.e. have a lot of people seen this story/information already?
This is one of the useful metrics possible thanks to *story classification*.
Based on web traffic information (provided by Alexa Rank) of related articles and previous historical data, we predict the exposure of the story into different levels  - low, mid, & high.
**Note:** Twitter tweets takes into account the number of followers, retweets, and other metrics that twitter user has.

**Quick Definition:** gauge the current potential exposure of a story

###How is it calculated? **Anshul**
3-Step Process for Computing Saturation

- Step 1: accumulate web traffic per story
We accumulate total web traffic based on all related articles per story

- Step 2: average web traffic per story
We look back at all similar stories’ total web traffic and take an average per story 

- Step 3: segment average story web traffic
We segment the average story web traffic into low, mid, and high saturation 

###Examples:
 
A story about NVIDIA's earnings published by at least 30 sources, of which it includes marketwatch.com , cnbc.com, etc. has high exposure (highly saturated) 
Even a story 
- Saturation (High) - story published on 100+ websites
 
- Saturation (High) - story published on two major newswires

- Saturation (Low) - story published on one medium-traffic website

- Saturation (Low) - story published on five small websites