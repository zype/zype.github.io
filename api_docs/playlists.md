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
playlist[active] | Choose if the playlist should be active | Boolean
playlist[priority] | Order priority relative to other playlists | Integer
playlist[purchase_required] | Enable purchase for the playlist *edge feature* | Boolean
playlist[purchase_price] | Purchase price for the playlist bundle, sent as a string, ie "4.99" *edge feature* | String
playlist[rental_required] | Enable rental for the playlist *edge feature* | Boolean
playlist[rental_price] | Rental price for the playlist bundle, sent as a string, ie "4.99" *edge feature* | String
playlist[rental_duration] | Rental duration for the playlist, in days *edge feature* | Integer
playlist[auto_update_consumer_videos] | Keep consumer video purchases and/or rentals in sync with playlist items. When videos are added to the playlist, also add them to a consumer's video purchase/rental list. *edge feature* | Boolean

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
playlist[active] | Choose if the playlist should be active | Boolean
playlist[priority] | Order priority relative to other playlists | Integer
playlist[purchase_required] | Enable purchase for the playlist *edge feature* | Boolean
playlist[purchase_price] | Purchase price for the playlist bundle, sent as a string, ie "4.99" *edge feature* | String
playlist[rental_required] | Enable rental for the playlist *edge feature* | Boolean
playlist[rental_price] | Rental price for the playlist bundle, sent as a string, ie "4.99" *edge feature* | String
playlist[rental_duration] | Rental duration for the playlist, in days *edge feature* | Integer
playlist[auto_update_consumer_videos] | Keep consumer video purchases and/or rentals in sync with playlist items. When videos are added to the playlist, also add them to a consumer's video purchase/rental list. *edge feature* | Boolean

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

## Managing Playlist Relationships

<p>Playlist Relationships allow you to create a parent / child relationship between two playlists. This is useful for nesting playlist content within OTT apps. For example, you could create a parent playlist called "Comedy" and nest child playlists underneath called "Romantic Comedies" and "Slapstick Comedies" to provide a better user experience for your audience. To manage Playlist Relationships, we use the <strong>parent_id</strong> and <strong>priority</strong> fields of a playlist.</p>

Parameter | Function | Type
--------- | -------- | ----
playlist[parent_id] | The parent playlist id. If this value is <strong>null</strong>, the playlist is a <strong>root</strong> playlist and can be used as the primary playlist within an app where all your other playlists and videos are nested under | String
playlist[priority] | The <strong>priority</strong> of the playlist related with its siblings. Playlists are ordered ascending by priority value | Integer

<p>When creating or updating a Playlist:</p>

<p>
  <ul>
    <li>If the <strong>parent_id</strong> and <strong>priority</strong> are not set, the playlist will be set as a <strong>root</strong> playlist with the highest <strong>priority</strong> value set.</li>
    <li>If the <strong>parent_id</strong> is not set, but the <strong>priority</strong> is, then, the playlist will be set as a <strong>root</strong> playlist, and will be ordered by the <strong>priority</strong> value set. If there is another root playlist with the same priority, then it will be added after this playlist.</li>
    <li>If the <strong>parent_id</strong> and <strong>priority</strong> are set, the playlist will be added as a child of the playlist with id <strong>parent_id</strong>, and will be ordered by the <strong>priority</strong> value set. If there is another sibling playlist with the same priority, then it will be added after the sibling.</li>
  </ul>
</p>

<p>To nest a playlist under a new parent, you need to change its <strong>parent_id</strong> field to the id of the playlist you want to nest it under. If you want it to be a <strong>root</strong> playlist, then you have to set the parent_id field as null or empty</p>

<p>Also, take into account that 0 (zero) is the highest priority.</p>

<hr>
### Create

<p><pre><b>POST</b> https://api.zype.com/playlists</pre></p>

<p>Here is an JSON example to be set as the body to create a Playlist with a relationship:</p>
<pre>
{
  "playlist": {
    "parent_id": "abcd1234",
    "priority": 1
  }
}
</pre>

<hr>
### Update

<p><pre><b>PUT</b> https://api.zype.com/playlists/[id]</pre></p>

<p>Here is an JSON example to be set as the body to create a Playlist with a relationship:</p>
<pre>
{
  "playlist": {
    "parent_id": "abcd1234",
    "priority": 1
  }
}
</pre>

### Relationships

<p><pre><b>GET</b> https://api.zype.com/playlists/relationships</pre></p>

<p>Returns the list of playlists and its relationships</p>

<p>Here is an JSON example to returned:</p>
<pre>
{
    "playlists": [
        {
            "id": "586124bfa54d7535cb001fc2",
            "title": "Playlist A",
            "priority": 0,
            "playlists": [
                {
                    "id": "5942dde0a54d750e3b000042",
                    "title": "Playlist A.1",
                    "priority": 0
                }
            ]
        },
        {
            "id": "58d1718aa54d750bf100002e",
            "title": "Playlist B",
            "priority": 1,
            "playlists": [
                {
                    "id": "5942defea54d750e3b000045",
                    "title": "Playlist B.1",
                    "priority": 0,
                    "playlists": [
                        {
                            "id": "586124bfa54d7535cb001fba",
                            "title": "Playlist B.1.1",
                            "priority": 0
                        }
                    ]
                },
                {
                    "id": "586124bea54d7535cb001fb1",
                    "title": "Playlist B.2",
                    "priority": 1
                }
            ]
        }
    ]
}
</pre>
