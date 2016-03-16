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
parent_id | Filters the records by their playlist parent id. Example: parent_id=556f397c69702d04c3cc4c01 | String
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
      "parent_id": "556f397c69702d04c3cc4c01",
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
title | The title of the playlist | String
site_id | The id of the site the playlist belongs to | String
video_ids | A list of items within the playlist by video id | Array

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
    "_keywords": ["playlist","sample"],
    "active": true,
    "created_at": "2014-12-16T14:04:32.666-05:00",
    "description": "",
    "priority": 0,
    "related_video_ids": [],
    "site_id": "545932274c616e2359000000",
    "title": "sample Playlist",
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
  "response": [
    {
      "_id":"5481f66e4c616e06ec670000",
      "active":true,
      "categories":
      [
        {
          "title":"Season",
          "value":["1"]
        },
        {
          "title":"Final sample",
          "value":["everything"]
        },
        {
          "title":"sample",
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
playlist | A set of key value pairs that describe the Playlist | Hash
title | The title of the playlist | String
site_id | The id of the site the playlist belongs to | String
video_ids | A list of items within the playlist by video id | Array
video_id | The id of a video to be repositioned within the playlist | String
position | The position that the video will now occupy within the playlist | Integer

#### Request
Content-Type: application/json

#### Response
201
Content-Type: application/json

<pre><code>{
  response:
  {
    "_id": "549082404c616e20e7290000",
    "_keywords": ["playlist","sample"],
    "active": true,
    "created_at": "2014-12-16T14:04:32.666-05:00",
    "description": "",
    "priority": 0,
    "related_video_ids": [],
    "site_id": "545932274c616e2359000000",
    "title": "Updated sample Playlist",
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

<hr>
### Add Video to a Playlist
<hr>
<pre><code>PUT - https://api.zype.com/playlists/{id}/add_videos/&video_id=video_id
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
video_id  | ID of the video to add the playlist | String

#### Request

Content-Type: application/json

#### Response
201
Content-Type: application/json

<pre><code>{
  "response"=> [
    {
      "_id"=>"5499c6bc4c616e04b8120000",
      "active"=>true,
      "country"=>"",
      "created_at"=>"2014-12-23T14:47:09.079-05:00",
      "description"=>
      "A staple of \"Bands To Watch\" lists far and wide, Alabama Shakes ...",
      "duration"=>665,
      "episode"=>nil,
      "featured"=>false,
      "foreign_id"=>nil,
      "keywords"=>[],
      "mature_content"=>false,
      "published_at"=>"2012-03-27T12:59:21.000-04:00",
      "rating"=>0.0,
      "related_playlist_ids"=>[],
      "request_count"=>0,
      "season"=>nil,
      "site_id"=>"5468f40d4c616e0a770c0000",
      "status"=>"created",
      "subscription_required"=>false,
      "title"=>"Alabama Shakes, Live In Concert: NPR Music's SXSW 2012 Showcase",
      "updated_at"=>"2014-12-24T17:57:15.731-05:00",
      "zobject_ids"=>[],
      "thumbnails"=>
        [
        {"aspect_ratio"=>nil, "height"=>90, "name"=>nil, "url"=>"https://i.ytimg.com/vi/eNa5wYXonbQ/default.jpg", "width"=>120},
        {"aspect_ratio"=>nil, "height"=>180, "name"=>nil, "url"=>"https://i.ytimg.com/vi/eNa5wYXonbQ/mqdefault.jpg", "width"=>320},
        {"aspect_ratio"=>nil, "height"=>360, "name"=>nil, "url"=>"https://i.ytimg.com/vi/eNa5wYXonbQ/hqdefault.jpg", "width"=>480},
        {"aspect_ratio"=>nil, "height"=>480, "name"=>nil, "url"=>"https://i.ytimg.com/vi/eNa5wYXonbQ/sddefault.jpg", "width"=>640},
        {"aspect_ratio"=>nil, "height"=>720, "name"=>nil, "url"=>"https://i.ytimg.com/vi/eNa5wYXonbQ/maxresdefault.jpg", "width"=>1280}
        ]
      }
    ],
    "pagination"=>{"current"=>1, "previous"=>nil, "next"=>nil, "per_page"=>25, "pages"=>1}
    }
  }
}
</code></pre>

<hr>
### Remove Video from a Playlist
<hr>
<pre><code>PUT - https://api.zype.com/playlists/{id}/add_videos/&video_id=video_id
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
video_id  | ID of the video to add the playlist | String

#### Request

Content-Type: application/json

#### Response
201
Content-Type: application/json

<pre><code>{
  "response"=>[],
  "pagination"=>
  {
    "current"=>1, "previous"=>nil, "next"=>2, "per_page"=>25, "pages"=>0
  }
}
</code></pre>
