##Noise Cancellation
Accern parses through data in the millions and over the years has optimized it's noise detection algorithms. **Anshul** *Some statistic here on the amoun of noise*

###Proprietary Pattern Recognition Spam Detector
Our proprietary noise cancellation mechanism identifies if the article it's seeing is an ad, or a spam, and does not contain information.
If article looks like spam. We have a list of blacklisted sources that are know to send spam a lot. Also have regex expression based phrases, which are indicators to if the article is spam or not. 
This noise cancellation mechanism takes around 150M+ articles + tweets every day and gives out around 25k articles at the end.
Using machine learning and pattern recognition, Accern is able to automatically figure out which articles can be classified as spam based on the way their titles are written.
<br/>
`Example: Save Up to 50% on Your Purchases with Coupons at Amazon.com!`
<br/>
Accern will use pattern recognition to identify future articles talking about coupon codes from Amazon and automatically remove it.
###Proprietary Blacklist of Spam Websites
Accern has developed a list of websites, such as retailmenot.com, that are known to release spam or irrelevant content to financial markets investors.
Looking into the history of our sources, we are able to figure out the probability of an article from this source will be spam. Hence, if it's metric is above a threshold we include it in our blacklist which is constantly updated.