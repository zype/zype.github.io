---
layout: api
title: Zype Developer Portal | Device Categories
permalink: /api_docs/device_categories/
---

## Device Categories
<hr />
### List Device Categories
<pre>
<b>GET</b> https://api.zype.com/device_categories
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | Query for a device category by ID | String
id!       | Exclude a device category from the query | String
q         | A query string for searching for device categories | String
title     | Filter device_categories by title | String
page | The page number of records to return (zero indexed). Example: 0. | Number
per_page | The number of records to return. Example: 10. | Number

###Retrieve a Device Category
<hr>
<pre><b>GET</b> https://api.zype.com/device_categories/[id]
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id | String ID of the device category to retrieve. Example: 5389352e69702d401b000000. | String

### Device Category Object

<pre>
{
  "_id": "5429b1c369702d2f7c040000",
  "_keywords": [
    "desktop"
  ],
  "created_at": "2014-09-29T15:23:47.302-04:00",
  "image_content_type": "image/png",
  "image_file_name": "desktop.png",
  "image_file_size": 19347,
  "image_fingerprint": "a661d27f5003bcf1523f75e3686f6b24",
  "image_updated_at": "2014-09-29T15:23:47.099-04:00",
  "name": "Desktop",
  "updated_at": "2014-09-29T15:23:47.302-04:00"
}
</pre>
