---
layout: api
title: Zype Developer Portal | Revenue Models
permalink: /api_docs/revenue_models/
---

## Revenue Models
<hr />
### List Revenue Models
<pre>
<b>GET</b> https://api.zype.com/revenue_models
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | Query for a revenue model by ID | String
id!       | Exclude a revenue model from the query | String
q         | A query string for searching for revenue models | String
title     | Filter revenue models by title | String
page | The page number of records to return (zero indexed). Example: 0. | Number
per_page | The number of records to return. Example: 10. | Number

###Retrieve a Revenue Model
<pre><b>GET</b> https://api.zype.com/revenue_models/[id]
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id | ID of the revenue model to retrieve. Example: 5389352e69702d401b000000. | String

### Revenue Model Object

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
