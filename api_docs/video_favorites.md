---
layout: api
title: Zype Developer Portal | Video Favorites
permalink: /api_docs/video_favorites/
---

## Video Favorites
<hr />
### List Video Favorite Objects
<pre>
<b>GET</b> https://api.zype.com/consumers/[consumer_id]/video_favorites
</pre>

#### Macros

Macro | Function | Type
--------- | -------- | ----
[consumer_id] | ID of the customer object (Example: 5389321e69702d401b120000)  | String

### Create a Video Favorite Object
<pre><b>POST</b> https://api.zype.com/consumers/[consumer_id]/video_favorites
</pre>

#### Macros

Macro | Function | Type
--------- | -------- | ----
[consumer_id] | ID of the customer object (Example: 5389321e69702d401b120000)  | String

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
video_id | ID of the video objecct (Example: 56d7594a0f8asd081208e4)  | String

### Delete a Video Favorite Object
<pre><b>DELETE</b> https://api.zype.com/consumers/[consumer_id]/video_favorites/[video_favorite_id]
</pre>

#### Macros

Macro | Function | Type
--------- | -------- | ----
[consumer_id] | ID of the customer object (Example: 5389321e69702d401b120000)  | String
[video_favorite_id] | ID of the video favorite object (Example: 57cbb0a375jf9asd87011259)  | String

### Video Favorite Object

<pre>
{
  "_id": "57cbb1231c4f960kj2015812",
  "consumer_id": "57cbg120e43f9aa981018199",
  "created_at": "2016-09-04T01:26:59.480-04:00",
  "deleted_at": null,
  "updated_at": "2016-09-04T01:26:59.480-04:00",
  "video_id": "56d7594a8f7aca08aabbc8e3"
}
</pre>