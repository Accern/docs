##Noise Cancellation
Accern processes millions of articles/day of which a significant amount ends up as spam/ads/coupons/etc.
To tackle this issue, Accern has optimized it's noise detection algorithms over the years.
This noise cancellation mechanism takes around 150M+ articles (tweets, articles, blogs, etc.) every day and gives out around 25k articles at the end.

**Proprietary Pattern Recognition Spam Detector**

Our proprietary noise cancellation mechanism identifies if the input article qualifies as spam and does not contain any insightful information.

**How? -** A compiled list of *regex-expression based phrases* are used to classify the articles as spam or not.
Using machine learning models and pattern recognition, Accern is able to automatically figure out which articles can be classified as spam based on the way their titles are written.

`Example: Save Up to 50% on Your Purchases with Coupons at Amazon.com!`

Accern will use pattern recognition to identify future articles talking about coupon codes from Amazon and automatically remove it.

**Proprietary Blacklist of Spam Websites**
Accern has compiled a proprietary list of websites that are known to release spam, irrelevant content to financial markets investors.

**How? -** Looking in the historical archive of articles posted by different news sources, we calculate the probability that a newly published article from this source will turn out as spam.
If the probability is above a threshold, we include it in our blacklist which is constantly kept up to date.