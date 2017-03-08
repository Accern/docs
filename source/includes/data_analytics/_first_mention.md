##First Mention (first_mention)
**What is it?** Whenever a financial news story breaks out, many articles (mentions) get published about the same story.
First Mention tells us if the article is the **FIRST** to break that new story.

**Quick Definition:** A story that has not been mentioned on the internet for at least 2 weeks.

**How is it created?** The story classification model extracts a theme(combination of event and companies) from input article. It then searches for highly similar themes in the last 2 weeks. 

If it finds one, it groups this article with the existing story (theme) and sets it's **first_mention** to **FALSE**.
Otherwise, it creates a new story and this article's **first_mention** attribute is set to **TRUE**.

**Examples**

In brief, the power of knowing an article is the first to break a new story ->

date | headline | first_mention
-----|---------|-----
08:50 AM 28 Feb | Xbox launches Netflix-like service for gamers | TRUE
11:35 AM 28 Feb | GameStop stock price tanks after Microsoft announces new digital-gaming service | FALSE