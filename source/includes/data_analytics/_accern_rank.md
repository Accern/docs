##Accern Rank(overall_source_rank)
**What is it?** Accern Rank identifies if the information from a source is posted promptly and if that information will go viral (similar articles published by others).
**Rank 1** is lowest and **Rank 10** is highest.
**In other words,** it lets you know which sources usually are among the first to publish articles on a new story and also informs if they have a knack at posting on stories that become wide spread.

**Quick Definition:**

* **overall_source_rank** - determines if the SOURCE is *reliable* at releasing trending stories. i.e. reliable indicating ability to post early and trending indicating potential of wide spread stories.

* **overall_author_rank** - determines if the AUTHOR is *reliable* at releasing trending stories. 

<aside class="notice">
Difference between source and author? Source is the website. Ex NYT or Bloomberg. Author is the writer within the organization.
In the below examples we use fictional name John Paul.
</aside>

**How is it created?** A graphical model takes into account historical data (past articles), how certain news appeared in the past and how the distribution of articles within a story looked like.
It checks in the past, which sources posted faster in comparison to other sources which then posted contextually similar articles.

**Examples**

- **Overall Source Rank (High)** - StreetInsider releases stories first, and their stories get republished by many other sources.

- **Overall Author Rank (Low-Mid)** - *John Paul*<sup>*</sup> releases stories on StreetInsider first, but his stories don’t get republished by any other authors.

<sup>*</sup>
##Accern Rank(event_source_rank)
**What is it?** Ranks are based on the same Accern Rank model which tries to predict promptness and ability to post republished stories.
**Rank 1** is lowest and **Rank 10** is highest.
**event_source_rank/event_author_rank** is more precise. 
For ex. Tumblr posts rumors faster than others. Bloomberg posts financial docs faster than others.
It would be prudent to the client to notice that sources will have varied ranks for different events.

**Quick Definition:**

* **event_source_rank** - determines if the SOURCE is *reliable* at releasing articles associated with a financial event. 

* **event_author_rank** - determines if the AUTHOR is *reliable* at releasing articles associated with a financial event.. 

**How is it created?** The ranking model is the same. Ranks are calculated by filtering based on financial events.

**Examples**
 
- **Event Source Rank (High)** - StreetInsider releases lawsuit stories first, and their lawsuit stories get republished by many other sources.

- **Event Author Rank (Low-Mid)** - *John Paul*<sup>*</sup> releases lawsuit stories on StreetInsider late, but his stories are republished by some authors.