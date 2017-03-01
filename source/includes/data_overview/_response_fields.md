## Data Attributes
> Sample object (article)

Table illustrates all the attributes in a single object *(article)* of the Accern API response

```json
{
    "id": 1774184,
    "article_id": {
      "$oid": "589b44a569fe9f7f77024f4a"
    },
    "article_sentiment": 0.098,
    "article_traffic": null,
    "article_type": "blog",
    "article_url": "http://feedproxy.google.com/~r/RedmondPie/~3/mF7K04DF1y4/",
    "author_id": null,
    "correlations": null,
    "entities": [
      {
        "name": "Apple Inc.",
        "type": "Public",
        "index": "S&P 500, Russell 1000, Russell 3000, Wilshire 5000, BARRON'S 400, NASDAQ 100",
        "region": "North America",
        "sector": "Technology",
        "ticker": "AAPL",
        "country": "United States",
        "exchange": "NASDAQ",
        "industry": "Computer Manufacturing",
        "entity_id": "EQ0010169500001000",
        "global_id": "BBG000B9XRY4",
        "competitors": [
          "GOOG",
          "HPQ"
        ]
      },
      {
        "name": "Amazon.com, Inc.",
        "type": "Public",
        "index": "S&P 500, Russell 1000, Russell 3000, Wilshire 5000, NASDAQ 100",
        "region": "North America",
        "sector": "Consumer Services",
        "ticker": "AMZN",
        "country": "United States",
        "exchange": "NASDAQ",
        "industry": "Catalog/Specialty Distribution",
        "entity_id": "EQ0021695200001000",
        "global_id": "BBG000BVPV84",
        "competitors": [
          "AAPL",
          "BKS"
        ]
      }
    ],
    "event_author_rank": [
      {
        "author_rank": 4,
        "event_group": "Employment Actions"
      },
      {
        "author_rank": 4,
        "event_group": "Employment Actions"
      }
    ],
    "event_groups": [
      {
        "type": "Recruitment",
        "group": "Employment Actions"
      },
      {
        "type": "Layoff",
        "group": "Employment Actions"
      }
    ],
    "event_impact_score": {
      "overall": 40.88471673254282,
      "on_entities": [
        {
          "entity": "AAPL",
          "on_entity": 31
        },
        {
          "entity": "AMZN",
          "on_entity": 32
        }
      ]
    },
    "event_source_rank": [
      {
        "event_group": "Employment Actions",
        "source_rank": 6
      },
      {
        "event_group": "Employment Actions",
        "source_rank": 6
      }
    ],
    "event_summary": {
      "group": "",
      "theme": "",
      "topic": "",
      "action": "",
      "sub-theme": "",
      "acting_party": ""
    },
    "first_mention": false,
    "harvested_at": "2017-02-08 16:17:39 UTC",
    "overall_author_rank": 5,
    "overall_source_rank": 6,
    "source_id": null,
    "story_id": {
      "$oid": "589a6b6469fe9f7f70ac1df6"
    },
    "story_saturation": "high",
    "story_sentiment": 0.072,
    "story_shares": null,
    "story_volume": 58
  }
```

Attributes | Type | Description
-----------|------|-------------
**id** | integer | unique id for feed (1 or greater)
**article_id.$oid** | string |  unique id per article 
**article_sentiment** | decimal | determines if article was [written positively/negatively](#sentiment-article_sentiment) (-1.000 - 1.000)
**article_type** | string | determines the source of an information (ex. blog, article, tweet)
**article_url** | url string | original link to article
**entities** | list | List of associated equities objects that are identified for this article
**entities_name** | string | name of the company (8,000+ U.S. public equities)
**entities_type** | string | Classifying if it's publicly traded (ex. public)
**entities_index** | string | Comma-separated string of indices company is listed on
**entities_region** | string | Region of the company's headquarters
**entities_sector** | string | Sector of the company
**entities_ticker** | string | Ticker of the company
**entities_country** | string | Country of company's headquarters
**entities_exchange** | string | Exchange the company is traded on
**entities_industry** | string | Industry of the company
**entities_entity_id** | string | Entity level ID of the company, derived from Bloomberg Open Symbology
**entities_global_id** | string | Unique global ID of the company, derived from Bloomberg Open Symbology
**entities_competitors** | list | List of top three competitors associated with the company
**event_author_rank** | list | Each object indicates the [author's reliability](#accern-rank-event_source_rank) in reporting on specific events
**event_groups** | list | Each object has a major event group and a subsection of that group
**event_groups_type** | string | A subsection of an event group for more detail
**event_groups_group** | string | A major event i.e. event group
**event_impact_score** | object | Calculates the article's impact i.e. chance of affecting the associated company's stock price
**event_impact_score_overall** | decimal | Determines chance of [event affecting stock prices in general](#impact-_overall) by end of trading day
**event_impact_score_on_entities** | list |Determines chance of [event affecting associated company's stock price](#impact-_on_entities) by end of trading day
**event_source_rank** | list | Each object indicates the [source's reliability](#accern-rank-event_source_rank) in reporting on specific events
**event_summary_topic** | string | Level 1 event category
**event_summary_group** | string | Level 2 event category
**event_summary_theme** | string | Level 3 event category
**event_summary_sub_theme** | string | Level 4 event category
**event_summary_action** | string | action of an event
**event_summary_acting_party** | string | parties associated with the event
**first_mention** | boolean | If this article is the first one to [break this new story](#first-mention-first_mention)
**harvested_at** | datetime | UTC formatted time when Accern received article
**overall_author_rank** | integer | rank (1-10) of how [reliable author](#accern-rank-overall_source_rank) is at releasing articles in general
**overall_source_rank** | integer | rank (1-10) of how [reliable source](#accern-rank-overall_source_rank) is at releasing articles in general
**story_saturation** | string | how much [exposure](#saturation-story_saturation) this story has currently. ex. high, mid, low
**story_sentiment** | decimal | [+ve/-ve sentiment score of the story](#sentiment-story_sentiment) by averaging related articles' sentiment published so far
**story_volume** | integer | number of articles associated with this story until now


<aside class="notice">
Fields like entities and event_groups have NESTED ATTRIBUTES.
Hence, attributes like entities_name, entities_ticker, and event_groups_type, mentioned in the table, actually refer to the nested name, ticker, and type attributes respectively.
</aside>