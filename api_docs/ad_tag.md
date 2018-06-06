---
layout: api
title: Zype Developer Portal | Ad Tags
permalink: /api_docs/ad_tags/
redirect_to: https://docs.zype.com/reference#ad-tags
---

## Ad Tags

<hr>
### List Ad Tags
<pre><b>GET</b> https://api.zype.com/ad_tags</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | Filter records by ID | String
id!       | Exclude records by ID | String
active | Filter by active, inactive, or all records (Example: true) | String
name | Filter by name | String
disabled | Filter by disabled | boolean
scope | Filter by assigned scope. Options are 'library' or 'video' | String
order     | Sort records in ascending or descending order (Example: asc/desc) | String
page | The page number of records to return (Example: 1) | Integer
per_page | The number of records to return (Example: 10) | Integer
q         | Filter records by keyword | String
sort      | Sort records on the specified field | String

### Create an Ad Tag
<pre><b>POST</b> https://api.zype.com/ad_tags</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
ad_tag[name] | Name of the ad tag | String
ad_tag[active] | Optional. Default set to 'true' | Boolean
ad_tag[interval_count] | Optional. How many times a video or videos in a collection will play before a single user gets an ad | Integer
ad_tag[scope] | Optional. Whether `interval_count` applies to single video ('video') or a collection of videos ('library'). Default is 'library'. | String
ad_tag[disabled] | Optional. Pass 'true' to disable a video. Default is 'false' | Boolean
ad_tag[\_type] | Optional. One of "AdTag::Vast" or "AdTag::Googima" | String
ad_tag[device_category_id] | ID of [DeviceCategory](/api_docs/device_categories) | String
ad_tag[device_id] | ID of [Device](/api_docs/devices) to display AdTag on | String
ad_tag[revenue_partner_id] | ID of revenue partner | String
ad_tag[vmap] | If Ad Tag is a vmap. Default is 'false' | Boolean
ad_tag[tag] | URL of the ad | String

### Retrieve an Ad Tag
<pre><b>GET</b> https://api.zype.com/ad_tags/[id]</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id | ID of the record to retrieve (Example: 5389352e69702d401b000000) | String

### Update an Ad Tag
<pre><b>PUT</b> https://api.zype.com/ad_tags/[id]</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id | ID of the record to update (Example: 540731274c616e047a000000) | String
ad_tag[name] | Name of the ad tag | String
ad_tag[active] | Optional. Default set to 'true' | Boolean
ad_tag[interval_count] | Optional. How many times a video or videos in a collection will play before a single user gets an ad | Integer
ad_tag[scope] | Optional. Whether `interval_count` applies to single video ('video') or a collection of videos ('library'). Default is 'library'. | String
ad_tag[disabled] | Optional. Pass 'true' to disable a video. Default is 'false' | Boolean
ad_tag[device_category_id] | ID of [DeviceCategory](/api_docs/device_categories) | String
ad_tag[device_id] | ID of [Device](/api_docs/devices) to display AdTag on | String
ad_tag[revenue_partner_id] | ID of revenue partner | String
ad_tag[vmap] | If Ad Tag is a vmap. Default is 'false' | Boolean
ad_tag[tag] | URL of the ad | String

### Delete an Ad Tag
<pre><b>DELETE</b> https://api.zype.com/ad_tags/[id]</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id | ID of the record to delete (Example: 5389352e69702d401b000000) | String

### Ad Tag Object

<pre>
{
  "response": {
    "_id": "5628f9354d656c46285b0000",
    "active": true,
    "created_at": "2015-10-22T10:56:53.896-04:00",
    "deleted_at": null,
    "device_category_id": "3940293kf9d9s0d93049c930"
    "device_id": "5628f99f4d656c46285c0000",
    "disabled": false,
    "interval_count": 3,
    "name": "Ad Tag Name",
    "revenue_partner_id": "5930325c7cebb20023001a0a",
    "scope": "library",
    "site_id": "593031674d740d01cd000000",
    "tag": "https://spotxchange.com"
    "vmap": false
  }
}
