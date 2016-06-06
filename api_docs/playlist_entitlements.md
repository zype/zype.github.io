---
layout: api
title: Zype Developer Portal | Playlists
permalink: /api_docs/playlist_entitlements/
---

## Playlist Entitlements

<hr>
### List Playlist Entitlements
<pre><b>GET</b> https://api.zype.com/consumer/playlists</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
active | Filter by active, inactive, or all records (Example: true) | String
category | Filter records by category value (Example: category[color]=blue) | Hash
category! | Exclude records by category value (Example: category![color]=blue) | Hash
id        | Filter records by ID | String
id!       | Exclude records by ID | String
order     | Sort records in ascending or descending order (Example: asc/desc) | String
page | The page number of records to return (Example: 1) | Integer
per_page | The number of records to return (Example: 10) | Integer
q         | Filter records by keyword | String
sort      | Sort records on the specified field | String
title     | Filter records by title | String

### Playlist Object

<pre>
{
  "response": {
    "_id": "5628f9354d656c46285b0000",
    "_keywords": [
      "bundle",
      "featured",
      "videos"
    ],
    "active": true,
    "auto_update_consumer_videos": true,
    "created_at": "2015-10-22T10:56:53.896-04:00",
    "deleted_at": null,
    "description": "",
    "parent_id": "5628f99f4d656c46285c0000",
    "priority": 0,
    "purchase_price": "5.0",
    "purchase_required": true,
    "related_video_ids": [
      "570daad0f283474187000669",
      "570da6a0f28347ccfc002366"
    ],
    "rental_duration": 3,
    "rental_price": "5.0",
    "rental_required": true,
    "site_id": "5468fd6569702d17ee500000",
    "title": "Featured Videos Bundle",
    "updated_at": "2016-04-21T13:43:06.965-04:00",
    "images": [
      {
        "_id": "57191023f2834757dc000028",
        "caption": "My caption",
        "title": "Boxed Set",
        "updated_at": "2016-04-21T13:38:44.834-04:00",
        "url": "http://upload.dev.zype.com/5468fd6569702d17ee500000/video_image/57191023f2834757dc000028/1461260323/original.png?1461260323"
      }
    ],
    "playlist_item_count": 1176,
    "thumbnails": [
      {
        "aspect_ratio": 1.78,
        "height": 240,
        "name": null,
        "url": "http://image.dev.zype.com/5468fd6569702d17ee500000/playlist/5628f9354d656c46285b0000/custom_thumbnail/240.png?1461254280",
        "width": 426
      },
      {
        "aspect_ratio": 1.78,
        "height": 480,
        "name": null,
        "url": "http://image.dev.zype.com/5468fd6569702d17ee500000/playlist/5628f9354d656c46285b0000/custom_thumbnail/480.png?1461254280",
        "width": 854
      },
      {
        "aspect_ratio": 1.78,
        "height": 720,
        "name": null,
        "url": "http://image.dev.zype.com/5468fd6569702d17ee500000/playlist/5628f9354d656c46285b0000/custom_thumbnail/720.png?1461254280",
        "width": 1280
      },
      {
        "aspect_ratio": 1.78,
        "height": 1080,
        "name": null,
        "url": "http://image.dev.zype.com/5468fd6569702d17ee500000/playlist/5628f9354d656c46285b0000/custom_thumbnail/1080.png?1461254280",
        "width": 1920
      }
    ]
  }
}
</pre>
