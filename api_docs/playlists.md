---
layout: api
title: Zype Developer Portal | Playlists
permalink: /api_docs/playlists/
---

## Playlists Collection

<hr>
### List Playlists
<hr>
<pre><b>GET</b> https://api.zype.com/playlists</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
active | Filters the records by whether active or not. Example: true. | String
category | An optional set of key value category pairs to filter the records returned by category. Example: category[color]=blue. | Hash
category! | Exclude a category from the query. Example: category![color] = blue | Hash
id        | Query for a category by ID | String
id!       | Exclude a category from the query | String
order     | Order playlists in ascending or descending order (Example: asc/desc) | String
page | The page number of records to return (zero indexed). Example: 0. | Number
per_page | The number of records to return. Example: 10. | Number
q         | A query string for searching for playlists. | String
sort      | Sort playlists on the specified field | String

### Create a Playlist
<hr>
<pre><b>POST</b> https://api.zype.com/playlists</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
playlist[title] | The title of the playlist | String
playlist[description] | The description of the playlist | String

### Retrieve a Playlist
<hr>
<pre><b>GET</b> https://api.zype.com/playlists/[id]
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id | ID of the Playlist to retrieve. Example: 5389352e69702d401b000000. | Number

### List Playlist Videos
<hr>
<pre><b>GET</b> https://api.zype.com/playlists/[id]/videos</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id | ID of the playlist videos to retrieve. Example: 5389352e69702d401b000000. | String

### Update a Playlist
<hr>
<pre><b>PUT</b> https://api.zype.com/playlists/[id]</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id | ID of the playlist to update. Example: 540731274c616e047a000000. | String
playlist[title] | The title of the playlist | String
playlist[description] | The description of the playlist | String

### Delete a Playlist
<hr>
<pre><b>DELETE</b> https://api.zype.com/playlists/[id]</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id | ID of the Playlist to remove. Example: 5389352e69702d401b000000. | Number

### Add Video(s) to a Playlist
<hr>
<pre><b>PUT</b> https://api.zype.com/playlists/[id]/add_videos</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | ID of the playlist. Example: 5389352e69702d401b000000. | String
video_id  | A comma separated list of video IDs to add to the playlist | String

### Remove Video(s) from a Playlist
<hr>
<pre><b>PUT</b> https://api.zype.com/playlists/[id]/remove_videos
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | ID of the playlist. Example: 5389352e69702d401b000000. | String
video_id  | A comma separated list of video IDs to remove from the playlist | String

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
