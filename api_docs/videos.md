---
layout: api
title: Zype Developer Portal | Videos
permalink: /api_docs/videos/
---

## Videos
<hr />
### List all Videos
<pre>
<b>GET</b> https://api.zype.com/videos
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
active    | Show active, inactive or all videos Example: true. | String
category  | An optional set of key value category pairs to filter the records returned by category. Example: category[color]=blue. | Hash
category! | Exclude a category from the query. Example: category![color] = blue | Hash
created_at | Filter the records returned by created date. You can use greater than or less than filters by adding a suffix: '.gt', '.gte', '.lt', 'lte'. Example: created_at.gte=2015-01-01 | Date
crunchyroll_id   | Filter videos that have the specified Crunchyroll ID. | String
dpt       | Only shows videos that are available to the end user based on device and country | Boolean
hulu_id   | Filter videos that have the specified Hulu ID. | String
id        | Query for a video by ID | String
id!       | Exclude a video from the query | String
order     | Order videos in ascending or descending order (Example: asc/desc) | String
on_air    | Filter videos that are either on or off air. | Boolean
mature_content    | Filter videos that are flagged as mature content. | Boolean
published_at | Filter the records returned by published date. You can use greater than or less than filters by adding a suffix: '.gt', '.gte', '.lt', 'lte'. Example: published_at.gte=2015-01-01 | Date
q         | A query string for searching for videos | String
sort      | Sort videos on the specified field | String
source_id | Search for videos using an optional user provided source identifier. | String
type      | The type of videos to query. Example: zype, hulu, youtube, crunchyroll | String
vimeo_id   | Filter videos that have the specified Vimeo ID. | String
youtube_id   | Filter videos that have the specified YouTube ID. | String
zobject_id  | Include only videos that belong to the specified Zobject ID. | String
zobject_id! | Exclude videos that belong to the specified Zobject ID. | String

### Create a Video
<hr>
<pre><b>POST</b> https://api.zype.com/videos</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
video[title] | The title of the video | String
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

###Retrieve a Video
<hr>
<pre><b>GET</b> https://api.zype.com/videos/[id]
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | String ID of the video to retrieve. Example: 5389352e69702d401b000000. | String

### Update a Video
<hr>
<pre><b>PUT</b> https://api.zype.com/videos/[id]
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
video[title] | The title of the video | String
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

###Delete a Video
<hr>
<pre><b>DELETE</b> https://api.zype.com/videos/[id]
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | String ID of the video to delete. Example: 5389352e69702d401b000000. | String

### Add Zobject(s) to Video
<hr>
<pre><b>PUT</b> https://api.zype.com/videos/[id]/add_zobjects
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | String ID of the video. Example: 5389352e69702d401b000000. | String
zobject_id | An array containing all of the zobject id's that you want to add to the video. | Array of Strings

### Remove Zobject(s) from Video
<hr />
<pre><b>PUT</b> https://api.zype.com/videos/[id]/remove_zobjects
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | String ID of the video. Example: 5389352e69702d401b000000. | String
zobject_id | An array containing all of the zobject id's that you want to dissociate from the video. | Array of Strings

### Video Object

<pre>
[
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
  </pre>