---
layout: api
title: Zype Developer Portal | Revenue Models
permalink: /api_docs/revenue_models/
redirect_to: https://docs.zype.com/reference#revenue-models
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
created_at | Filter records by created date using times in ISO8601 format (Example: 2017-01-01T00:00:00-00:00) or Unix timestamps (Example: 1483228800) <br />**Note**: Range filters can be applied by adding a suffix: '.gt', '.gte', '.lt', 'lte' (Example: created_at.gte) | Date
id        | Filter records by ID | String
id!       | Exclude records by ID | String
order     | Sort records in ascending or descending order (Example: asc/desc) | String
page      | The page number of records to return (Example: 1) | Integer
per_page  | The number of records to return (Example: 10) | Integer
q         | Filter records by keyword | String
sort      | Sort records on the specified field | String
title     | Filter records by title | String

### Retrieve a Revenue Model
<pre><b>GET</b> https://api.zype.com/revenue_models/[id]
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id | ID of the record to retrieve (Example: 5389352e69702d401b000000) | String

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
