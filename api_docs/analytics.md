---
layout: api
title: Zype Developer Portal | Analytics
permalink: /api_docs/analytics/
---

## Analytics

Zype's video analytics API allows you to run custom queries for stream hours and impressions data based on the following dimensions:
  * date range
  * video
  * consumer
  * device type

The API will make it possible for your team to download and use this data in either JSON or CSV format.

**Please note that analytics data for this API is available from January 1, 2018 forward.**

This API adheres to the (JSON API specs)[http://jsonapi.org/].

#### How to Request Data
<pre>
curl https://analytics.zype.com/v1/stream_hours \
-d api_key=YOUR-API-KEY \
-d filters[start_date_gte]='02-26-2018 00:00' \
-d filters[device_name_eq]=FireTV \
-d group_by[]=consumer_name
-d view_mode=summary
</pre>

#### Filtering
You can filter on any of the data that is returned in the request. To filter, simply attach a filter type to the attribute you are filtering by.

For instance, to find all videos with ID of 5a93251d526ecd11b50142fa, use `video_id_eq: 5a93251d526ecd11b50142fa`. To find all records with a date after February 26th, use `start_date_gt: 02-26-2018 00:00`.
These are the attributes you are able to filter with:
* start_date
* video_id
* video_title
* consumer_name
* consumer_id
* consumer_email
* device_name
* monetized_option
* country_code
* country_name

We provide the following filter types:
* gt (greater than)
* gte (greater than or equal to)
* lt (less than)
* lte (less than or equal to)
* eq

#### Group By
You can group the information by a specific attribute. Grouping allows you to add up data related to the attribute you are grouping by. For instance, if you want to find the number of stream hours and impressions for each video title, you add `group_by[]: video_title`. The `[]` are there because you are allowed to group by more than one attribute and must be present.

#### Sorting
You can sort the response by any values that are sortable. Default sort is `asc` but you can also sort by `desc`. Attach `asc` or `desc` to the attribute you want to sort by. An example request looks like `sort_by: consumer_name_asc`. This sorts by the consumer name in ascending order.
summary/detailed mode

#### Dates
**Dates must be formatted in a specific way**. This makes it easy to do queries and gives you granular control over date ranges. Use `mm-dd-yyyy hh:mm` format.

#### View Mode
You have two modes to view your data - `summary` and `detailed`.
* summary - allows you to group information to see a summary of stream hours and impressions.
* detailed - responds with all information for each record in your analytics.

You can specify the mode with `view_mode: summary`.

#### Defaults
* date range - If no dates are supplied, you will receive data from two weeks ago until today
* view_mode - `detailed`
* group_by - If you specify `summary` as the `view_mode` and do not specify a `group_by` option, then `start_date` will be used.

#### JSON or CSV
JSON is the default response format.

Tack on `.csv` to the url to receive CSV - https://analytics.zype.com/v1/stream_hours.csv?<query_params>

#### Rate Limits
You are not allowed to make more than 10 requests/minute.

---

<pre><b>GET</b> https://analytics.zype.com/v1/stream_hours</pre>

#### Parameters

Parameter                   | Description                | Type
---------                   | -----------                | ----
api_key                     | Admin API key              | String
filters[start_date]         | Date to filter by          | String
filters[device_name]        | Device to filter by        | String
filters[video_title]        | Filter by video_title      | String
filters[video_id]           | Filter by video_id         | String
filters[stream_type]        | Filter by stream_type      | String
filters[consumer_id]        | Filter by consumer_id      | String
filters[monetized_option]   | Filter by monetized_option | String
filters[country_code]       | Filter by country_code     | String
filters[country_name]       | Filter by country_name     | String
filters[consumer_email]     | Filter by consumer_email   | String
group_by[] start_date       | Group by start_date        | String
group_by[] device_name      | Group by device_name       | String
group_by[] video_title      | Group by video_title       | String
group_by[] video_id         | Group by video_id          | String
group_by[] stream_type      | Group by stream_type       | String
group_by[] consumer_id      | Group by consumer_id       | String
group_by[] monetized_option | Group by monetized_option  | String
group_by[] country_code     | Group by country_code      | String
group_by[] country_name     | Group by country_name      | String
group_by[] consumer_email   | Group by consumer_email    | String


#### Response
Detailed Response
<pre>
{
  "data": [
    {
      "type": "analytics",
      "attributes": {
        "player_request_id": "5a8f134dc1205b0001000008",
        "device_name": "Desktop",
        "video_title": "Fancy Title",
        "stream_hours": 2.46894656711155,
        "stream_type": "vod",
        "video_id": "5a93251d526ecd11b50142fa",
        "consumer_id": "573cbgbb1d2e230d12001f34",
        "monetized_option": "paid",
        "country_code": "US",
        "consumer_email": "bonzaa140@hotmail.com",
        "country_name": "United States",
        "bytes_streamed": 72812197.0,
        "consumer_name": "Bonnie Sparrow",
        "start_date": "2018-02-27T00:00:00.000Z"
      }
    }
  ]
}
</pre>

Summary Response
<pre>
{
  "data": [
    {
      "type": "parameters",
      "attributes": {
        "filters": {
          "start_date": {
            "gte": "2018-02-26T00:00:00.000Z"
          },
          "video_id": {
            "eq": "5a93251d526ecd11b50142fa"
          },
          "consumer_id": {
            "eq": "573cbgbb1d2e230d12001f34"
          }
        },
        "group_by": [
          "video_title"
        ]
      }
    },
    {
      "type": "analytics",
      "attributes": {
        "video_title": "Fancy Title",
        "start_date": "2018-02-27T00:00:00.000Z",
        "video_id": "5a93251d526ecd11b50142fa",
        "consumer_id": "573cbgbb1d2e230d12001f34",
        "impressions": 2,
        "stream_hours": 4.0576554022895
      }
    }
  ]
}
</pre>

### Use Cases
Assume current date is March 1.

Stream hours and impressions each video has received for the month of February

Parameter                | Value
---------                | -----
filters[start_date_gte]  | 02-01-2018 00:00
filters[start_date_lte]  | 02-28-2018 59:59
group_by[]               | video_title
view_mode                | summary

Stream Hours and impressions from a specific consumer over the last two weeks

Parameter               | Value
---------               | -----
filters[start_date_gte] | 02-14-2018 00:00
filters[start_date_lte] | 02-28-2018 59:59
filters[consumer_id_eq] | 573cbgbb1d2e230d12001f34
group_by[]              | consumer_name
view_mode               | summary

Stream Hours and impressions from all devices since 3rd week of February

Parameter               | Value
---------               | -----
filters[start_date_gte] | 02-21-2018 00:00
filters[start_date_lte] | 02-28-2018 59:59
group_by[]              | device_name
view_mode               | summary

Stream Hours and impressions for FireTV device since 3rd week of February

Parameter               | Value
---------               | -----
filters[start_date_gte] | 02-21-2018 00:00
filters[start_date_lte] | 02-28-2018 59:59
filters[device_name_eq] | FireTV
group_by[]              | device_name
view_mode               | summary

Filter all data by video ID over last 3 weeks

Parameter               | Value
---------               | -----
filters[start_date_gte] | 02-07-2018 00:00
filters[start_date_lte] | 02-28-2018 59:59
filters[device_name_eq] | FireTV
group_by[]              | device_name
view_mode               | summary
