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
created_at | Filter the records returned by created date. Greater or less than filters can be used by adding a suffix (Example: created_at.gte) | Date
id        | Filter records by ID | String
id!       | Exclude records by ID | String
order     | Sort records in ascending or descending order (Example: asc/desc) | String
page      | The page number of records to return (Example: 1) | Integer
per_page  | The number of records to return (Example: 10) | Integer
q         | Filter records by keyword | String
sort      | Sort records on the specified field | String
title     | Filter records by title | String

### Retrieve a Device Category
<pre><b>GET</b> https://api.zype.com/device_categories/[id]
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id | ID of the record to retrieve (Example: 5389352e69702d401b000000) | String

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
