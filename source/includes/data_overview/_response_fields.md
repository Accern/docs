### Response Fields
> The below example json is a single story response.

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
**id** | integer |
**article_id.$oid** | string |  
**article_sentiment** | decimal | +ve/-ve sentiment score of article
**article_type** | string | ex. blog, article, tweet
**article_url** | string |
**entities** | list | List of associated equities objects that are identified for this article
**event_author_rank** | list | Each oject indicates the author's reliability in reporting on these financial events
**event_groups** | list | Each object has a major event group and a subsection of that group
**event_impact_score** | object | Calculates the article's impact i.e. chance of affecting the associated companys' stock price
**event_source_rank** | list | Each oject indicates the sources's reliability in reporting on these financial events
**event_summary** | object | A brief categorization of the associated financial event
**first_mention** | boolean | If this article is the first one to break/mention a new story
**harvested_at** | datetime | UTC formatted time when article was scraped
**overall_author_rank** | integer | rank (1-10) of how reliable author is at releasing articles
**overall_source_rank** | integer | rank (1-10) of how reliable source is at releasing articles
**story_saturation** | string | how much exposure this story has currently. ex. high, mid, low
**story_sentiment** | decimal | +ve/-ve sentiment score of the story taking into account the articles published so far
**story_volume** | integer | number of articles associated with this story

*More tables expressing nested fields like entities, event_author_rank, event_groups, etc.. *