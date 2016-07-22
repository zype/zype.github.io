---
layout: api
title: Zype Developer Portal | Videos
permalink: /api_docs/videos/
---

## Videos
<hr />
### List Videos
<pre>
<b>GET</b> https://api.zype.com/videos
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
active    | Filter by active, inactive, or all records (Example: true) | String
category  | Filter records by category value (Example: category[color]=blue) | Hash
category! | Exclude records by category value (Example: category![color]=blue) | Hash
created_at | Filter records by created date. Greater or less than filters can be used by adding a suffix (Example: created_at.gte) | Date
crunchyroll_id   | Filter records by a Crunchyroll ID | String
dpt       | Filter records by DPT conditions (Geo-location and device restrictions) | Boolean
friendly_title | Find records by URL friendly title for SEO purposes | String
hulu_id   | Filter records by a Hulu ID | String
id        | Filter records by ID | String
id!       | Exclude records by ID | String
mature_content    | Filter records that are flagged as mature content | Boolean
order     | Sort records in ascending or descending order (Example: asc/desc) | String
on_air    | Filter records that are either on or off air | Boolean
page | The page number of records to return (Example: 1) | Integer
per_page | The number of records to return (Example: 10) | Integer
published_at | Filter records by published date. Greater or less than filters can be used by adding a suffix (Example: published_at.gte) | Date
q         | Filter records by keyword | String
sort      | Sort records on the specified field | String
source_id | Filter records by an optional source identifier | String
type      | Filter records by type (Example: zype, hulu, youtube, crunchyroll) | String
vimeo_id   | Filter records by a Vimeo ID | String
youtube_id   | Filter records by a YouTube ID | String
zobject_id  | Filter records by Zobject ID | String
zobject_id! | Exclude records by Zobject ID | String

### Create a Video
<pre><b>POST</b> https://api.zype.com/videos</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
video[title] | The title of the video | String
video[friendly_title] | The URL friendly title of the video. Optional — if left blank, it will be generated automatically. | String
video[description] | The description of the video | String
video[short_description] | The description of the video | String
video[published_at]  | The date and time that the video will appear to have been published | String
video[episode] | The video's episode number | Integer
video[season] | The video's season number | Integer
video[country] | The country the video was created in | String
video[active] | Whether or not the video is active | Boolean
video[featured] | Whether or not the video is featured | Boolean
video[keywords] | Keywords for the video | Array
video[subscription_required] | Whether or not the video requires a subscription to view | Boolean
video[subscription_required] | Whether or not the video requires a pass to view | Boolean
video[mature_content] | Whether or not the video requires the viewer to be 18+ to view | Boolean
video[discovery_url] | The URL where the video will be hosted, this field can be used in RSS distribution | String
video[source_id] | An optional user specified identifier for a video | String
video[custom_thumbnail_url] | A URL where a custom thumbnail for the video can be retrieved (JPEG, PNG or GIF) | String

### Retrieve a Video
<pre><b>GET</b> https://api.zype.com/videos/[id]
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | ID of the record to retrieve (Example: 5389352e69702d401b000000) | String

### Update a Video
<pre><b>PUT</b> https://api.zype.com/videos/[id]
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id | ID of the record to update (Example: 540731274c616e047a000000) | String
video[title] | The title of the video | String
video[friendly_title] | The URL friendly title of the video. | String
video[description] | The description of the video | String
video[short_description] | The description of the video | String
video[published_at]  | The date and time that the video will appear to have been published | String
video[episode] | The video's episode number | Integer
video[season] | The video's season number | Integer
video[country] | The country the video was created in | String
video[active] | Whether or not the video is active | Boolean
video[featured] | Whether or not the video is featured | Boolean
video[keywords] | Keywords for the video | Array
video[subscription_required] | Whether or not the video requires a subscription to view | Boolean
video[subscription_required] | Whether or not the video requires a pass to view | Boolean
video[mature_content] | Whether or not the video requires the viewer to be 18+ to view | Boolean
video[discovery_url] | The URL where the video will be hosted, this field can be used in RSS distribution | String
video[source_id] | An optional user specified identifier for a video | String
video[custom_thumbnail_url] | A URL where a custom thumbnail for the video can be retrieved (JPEG, PNG or GIF) | String

### Delete a Video
<pre><b>DELETE</b> https://api.zype.com/videos/[id]
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | ID of the record to delete (Example: 5389352e69702d401b000000) | String

### Add Zobject(s) to Video
<pre><b>PUT</b> https://api.zype.com/videos/[id]/add_zobjects</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | ID of the record (Example: 5389352e69702d401b000000) | String
zobject_id[] | The zobject IDs to add | Array

### Remove Zobject(s) from Video
<pre><b>PUT</b> https://api.zype.com/videos/[id]/remove_zobjects</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | ID of the record (Example: 5389352e69702d401b000000) | String
zobject_id[] | The zobject IDs to remove | Array

### Video Object

<pre>
{
  "_id": "547b4dca69702d070dca0000",
  "active": true,
  "categories": [
    {
      "title": "Additional Videos from YouTube",
      "value": []
    },
    {
      "title": "Genre",
      "value": [
        "Adventure"
      ]
    },
    {
      "title": "series",
      "value": []
    }
  ],
  "country": "",
  "created_at": "2014-11-30T12:03:06.783-05:00",
  "description": "A continuation of the saga created by George Lucas set thirty years after Star Wars: Episode VI - Return of the Jedi (1983).",
  "discovery_url": "http://www.yoursite.com/video"
  "duration": 91,
  "episode": null,
  "featured": false,
  "foreign_id": null,
  "friendly_title": "star-wars-episode-vii-the-force-awakens-official-teaser-trailer",
  "keywords": [],
  "segments": [],
  "mature_content": false,
  "published_at": "2014-11-30T12:01:32.000-05:00",
  "rating": 0,
  "related_playlist_ids": [
    "5464084f69702d76c1770000"
  ],
  "request_count": 14,
  "season": null,
  "site_id": "5463c68e69702d24db490000",
  "status": "created",
  "subscription_required": false,
  "title": "Star Wars: Episode VII - The Force Awakens Official Teaser Trailer",
  "updated_at": "2014-12-17T23:00:03.649-05:00",
  "video_zobjects": [
    {
      "_id": "547b4e6f69702d070dd30000",
      "description": "",
      "title": "Harrison Ford",
      "zobject_type_title": "actor"
    },
    {
      "_id": "547b4e9369702d070edc0000",
      "description": "",
      "title": "J.J. Abrams",
      "zobject_type_title": "director"
    },
    {
      "_id": "54808d6a69702d18b51d0000",
      "description": "",
      "title": "John Boyega",
      "zobject_type_title": "actor"
    }
  ],
  "zobject_ids": [
    "547b4e6f69702d070dd30000",
    "547b4e9369702d070edc0000",
    "54808d6a69702d18b51d0000"
  ],
  "thumbnails": [
    {
      "aspect_ratio": null,
      "height": 90,
      "name": null,
      "url": "https://i.ytimg.com/vi/PlFckE98xN4/default.jpg",
      "width": 120
    },
    {
      "aspect_ratio": null,
      "height": 180,
      "name": null,
      "url": "https://i.ytimg.com/vi/PlFckE98xN4/mqdefault.jpg",
      "width": 320
    },
    {
      "aspect_ratio": null,
      "height": 360,
      "name": null,
      "url": "https://i.ytimg.com/vi/PlFckE98xN4/hqdefault.jpg",
      "width": 480
    }
  ]
}
</pre>
