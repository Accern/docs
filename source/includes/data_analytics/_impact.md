##Impact (_overall)
**What is it?** When a certain type of story appears in media, calculate the probability that the stock price of the company moves up/down by more than 1% by EOD.
Overall Impact score checks how an event like **Company Earnings** generally has high impact compared to other events.
Overall Impact Score is an average across all the **entity_impact_scores** for different companies.

**Quick Definition (event_impact_score_overall):** determines if an event has a chance of affecting stock prices of companies in general by more than 1% at the end of the trading day.

**How is it created?** An example of a retrospective metric. Looking back in history archive, how market behaved for a past similar event is evaluated.
In brief, by overlaying 3+ years of financial events data with stock prices market data, we determine if the event has a chance of moving the stock price of companies in general by more than 1% by the end of the day.

**Examples**

- Event Impact Score Overall (High) - In the past 3 years, whenever a lawsuit happened, it affected the stock prices of companies in general by 1% or more EOD.

##Impact (_on_entities)
**What is it?** Entity Impact Score is more precise as it it returns a probability that particular event will affect SPECIFIC equities.
For example, **event_impact_score_on_entities** of 90 for *Apple and 'Mergers & Acquisition' event* conveys this sort of story/theme moved the market before in the past and there is a high likelihood now as well.
Also, this event can vary in impact score for different companies.

**Quick Definition (event_impact_score_on_entities:)** determines if an event has a chance of affecting the stock price of the mentioned company by more than 1% at the end of the trading day.

**How is it created?** Using the same procedure to calculate overall impact score of an event, this process filters based on every entity and calculates respective probabilities.

**Examples**

> Sample Snippet

```json
{
    "....": "...",
    "event_groups": [
      {
        "type": "Financial Results",
        "group": "Company Earnings"
      }
    ],
    "event_impact_score": {
      "overall": 48.55540720961282,
      "on_entities": [
        {
          "entity": "EBAY",
          "on_entity": 26
        },
        {
          "entity": "AMZN",
          "on_entity": 36
        }
      ]
    }
}
```

- Considering the **right-side snippet**, we see that the results of Company Earnings reports have a lower impact on EBay and Amazon compared to all the companies overall.

- Similarly, an event involving Criminal Actions/Fraud may have a high overall impact (event_impact_score.overall), but certain entities like Google are impacted 50% less. (event_impact_score.on_entities.on_entity)