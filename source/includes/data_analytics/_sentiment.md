##Sentiment Analysis
**article_sentiment** - `Definition: determines if the article was written positively or negatively by the author.`
Sentiment of the article written by the author/editor.

**story_sentiment** - `Definition: aggregates article sentiment and calculate the average sentiment for each story.`
An average of all the articles that fall into this story until now. If there is only one article, then first_mention=true, and story_sentiment equals article_sentiment.

Accern sentiment = bag of words + n-grams + deep-learning

3-Step Process for Computing Accern Sentiment

- Step 1: bag-of-words approach
A proprietary list of 300,000-plus positive and negative words, differently weighed, were used to gauge a base sentiment of an article.

- Step 2: n-grams
A proprietary list of positive and negative two- to three-word phrases was used to gauge a
more accurate sentiment in articles. 

- Step 3: deep learning
A few finance scholars manually identify the sentiment of a few thousand articles, which were used as a training set for future articles.

3 parallel processes. Financial phrases created by our analysts. Deep Learning model that predicts if the article is positve or negative based on the representation of text. Then a metamodel (ensemble learning) that uses output of all these 3 models to generate a final score.
 