---
layout: api
title: Zype Developer Portal | Playlists
permalink: /api_docs/playlist_entitlements/
redirect_to: https://docs.zype.com/reference#playlist-entitlements
---

## Playlist Entitlements

<hr>
### List Playlist Entitlements
<pre><b>GET</b> https://api.zype.com/consumer/playlists</pre>

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
playlist_id | Filter records by playlist ID | String
q         | Filter records by keyword | String
transaction_id | Filter records by transaction ID | String
transaction_type | Filter records by the type of transaction that created the entitlement (Example: purchase) | String

### List Playlist Entitlements for a specific Consumer
<pre>
<b>GET</b> https://api.zype.com/consumers/[consumer_id]/playlists
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
consumer_id | ID of the consumer whose playlist entitlements will be retrieved | String

### Create a Playlist Entitlement
<pre>
<b>POST</b> https://api.zype.com/consumers/[consumer_id]/playlists
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
consumer_id | ID of the consumer whose playlist entitlement will be created | String
entitlement[playlist_id] | ID of the [playlist](/api_docs/playlists) you wish the consumer to have access to | String
entitlement[transaction_id] | ID of the transaction that happened to allow the consumer to have access to the Playlist | String
entitlement[transaction_type] | Type of transaction (Example: purchase) | String
entitlement[expires_at] | When the entitlement expires | Date

### Retrieve a Playlist Entitlement
<pre>
<b>GET</b> https://api.zype.com/consumers/[consumer_id]/playlists/[id]
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
consumer_id | ID of the consumer whose playlist entitlement will be retrieved | String
id | ID of the record to retrieve | String

### Update a Playlist Entitlement
<pre>
<b>PUT</b> https://api.zype.com/consumers/[consumer_id]/playlists/[id]
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
consumer_id | ID of the consumer whose playlist entitlement will be updated | String
id | ID of the record to update | String
entitlement[playlist_id] | ID of the [playlist](/api_docs/playlists) you wish the consumer to have access to | String
entitlement[transaction_id] | ID of the transaction that happened to allow the consumer to have access to the Playlist | String
entitlement[transaction_type] | Type of transaction (Example: purchase) | String
entitlement[expires_at] | When the entitlement expires | Date

### Delete a Playlist Entitlement
<pre>
<b>DELETE</b> https://api.zype.com/consumers/[consumer_id]/playlists/[id]
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
consumer_id | ID of the consumer whose playlist entitlement will be deleted | String
id | ID of the playlist entitlement | String

### Playlist Entitlement Object

<pre>
{
  _id: "574df05109838853df000001",
  consumer_id: "5543e4a269702d070d330600",
  created_at: "2016-05-31T16:13:05.437-04:00",
  expires_at: null,
  transaction_id: '57214ac2098388d3a800000c',
  transaction_type: 'purchase',
  updated_at: "2016-05-31T16:13:05.437-04:00",
  playlist_id: "574decf509838854f1000183",
  playlist_title: "Sample Playlist"
}
</pre>
