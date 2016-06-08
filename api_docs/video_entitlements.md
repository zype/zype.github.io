---
layout: api
title: Zype Developer Portal | Video Entitlements
permalink: /api_docs/video_entitlements/
---

## Video Entitlements
<hr />
### List Video Entitlements
<pre>
<b>GET</b> https://api.zype.com/consumer/videos
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
created_at | Filter records by created date. Greater or less than filters can be used by adding a suffix (Example: created_at.gte) | Date
expires_at | Filter records by expire date. Greater or less than filters can be used by adding a suffix (Example: expires_at.gte) | Date
id        | Filter records by ID | String
id!       | Exclude records by ID | String
order     | Sort records in ascending or descending order (Example: asc/desc) | String
page | The page number of records to return (Example: 1) | Integer
per_page | The number of records to return (Example: 10) | Integer
q         | Filter records by keyword | String
transaction_id | Filter records by transaction ID | String
transaction_type | Filter records by the type of transaction that created the entitlement (Example: purchase) | String
video_id | Filter records by video ID | String

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