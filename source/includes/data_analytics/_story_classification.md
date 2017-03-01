##Unique Stories (story_id)

**What is it?** Financial news stories are published on the web and social media in many forms. For ex. articles, tweets, & SEC filings. 
We scour millions of these articles talking about financial events and group them into similar **stories**.
Each **story** specifies 2 important details. 
The **equities** that are being talked about (currently amongst 8000+ US public equities) and
a description of the associated **financial events** (currently 1000+ financial event distinctions available)

**Quick Definition:** a story is an event that involves a company.

**How is it created?** Every day we scrape a million+ articles of various types such as blogs, tweets, SEC filings and news articles. 
These **mentions** go through the [story classification model](#story-classification) to identify the associated **equities** (from the existing 8000+ US public equities)
and the associated **financial event** (1000+ distinctions available). 
All mentions that are similar in the above entities are grouped together into their own **stories**.
Each story which is a combination of companies and events is given unique ids - (**story_id**).

**Examples**

An example of a big, viral story regarding **Google** and **Legal Actions** consists of articles below that are all talking about similar information.

* 'Google alleges Uber stole its self-driving secrets' by Livemint.com

* 'Google accuses Uber of stealing self-drive technology' by Business-standard.com

* 'Lawsuit: Google self-driving car spinout Waymo claims Uber using stolen laser-mapping technology' by geekwire.com

* 'Waymo: Uber stole our self-driving car tech' by cnet.com

An example of a story reporting on a **Rumour** about **Apple** can be seen to have been initially posted on a blog before finally showing up on other sources wih bigger reach.

* "Apple reportedly plans to 'significantly' expand Seattle office after Turi acquisition" by bizjournals.com

* "Apple plans expansion of artificial intelligence efforts in Seattle" by forums.imore.com