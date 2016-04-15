---
layout: api
title: Zype Developer Portal | Video Sources
permalink: /api_docs/video_sources/
---

## Video Sources Collection
<hr>
### List Video Sources
<pre><b>GET</b> https://api.zype.com/video_sources</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
page      | The page number of records to return (Example: 1) | Integer
per_page  | The number of records to return (Example: 10) | Integer
q         | Filter records by keyword | String
type      | The type of video sources to query. Example: zype, hulu, youtube, crunchyroll | String
id        | Query for a video source by id | String
id!       | Exclude records by ID | String

### Retrieve a Video Source
<pre><b>GET</b> https://api.zype.com/video_sources/[id]</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | ID of the record (Example: 5389352e69702d401b000000) | String

### Delete a Video Source
<pre><b>DELETE</b> https://api.zype.com/video_sources/[id]</pre>

#### Parameters  

Parameter | Function | Type
--------- | -------- | ----
id        | ID of the record to delete (Example: 5389352e69702d401b000000) | String

### Video Source Object

<pre>
{
  "_id": "5468f40d4c616e0a770d0000",
  "created_at": "2014-11-16T13:59:25.420-05:00",
  "deleteable": false,
  "editable": false,
  "name": "Zype",
  "provider_id": "5429b1ca69702d2f7c190000",
  "refreshed_at": null,
  "site_id": "5468f40d4c616e0a770c0000",
  "updated_at": "2014-11-16T13:59:25.420-05:00",
  "video_count": 0
}
</pre>