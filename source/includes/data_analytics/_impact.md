##Impact

Retrospective metric. Looking back in the history, we try to see how market behaved for a past similar event. Gives you probability that when a certain type of theme/event appears in media, will the stock of the company move up/down by more than 1% by EOD.
Overall Impact checks how an event like 'Company Earnings' generally has high impact compared to other events.
Entity Impact Score is more precise. Ex, for Apple, how did 'Mergers & Acquisition' event affect them in the past. But this event can vary for different companies in their impact.
Overall Impact Score, is an average across al the entity_impact_scores.

`Definition: determine whether an event has a chance of affecting the stock price of the related company or in general by more than 1% at the end of the trading day.`

Process for Computing Impact (historical analysis)

Overlay 3-plus years of events data with market data to determine if the event has a chance of moving the stock price of the company mentioned or in general by more than 1% by the end of the day.

**event_impact_score_overall** - `Definition: determines if an event has a chance of affecting stock prices of companies in general by more than 1% at the end of the trading day.`

**event_impact_score_on_entities** - `Definition: determines if an event has a chance of affecting the stock price of the mentioned company by more than 1% at the end of the trading day.`

Examples:

- Event Impact Score Overall (High) - In the past 3 years, whenever a lawsuit happened, it affected the stock prices of companies in general by 1% or more EOD.

- Event Impact Score On Entities (High) - In the past 3 years, whenever a lawsuit happened in relation to AAPL, it affected the stock price of AAPL by 1% or more EOD.