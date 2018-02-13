---
layout: api
title: Zype Developer Portal | Video Entitlements
permalink: /api_docs/video_entitlements/
---

## Video Entitlements

<hr />

### Check Video Entitlement

Check if a consumer has access to a video (entitled).

<pre>
<b>GET</b> https://api.zype.com/videos/[video_id]/entitled
</pre>

#### Macros

Macro | Function | Type
----- | -------- | ----
video_id | Video object ID | String

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
access_token | OAuth token of a consumer | String

#### Errors

**422**: A consumer does not have permission to play this video

<hr />
### List Video Entitlements
<pre>
<b>GET</b> https://api.zype.com/consumer/videos
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
created_at | Filter records by created date using times in ISO8601 format (Example: 2017-01-01T00:00:00-00:00) or Unix timestamps (Example: 1483228800) <br />**Note**: Range filters can be applied by adding a suffix: '.gt', '.gte', '.lt', 'lte' (Example: created_at.gte) | Date
expires_at | Filter records by expire date using times in ISO8601 format (Example: 2017-01-01T00:00:00-00:00) or Unix timestamps (Example: 1483228800) <br />**Note**: Range filters can be applied by adding a suffix: '.gt', '.gte', '.lt', 'lte' (Example: expires_at.gte) | Date
id        | Filter records by ID | String
id!       | Exclude records by ID | String
order     | Sort records in ascending or descending order (Example: asc/desc) | String
sort | Sort records on the specified field | String
page | The page number of records to return (Example: 1) | Integer
per_page | The number of records to return (Example: 10) | Integer
q         | Filter records by keyword | String
transaction_id | Filter records by transaction ID | String
transaction_type | Filter records by the type of transaction that created the entitlement (Example: purchase) | String
video_id | Filter records by video ID | String

### List Video Entitlements for a specific Consumer
<pre>
<b>GET</b> https://api.zype.com/consumers/[consumer_id]/videos
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
consumer_id | ID of the consumer whose video entitlements will be retrieved | String

### Create a Video Entitlement
<pre>
<b>POST</b> https://api.zype.com/consumers/[consumer_id]/videos
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
consumer_id | ID of the consumer whose video entitlement will be created | String
entitlement[video_id] | ID of the [video](/api_docs/video) you wish the consumer to have access to | String
entitlement[transaction_id] | ID of the transaction that happened to allow the consumer to have access to the video | String
entitlement[transaction_type] | Type of transaction (Example: purchase) | String
entitlement[expires_at] | When the entitlement expires | Date

### Retrieve a Video Entitlement
<pre>
<b>GET</b> https://api.zype.com/consumers/[consumer_id]/videos/[id]
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
consumer_id | ID of the consumer whose video entitlement will be retrieved | String
id | ID of the record to retrieve | String

### Update a Video Entitlement
<pre>
<b>PUT</b> https://api.zype.com/consumers/[consumer_id]/videos/[id]
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
consumer_id | ID of the consumer whose video entitlement will be updated | String
id | ID of the record to retrieve | String
entitlement[video_id] | ID of the [video](/api_docs/videos) you wish the consumer to have access to | String
entitlement[transaction_id] | ID of the transaction that happened to allow the consumer to have access to the video | String
entitlement[transaction_type] | Type of transaction (Example: purchase) | String
entitlement[expires_at] | When the entitlement expires | Date

### Delete a Video Entitlement
<pre>
<b>DELETE</b> https://api.zype.com/consumers/[consumer_id]/videos/[id]
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
consumer_id | ID of the consumer whose video entitlement will be deleted | String
id | ID of the video entitlement | String

### Video Entitlement Object

<pre>
{
  _id: "574df05109838853df000001",
  consumer_id: "5543e4a269702d070d330600",
  created_at: "2016-05-31T16:13:05.437-04:00",
  expires_at: null,
  transaction_id: '57214ac2098388d3a800000c',
  transaction_type: 'purchase',
  updated_at: "2016-05-31T16:13:05.437-04:00",
  video_id: "574decf509838854f1000183",
  video_title: "Sample Video"
}
</pre>
