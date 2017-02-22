##First Mention (first_mention)

###What is it?
Whenever story classification model checks on a given article for a similar theme in the last 2 weeks for the same set of companies. If it finds, it groups with this existing theme.
Else it assigns a new story for this article. Hence, this article is marked as first mention as it breaks the story.

Whenever a financial news story breaks out, many articles (mentions) get published about the same story.
It may be a tweet from a top financial analyst or even a SEC filing that documents some aspect of the story.

`Definition: A story that has not been mentioned on the internet for at least two weeks.`

###How is it created?

###Examples
September 1st, 2016 - (AAPL, MSFT) + Lawsuit - first_mention = **TRUE**

September 12th, 2016 - (AAPL, MSFT) + Lawsuit - first_mention = **FALSE**