##Accern Rank

What? A main IP. Identifies if information from a source is prompt/quick and if that information will go viral/ get reposted by others.
How? A graphical model that takes into account historical data (past news), how certain news appeared in the past and how distribution of articles within a story looked like.
Checks which sources were faster, slower, etc. Which source in the past posted faster in the past, and then these other sources posted contextually similar articles.

Source is the main website. Ex NYT or Bloomberg. Author is within the organization.
Ranks are based on Accern Rank model. General model tries to predict reliability and their ability to post republished stories.
Event_source_rank is more precise. Example. Tumblr posts rumors faster than others. Bloomberg posts financial docs faster than others.
Hence, possible for source has high rank to post for a certain event compared to others.

**overall_source_rank** - Definition: determines if the author is reliable at releasing articles. 

**overall_author_rank** - Definition: determines if the source is reliable at releasing articles. 

**event_source_rank** - Definition: determines if the source is reliable at releasing articles associated with a financial event. 

**event_author_rank** - Definition: determines if the source is reliable at releasing articles associated with a financial event.. 

Accern rank = timeliness + republished rate

2-Step Process for Computing Accern Rank

- timeliness
Determines if the source or author is usually the first to release a story

- republished rate
Determines if the story released by the source or author gets republished by many others 

Examples:
 
- **Overall Source Rank (High)** - StreetInsider releases stories first, and their stories get republished by many other sources.
 
- **Event Source Rank (High)** - StreetInsider releases lawsuit stories first, and their lawsuit stories get republished by many other sources.

- **Overall Author Rank (Low-Mid)** - John Paul releases stories on StreetInsider first, but his stories don’t get republished by any other authors.

- **Event Author Rank (Low-Mid)** - John Paul releases lawsuit stories on StreetInsider late, but his stories are republished by some authors.