##Sentiment (article_sentiment)
Sentiment of the article written by the author/editor. Articles are published by sources like Bloomberg, NYT, etc.
Within each source, exists authors who are responsible for their articles.

###How is Sentiment Analysis done?
Sentiment Analysis of articles involves 3 parallel models. (bag of words + n-grams + deep-learning)
Bag of Words involves a proprietary list of 300,000-plus positive and negative words, differently weighed, which are used to gauge a base sentiment of an article.
N-grams involves a proprietary list of positive and negative two- to three-word phrases which are used to gauge a
more accurate sentiment in articles. These lists are compiled by financial analysts.
Next, a Deep Learning model predicts if the article is positve or negative based on the vector representation of its text. 
Finally, a meta model (ensemble learning) uses the output of all these 3 models to generate a final score.

**Quick Definition:** determines if the article was written positively or negatively by the author/editor.

###Examples

Articles with a negative sentiment about a plublicly traded equity - Tesco Inc

'Tesco strike to escalate' by http://tippfm.com/news/news_detail/tesco_strike_to_escalate

'Striking Tesco workers will not have Family Income Supplement suspended - Dept' by http://www.rte.ie/news/2017/0224/855211-tesco-dispute/

'Tesco workers shouldn’t lose Family Income Supplement, says O’Dea' byhttp://www.limerickpost.ie/2017/02/24/tesco-workers-shouldnt-lose-family-income-supplement-says-odea/

##Sentiment (story_sentiment)
An average of all the articles that fall into this story until now.
**Note:** If there is only one article in a story so far, then its *first_mention=true*, and *story_sentiment* equals *article_sentiment*.

**Quick Definition:** aggregates article sentiment and calculate the average sentiment for each story

###Examples
Looking at the recent **company earnings** story about **Southwestern Energy Company (SWN)** you can see mixed reviews from sources.
Positive articles - 

'SOUTHWESTERN ENERGY PIVOTS TO VALUE-ADDING GROWTH AND ANNOUNCES GUIDANCE FOR 2017' by envestorfirst.com

'Southwestern Energy Company (SWN) to Release Earnings on Friday' by baseballnewssource.com

Negative articles - 

'Earnings Miss Causes Southwestern Energy Company’s Stock to Tumble' by host.madison.com

'Earnings Miss Causes Southwestern Energy Company’s Stock to Tumble' by www.fool.com

But overall story sentiment indicates to be negative.

