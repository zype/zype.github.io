---
layout: api
title: Zype Developer Portal | Playlists
permalink: /api_docs/playlists/
---

## Playlists

<hr>
### List Playlists
<pre><b>GET</b> https://api.zype.com/playlists</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
active | Filter by active, inactive, or all records (Example: true) | String
category | Filter records by category value (Example: category[color]=blue) | Hash
category! | Exclude records by category value (Example: category![color]=blue) | Hash
friendly_title | Filter records by their SEO friendly title | String
id        | Filter records by ID | String
id!       | Exclude records by ID | String
order     | Sort records in ascending or descending order (Example: asc/desc) | String
page | The page number of records to return (Example: 1) | Integer
per_page | The number of records to return (Example: 10) | Integer
q         | Filter records by keyword | String
sort      | Sort records on the specified field | String
title     | Filter records by title | String

### Create a Playlist
<pre><b>POST</b> https://api.zype.com/playlists</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
playlist[title] | The title of the playlist | String
playlist[description] | The description of the playlist | String

### Retrieve a Playlist
<pre><b>GET</b> https://api.zype.com/playlists/[id]
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id | ID of the record to retrieve (Example: 5389352e69702d401b000000) | String

### List Playlist Videos
<pre><b>GET</b> https://api.zype.com/playlists/[id]/videos</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id | ID of the record to retrieve (Example: 5389352e69702d401b000000) | String

### Update a Playlist
<pre><b>PUT</b> https://api.zype.com/playlists/[id]</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id | ID of the record to update (Example: 540731274c616e047a000000) | String
playlist[title] | The title of the playlist | String
playlist[description] | The description of the playlist | String

### Delete a Playlist
<pre><b>DELETE</b> https://api.zype.com/playlists/[id]</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id | ID of the record to delete (Example: 5389352e69702d401b000000) | String

### Add Video(s) to a Playlist
<pre><b>PUT</b> https://api.zype.com/playlists/[id]/add_videos</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | ID of the record (Example: 5389352e69702d401b000000) | String
video_id[]  | A comma separated list of video IDs to add to the playlist | Array

### Remove Video(s) from a Playlist
<pre><b>PUT</b> https://api.zype.com/playlists/[id]/remove_videos
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | ID of the record (Example: 5389352e69702d401b000000) | String
video_id[]  | A comma separated list of video IDs to remove from the playlist | String

### Playlist Object

<pre>
{  
  "_id": "54908b5c4c616e20e73a0000",
  "_keywords": ["active","best","playlist"],
  "active": true,
  "created_at": "2014-12-16T14:43:24.272-05:00",
  "description": null,
  "priority": null,
  "related_video_ids": [],
  "site_id": "545932274c616e2359000000",
  "title": "The best active playlist!!",
  "updated_at": "2014-12-16T14:43:24.272-05:00",
  "playlist_item_count": 0
}
</pre>
