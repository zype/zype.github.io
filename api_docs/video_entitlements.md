---
layout: api
title: Zype Developer Portal | Video Entitlements
permalink: /api_docs/video_entitlements/
---

## Video Entitlements
<hr />
### List Video Entitlements
<pre>
<b>GET</b> https://api.zype.com/consumer/videos
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
