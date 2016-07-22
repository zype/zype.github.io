---
layout: api
title: Zype Developer Portal | Device Linking
permalink: /api_docs/device_linking/
---

## Device Linking
<hr>
### Retrieve Device Pin
<pre><b>GET</b> https://api.zype.com/pin/status</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
linked_device_id      | Unique ID of the user's device | String


### Create Device Pin
<pre><b>POST</b> https://api.zype.com/pin/acquire</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
linked_device_id      | Unique ID of the user's device | String

### Link Device Pin

<pre><b>PUT</b> https://api.zype.com/pin/link</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
consumer_id      | ID of the consumer to link | String
pin | The value for the acquired device pin (Example: zabc123) | String


### Device Pin Object

<pre>
{
  "_id": "57113fc6f283474159000004",
  "consumer_id": null,
  "created_at": "2016-04-15T15:23:50.198-04:00",
  "deleted_at": null,
  "device_id": null,
  "linked_device_id": "sdkjafklsjdklfjasdf",
  "pin": "zizm529",
  "pin_expiration": "2016-04-15T15:53:50.195-04:00",
  "site_id": "5468fd6569702d17ee500000",
  "updated_at": "2016-04-15T15:23:50.198-04:00",
  "linked": false,
  "subscription_count": null
}
</pre>