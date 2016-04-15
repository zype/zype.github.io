---
layout: api
title: Zype Developer Portal | Apps
permalink: /api_docs/apps/
---

## Apps
<hr>
### Retrieve App
<pre><b>GET</b> https://api.zype.com/app</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
app_key   | The app key | String

### App Object
App profiles vary by the type of application. 
<pre>
{
  "_id": "12345",
  "active": true,
  "app_type_id": "12345",
  "site_id": "abc1234",
  "store_id": "abc1234",
  "title": "Roku Title",
  "version": 1.0,
  "store_icon_url": null
}
</pre>
