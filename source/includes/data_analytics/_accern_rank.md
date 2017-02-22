##Accern Rank(overall_source_rank)
Accern Rank identifies if information from a source is prompt and if that information will go viral (get reposted by others).
In other words, it lets you know a source is usually the first to release a story and conveys if the stories published get republished by others.

**Note:** Source is the main website. Ex NYT or Bloomberg. Author is the writer within the organization.

**Quick Definition (overall_source_rank)** - determines if the author is reliable at releasing trending stories. 
**Quick Definition (overall_author_rank)** - determines if the source is reliable at releasing trending stories. 

###How is it calculated?
A graphical model takes into account historical data (past articles), how certain news appeared in the past and how the distribution of articles within a story looked like.
It checks which sources were faster/slower, which source in the past posted faster in comparison to other sources which then posted contextually similar articles.

###Examples:

##Accern Rank(event_source_rank)
Ranks are based on the same Accern Rank model which tries to predict reliability and their ability to post republished stories.
event_source_rank/event_author_rank is more precise. 
For ex. Tumblr posts rumors faster than others. Bloomberg posts financial docs faster than others.
Hence, it is possible for a source to have high rank for a specific type of event and lower ranks in other categories.

**Quick Definition (event_source_rank)** - determines if the source is reliable at releasing stories associated with a financial event. 

**Quick Definition (event_author_rank)** - determines if the source is reliable at releasing stories associated with a financial event.. 

###Examples:
 
- **Overall Source Rank (High)** - StreetInsider releases stories first, and their stories get republished by many other sources.
 
- **Event Source Rank (High)** - StreetInsider releases lawsuit stories first, and their lawsuit stories get republished by many other sources.

- **Overall Author Rank (Low-Mid)** - John Paul releases stories on StreetInsider first, but his stories don’t get republished by any other authors.

- **Event Author Rank (Low-Mid)** - John Paul releases lawsuit stories on StreetInsider late, but his stories are republished by some authors.