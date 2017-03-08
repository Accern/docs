##Sentiment (article_sentiment)
**What is it?** Sentiment score (-1 - +1) of the article based on title and content.

**Quick Definition:** determines if the article was written positively or negatively by the author/editor.

**How is it created?** Sentiment Analysis of articles involves 3 parallel models. **(bag of words + n-grams + deep-learning)**

* Bag of Words involves a proprietary list of 300,000-plus positive and negative words, differently weighed, which are used to gauge a base sentiment of an article.

* N-grams involves a proprietary list of positive and negative two- to three-word phrases which are used to gauge a more accurate sentiment in articles. 
These lists are compiled by financial analysts.

* Next, a Deep Learning model predicts how much the article is positive or negative based on the vector representation of its text. 

* Finally, a meta model (ensemble learning) uses the output of all these 3 models to generate a final score.

**Examples**

Snippets of articles with a **negative sentiment** about a publicly traded equity - Tesco Inc

* **Tesco strike to escalate** - "Over 2-thousand staff in 22 Tesco stores will be on strike by the middle of next week. Another 24 stores were balloted for industrial action by Mandate over the past three nights - 6 agreed to join the 16 stores currently on the picket line.
The retailer says the results of the ballot mean there's an onus on the union to call-off the strike...."

* **Striking Tesco workers will not have Family Income Supplement suspended** - "The ongoing strike at a number of Tesco stores has been suspended from this morning after both sides in the dispute agreed to attend discussions at the invitation of the Labour Court.
Tesco has confirmed that it will not make any changes to pre-1996 terms and conditions whilst this process is ongoing. The Mandate trade union said all pickets will be suspended and the talks are expected to get under way this weekend...."

* **Tesco workers shouldn’t lose Family Income Supplement** - "This would be a completely unfair and mean spirited move. I believe that there is scope under the current legislation for the Minister to direct that no such decision is made. 'By engaging in strike action, the workers are already seeing a reduction in their take home pay; a cut to their FIS payment will devastate families....'"

##Sentiment (story_sentiment)
**What is it?** An average of all the sentiment scores of articles that fall into this story until now.
**NOTE:** If there is only one article in a story so far, then its **first_mention=TRUE** , and **story_sentiment** equals **article_sentiment**.

**Quick Definition:** aggregates article sentiment and calculate the average sentiment for each story

**How is it created?** Article sentiments calculated via the procedure explained in the above [Article Sentiment Section](#sentiment-article_sentiment) are all aggregated and the average is calculated.
As the story grows, the overall sentiment keeps changing and a trend can be captured with time.

**Examples**

Looking at articles reporting on **company earnings** of Baidu (BIDU), there exist mixed reviews from different sources.
Interestingly, the overall story sentiment saturated to end up as positive as more and more articles were posted.

Initial Negative articles - 

* **Baidu's quarterly revenue falls 2.6 percent** - "Baidu Inc reported a second straight drop in quarterly revenue as regulatory scrutiny into healthcare and related advertisements continued to take a toll on the Chinese internet search giant. The drop, however, was within the 17.84-18.38 billion yuan range the company had previously forecast. Analysts estimate that healthcare accounts for about 20-30 percent of Baidu's search revenue, which represents more than 80 percent of the company's total sales...."

Dispersed Positive articles - 

* **Baidu reports stable 2016 revenue growth** - "Chinese Internet giant Baidu reported stable revenue growth in 2016, helped in part by artificial intelligence (AI) upgrades to its various products. Baidu continued to see stable user growth for its search and map services, with its mobile payment business Baidu Wallet attracting 100 million users by the end of 2016, surging 88 percent compared with 2015...."

* **Baidu posts bleak fourth quarter, but sees business reshuffle driving 2017 growth** - "Baidu Inc's revenue fell for a second straight quarter, hurt by a government crackdown on healthcare advertising, but the internet search giant expects a rebound this year as it retools to find growth outside its core ad business. The company has stumbled over the past few years - firstly from a cash-burning subsidy war with rivals such as Alibaba in businesses like food delivery, movie tickets and taxi hailing...."