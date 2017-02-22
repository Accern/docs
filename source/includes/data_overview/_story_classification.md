##Story Classification
Millions of articles (tweets, blogs, etc.) are processed by Accern every day. When a story about Snapchat breaks out and it's related to an *IPO* event, many articles are published from different sources and new articles are published from the same sources with updates as the story progresses. To track analytics such as the sentiment or the exposure of this fresh news, we group together similar articles about the same information and call it stories.
Accern is the pioneer in this story classification process, allowing you to track how information flows in the media. By grouping together multiple articles which have the same gist of information/ talking about the same information, we can track the life of the story from start to end.

Story classification model is agnostic of the sentiment and it only groups based on the entities and events.
Semantic structure of the article is taken as input. The model identifies important themes and checks in the last 2 weeks for similar theme.
If similar theme was found, it groups along with this theme.
*Use a combination of machine learning models to identify entities and eventually map them back to one of these 8k+ equities in the dictionary.*

###Proprietary Entities Dictionary
Accern has developed a proprietary dictionary that tracks online articles mentioning any of the 8,000-plus U.S. public equities.
By mapping all ways financial entities are mentioned in the media back to 8k+ equities, this dictionary aids in entity extraction when classifying stories.

The dictionary consists of over 150,000 company name variations, which are mapped back to the 8,000-plus U.S. public equities.
It includes Bloomberg IDs, ticker symbols, etc. back to these company names.
Looking at historical data, we identify the different ways companies have been mentioned to build and update this dictionary.

###Proprietary Financial Events Dictionary
Accern has developed a proprietary dictionary that tracks online articles mentioning any of the 1,000-plus financial events. 
The dictionary consists of over 30,000 financial event variations, which are mapped back to the 1,000-plus financial events.
We worked with financial analysts/equity researchers to figure out an initial list of important financial events. 
Then, we used this list and looked at the historical data to figure out different variations of event names which are updated into the list. 
Again, this dictionary is essential for extracting events/themes for each story.

**Anshul**