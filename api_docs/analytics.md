---
layout: api
title: Zype Developer Portal | Analytics
permalink: /api_docs/analytics/
---

## Analytics

The Analytics API can be used to fetch site specific analytics that are also available in the Zype Admin. The API will make it possible for your team to download and use this data.

There are several endpoints for gathering data. Below are the endpoints and the types of data they return.

This API adheres to the (JSON API specs)[http://jsonapi.org/].

### Stream Hours
<pre><b>GET</b> https://analytics.zype.com/stream_hours</pre>

#### Parameters

Parameter  | Function                     | Type
---------  | --------                     | ----
api_key    | Admin API key                | String
start_date | Date on which to begin query | Date
end_date   | Date on which to end query   | Date

#### Response
<pre>
{
  "data": [
    {
      "type": "analytics",
      "attributes": {
        "date": "2018-02-19",
        "video_title": "Video Title",
        "video_id": "5a8b77b2f960de10b70080f0",
        "consumer_name": "Consumer Name",
        "consumer_id": "5497137269712f0ed52c0000",
        "device": "Desktop",
        "stream_hours": 11.39327730740749,
        "impressions": 8
      }
    }
  ]
}
</pre>
