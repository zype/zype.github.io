---
layout: api
title: Zype Developer Portal | Segments
permalink: /api_docs/segments/
redirect_to: https://docs.zype.com/reference#segments
---

## Segments
<hr />
### List Segments
<pre>
<b>GET</b> https://api.zype.com/videos/[id]/segments
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
video_id  | ID of the parent video (Example: 5389352e69702d401b000000) | String

### Retrieve a Segment
<pre><b>GET</b> https://api.zype.com/videos/[video_id]/segments/[id]
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
video_id        | ID of the parent video (Example: 5389352e69702d401b000000) | String
id        | ID of the record (Example: 5389352e69702d401b000000) | String

### Create a Segment
<pre><b>POST</b> https://api.zype.com/videos/[video_id]/segments
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
video_id        | ID of the parent video (Example: 5389352e69702d401b000000) | String
segment[description] | The description for the video segment | String
segment[start] | The point in the video where the segment begins | Integer
segment[end] | The point in the video where the segment ends | Integer

### Update a Segment
<pre><b>PUT</b> https://api.zype.com/videos/[video_id]/segments/[id]</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
video_id        | ID of the parent video (Example: 5389352e69702d401b000000) | String
segment[description] | The description for the video segment | String
segment[start] | The point in the video where the segment begins | Integer
segment[end] | The point in the video where the segment ends | Integer

### Delete a Segment
<pre><b>DELETE</b> https://api.zype.com/videos/[video_id]/segments/[id]
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
video_id       | ID of the parent video (Example: 5389352e69702d401b000000) | String
id       | ID of the record to be deleted (Example: 5389352e69702d401b000000) | String

### Segment Object

<pre>
{
  "_id": "54c6cbe56368726454050000",
  "description": "theBest",
  "end": 112,
  "start": 90
}
</pre>
