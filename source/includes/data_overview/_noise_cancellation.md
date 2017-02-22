##Noise Cancellation
Accern parses through data in the millions and over the years has optimized it's noise detection algorithms.
This noise cancellation mechanism takes around 150M+ articles (tweets, articles, blogs, etc.) every day and gives out around 25k articles at the end.
**Anshul**

###Proprietary Pattern Recognition Spam Detector
Our proprietary noise cancellation mechanism identifies if the article it's seeing is an ad/spam and does not contain insightful information.
A compiled list of regex expression based phrases act as indicators to if the article is spam or not. 
Using machine learning and pattern recognition, Accern is able to automatically figure out which articles can be classified as spam based on the way their titles are written.

`Example: Save Up to 50% on Your Purchases with Coupons at Amazon.com!`

Accern will use pattern recognition to identify future articles talking about coupon codes from Amazon and automatically remove it.

###Proprietary Blacklist of Spam Websites
Accern has developed a list of websites, such as retailmenot.com, that are known to release spam/ irrelevant content to financial markets investors.
Looking into the history of the sources, we are able to figure out the probability that an article from this source will turn out as spam.
Hence, if the calculated metric is above a threshold, we include it in our blacklist which is constantly updated.