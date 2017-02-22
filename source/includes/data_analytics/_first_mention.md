##First Mention (first_mention)

###What is it?
Whenever a financial news story breaks out, many articles (mentions) get published about the same story.
First Mention tells us if this article is the first to break that new story.

**Quick Definition:** A story that has not been mentioned on the internet for at least two weeks.

###How is it created?
The story classification model checks on a given article for a similar theme(combination of event and companies) in the last 2 weeks. 
If it finds one, it groups the article with this existing theme.
Otherwise, it assigns a new story for this article and this article's first mention field is set to *'true'*.

###Examples
September 1st, 2016 - (AAPL, MSFT) + Lawsuit - first_mention = **TRUE**

September 12th, 2016 - (AAPL, MSFT) + Lawsuit - first_mention = **FALSE**