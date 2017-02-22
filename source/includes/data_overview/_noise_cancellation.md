##Story Classification
###Proprietary Entities Dictionary
Accern has developed a proprietary dictionary that tracks online articles mentioning any of the 8,000-plus U.S. public equities. The dictionary consists of over 150,000 company name variations, which are mapped back to the 8,000-plus U.S. public equities.
Dictionaries map different ways financial entities are mentioned in the media back to 8k+ equities. 
It includes Bloomberg IDs, ticker symbols, etc. back to these company names.
Looking at historical data, we identify the different ways companies have been mentioned to build and update this dictionary.

###Entity Extraction
Use a combination of machine learning models to identify entities and eventually map them back to one of these 8k+ equities in the dictionary.

###Proprietary Financial Events Dictionary
Accern has developed a proprietary dictionary that tracks online articles mentioning any of the 1,000-plus financial events. The dictionary consists of over 30,000 financial event variations, which are mapped back to the 1,000-plus financial events.
We worked with financial analysts/equity researchers to figure out an initial list of important financial events. Then, we used this list and looked at the historical data to figure out different variations of event names which are updated into the list. 

##Noise Cancellation
Accern parses through data in the millions. * Have to break this up into noise cancellation tab and entity detection tab *

###Proprietary Pattern Recognition Spam Detector
Our proprietary noise cancellation mechanism identifies if the article it's seeing is an ad, or a spam, and does not contain information . If article looks like spam. We have a list of blacklisted sources that are know to send spam a lot. Also have regex expression based phrases, which are indicators to if the article is spam or not. 
This noise cancellation mechanism takes around 150M+ articles + tweets every day and gives out around 25k articles at the end.
Using machine learning and pattern recognition, Accern is able to automatically figure out which articles can be classified as spam based on the way their titles are written.
<br/>
`Example: Save Up to 50% on Your Purchases with Coupons at Amazon.com!`
<br/>
Accern will use pattern recognition to identify future articles talking about coupon codes from Amazon and automatically remove it.
###Proprietary Blacklist of Spam Websites
Accern has developed a list of websites, such as retailmenot.com, that are known to release spam or irrelevant content to financial markets investors.
Looking into the history of our sources, we are able to figure out the probability of an article from this source will be spam. Hence, if it's metric is above a threshold we include it in our blacklist which is constantly updated.