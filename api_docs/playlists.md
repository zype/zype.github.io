---
layout: api
title: Zype Developer Portal | Playlists
permalink: /api_docs/playlists/
---

## Playlists Collection

Lists all Playlists. Playlist information includes descriptive information about the playlist.
<hr>
### List all Playlists
<hr>
<pre><code>GET - https://api.zype.com/playlists?page=page&per_page=per_page&
active=active&keyword=keyword&category=category
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
page | The page number of records to return (zero indexed). Example: 0. | Number
per_page | The number of records to return. Example: 10. | Number
keyword | Filters the records returned by keyword. Example: comedy. | String
active | Filters the records by whether active or not. Example: true. | String
category | An optional set of key value category pairs to filter the records returned by category. Example: category[color]=blue. | Hash

#### Response
200
Content-Type: application/json

<pre><code>{
  "response": [
    {
      "_id": "546407fb69702d76c1740000",
      "_keywords": [
        "featured",
        "horror"
      ],
      "active": true,
      "created_at": "2014-11-12T20:23:07.291-05:00",
      "description": "",
      "priority": 0,
      "related_video_ids": [],
      "site_id": "5463c68e69702d24db490000",
      "title": "Featured Horror ",
      "updated_at": "2014-11-12T20:23:07.291-05:00",
      "playlist_item_count": 6
    }
  ]
}
</code></pre>
<hr>
### Create a Playlist
<hr>
<pre><code>POST - https://api.zype.com/playlists?page=page&per_page=per_page&
active=active&keyword=keyword&category=category
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
playlist | A set of key value pairs that describe the Playlist | Hash

#### Request

Content-Type: application/json

#### Response
201
Content-Type: application/json

<pre><code>{
  "response":
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
}
</code></pre>

## Playlist

Lists descriptive information about Playlist.

<hr>
### Retrieve a Playlist
<hr>
<pre><code>GET - https://api.zype.com/playlists/{id}
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id | String id of the Playlist to retrieve. Example: 5389352e69702d401b000000. | Number

#### Request
Content-Type: application/json

#### Response
200
Content-Type: application/json

<pre><code>{  
  "response":
  {
    "_id": "549082404c616e20e7290000",
    "_keywords": ["playlist","test"],
    "active": true,
    "created_at": "2014-12-16T14:04:32.666-05:00",
    "description": "",
    "priority": 0,
    "related_video_ids": [],
    "site_id": "545932274c616e2359000000",
    "title": "Test Playlist",
    "updated_at": "2014-12-16T14:04:32.666-05:00",
    "playlist_item_count": 4
  }
}
</code></pre>

<hr>

### Retrieve Videos in a Playlist
<hr>
<pre><code>GET - https://api.zype.com/playlists/{id}/videos
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id | String id of the Playlist to retrieve. Example: 5389352e69702d401b000000. | String

#### Request
Content-Type: application/json

#### Response
200
Content-Type: application/json

<pre><code>{
  "response":
  [
    {
      "_id":"5481f66e4c616e06ec670000",
      "active":true,
      "categories":
      [
        {
          "title":"Season",
          "value":["1","2","3","4","5","6","7"]
        },
        {
          "title":"Final test",
          "value":["everything"]
        },
        {
          "title":"Test",
          "value":["no","yes"]
        }
      ],
      "country": "",
      "created_at": "2014-12-05T13:16:14.280-05:00",
      "description": "Music video by Taylor Swift performing #VEVOCertified, Pt. 3: Taylor Talks About Her Fans. (C) 2012 Big Machine Records, LLC.",  
      "duration": 141,
      "episode": null,
      "featured": false,
      "foreign_id": null,
      "keywords": [],
      "mature_content": false,
      "published_at": "2012-10-29T11:45:07.000-04:00",
      "rating": 0.0,
      "related_playlist_ids": [],
      "request_count": 0,
      "season": null,
      "site_id": "545932274c616e2359000000",
      "status": "created",
      "subscription_required": false,
      "title": "#VEVOCertified, Pt. 3: Taylor Talks About Her Fans",
      "updated_at": "2014-12-15T17:53:24.119-05:00",
      "zobject_ids": [],
      "thumbnails":
      [
        {
          "aspect_ratio": null,
          "height": 90,
          "name": null,
          "url": "https://i.ytimg.com/vi/ehLp0cjqkRk/default.jpg",
          "width": 120
        }
      ]
    }
  ]
  "pagination":
  {
    "current": 1,
    "previous":null,
    "next":null,
    "per_page": 10,
    "pages": 1
  }
}
</code></pre>

<hr>


### Update a Playlist
<hr>
<pre><code>PUT - https://api.zype.com/playlists/{id}
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
playlist | A set of key value pairs that describe the playlist. | Hash

#### Request
Content-Type: application/json

#### Response
201
Content-Type: application/json

<pre><code>{
  response:
  {
    "_id": "549082404c616e20e7290000",
    "_keywords": ["playlist","test"],
    "active": true,
    "created_at": "2014-12-16T14:04:32.666-05:00",
    "description": "",
    "priority": 0,
    "related_video_ids": [],
    "site_id": "545932274c616e2359000000",
    "title": "Updated Test Playlist",
    "updated_at": "2014-12-18T14:04:32.666-05:00",
    "playlist_item_count": 4
  }
}
</code></pre>
<hr>
### Remove a Playlist
<hr>
<pre><code>DELETE - https://api.zype.com/playlists/{id}
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id | String id of the Playlist to remove. Example: 5389352e69702d401b000000. | Number

#### Request
Content-Type: application/json

#### Response
204

No Content
