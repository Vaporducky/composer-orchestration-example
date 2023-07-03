This is a small project regarding the architecture of small company "Bikeshare Enterprise".

Given a range of dates (E.g. Initial_day=2021-01-01,end_day=2022-01-02) calculates the total cost for trip, it means, given the duration_minutes of a trip, calculate the trip cost, the cost per minute is 0.6 USD.

1. A Cloud Function publishes a message (ingested through HTTPS) in a PubSub topic
2. A Cloud Function is triggered when a message is Published in the topic
3. DataFlow *batch* job is submitted through the previous Cloud Function
4. Data is load/truncated into a BQ table 


