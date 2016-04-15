---
layout: api
title: Zype Developer Portal | Video Imports
permalink: /api_docs/video_imports/
---

## Video Imports
<hr>
### List Video Imports
<pre><b>GET</b> https://api.zype.com/video_imports</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
page      | The page number of records to return (Example: 1) | Integer
per_page  | The number of records to return (Example: 10) | Integer
q         | Filter records by keyword | String
status    | Filters the records returned by status. Example: created | String
active    | Filter by active, inactive, or all records (Example: true) | String
type      | Filter records by type (Example: hulu, youtube, crunchyroll) | String
id        | Query for a video import by id | String
id!       | Exclude records by ID | String
video_source_id | Query by video source | String

### Retrieve a Video Import
<pre><b>GET</b> https://api.zype.com/video_imports/[id]</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | ID of the record (Example: 5389352e69702d401b000000) | String

### Create Video from a Video Import
<pre><b>PUT</b> https://api.zype.com/video_imports/[id]/add_video
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | ID of the record (Example: 5389352e69702d401b000000) | String
video_id  | ID of a video to add the record to (Example: 5389352e69702d401b000000) | String

### Video Import Object
<pre>
{
  "_id": "5499c02d4c616e0545000000",
  "active": true,
  "created_at": "2014-12-23T14:19:09.369-05:00",
  "description": 
    "She came to the Tiny Desk a little unsure, and left singing \"West Memphis\" with intensity and passion ...",
  "duration": 1195,
  "episode": nil,
  "etag": "\"F9iA7pnxqNgrkOutjQAa9F2k8HY/RVSzO8IXeqRD4Xh1SisxwseyKvk\"",
  "keywords": [],
  "published_at": "2014-12-22T18:03:09.000-05:00",
  "season": nil,
  "site_id": "12345abcd",
  "status": "ready",
  "thumbnails": 
  [
    {"aspect_ratio": nil,
    "height": 90,
    "name": nil,
    "url": "https://i.ytimg.com/vi/mTu4cXW9H_Q/default.jpg",
    "width": 120}
  ],
  "title": "Lucinda Williams: NPR Music Tiny Desk Concert",
  "updated_at": "2014-12-23T14:19:09.369-05:00",
  "upload_id": nil,
  "video_id": nil,
  "video_source_id": "5499c0274c616e04b8110000",
  "youtube_id": "mTu4cXW9H_Q"
}
</pre>