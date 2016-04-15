---
layout: api
title: Zype Developer Portal | Devices
permalink: /api_docs/devices/
---

## Devices
<hr />
### List Devices
<pre>
<b>GET</b> https://api.zype.com/devices
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | Query for a device by ID | String
id!       | Exclude a device from the query | String
q         | A query string for searching for devices | String
title     | Filter devices by title | String
page | The page number of records to return (zero indexed). Example: 0. | Number
per_page | The number of records to return. Example: 10. | Number

###Retrieve a Device
<pre><b>GET</b> https://api.zype.com/devices/[id]
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id | ID of the device to retrieve. Example: 5389352e69702d401b000000. | String

### Device Object

<pre>
{
  "id": "54204805636261f298090000",
  "keywords": [
    "accessed",
    "android",
    "chrome",
    "html5",
    "via"
  ],
  "created_at": "2014-09-22T16:02:13.578Z",
  "description": "Accessed via Chrome",
  "device_category_id": "54204804636261f298050000",
  "image_content_type": "image/png",
  "image_file_name": "mobile.png",
  "image_file_size": 18671,
  "image_fingerprint": "070c15b95b315a6f472a6efb6c3b898c",
  "image_updated_at": "2014-09-22T16:02:13.558+00:00",
  "name": "Chrome Android (HTML5)",
  "player_ids": [
    "54204808636261f298110000",
    "54204808636261f298100000"
  ],
  "updated_at": "2014-09-22T16:02:13.578Z"
}
</pre>
