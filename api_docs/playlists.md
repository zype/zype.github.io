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

## Category Playlists

<hr>
### Create

<p>Creating a Category Playlist, is the same as creating a Playlist but setting its <strong>playlist_type</strong> with a <i>'category'</i> value. You should call the POST action:</p>

<pre><b>POST</b> https://api.zype.com/playlists</pre>

<p>with the following parameters:</p>

Parameter | Function | Type
--------- | -------- | ----
playlist[playlist_type] | The playlist type to create. Accepted values: **manual**, **category** | String
playlist[match_type] | Videos that should match with the categories selected. Accepted values: **any**, **all**. If match_type is *any*, videos to be added to the playlist should match *ANY* of the categories selected. If match_type is *all*, videos to be added to the playlist should match *ALL* of the categories selected. | String
playlist[categories] | Categories that will be used to selected the proper videos to add into the playlist | Array

<p>The <strong>playlist[categories]</strong> should contain an array of hashes. Every hash will represent a category to be added with the following parameters:</p>

Parameter | Function | Type
--------- | -------- | ----
categories[category_id] | ID of the category that will be referenced | Integer
categories[title] | Title of the category to be added | String
playlist[values] | Values selected of the category referenced | Array

<p>Here is an JSON example to be set as the body to create a Category Playlist:</p>
<pre>
{
  "playlist": {
    "title": "Category Playlist",
    "playlist_type": "category",
    "match_type": "any",
    "categories": [
      {
        "category_id": "1234",
        "title": "Category Title",
        "value": [
          "Category Value"
        ]
      }
    ]
  }
}
</pre>

<p>Take into account that the <strong>category_id</strong> should be included into the site's categories. To get the list of categories, please go to the <a href="/api_docs/categories" target="none">categories documentation</a>. If a category with the selected <i>category_id</i> doesn't exists, you will get a <strong>422</strong> response with the following message:</p>

<pre>
{
  "message": "Could not save playlist: Categories is invalid"
}
</pre>

<hr>
### Update

<p>Updating a Category Playlist, is the same as updating a Playlist but changing its <strong>categories</strong>. You should call the PUT action:</p>

<pre><b>PUT</b> https://api.zype.com/playlists/[id]</pre>

<p>Take into account that <strong>updating</strong> a playlist categories will overwrite the current categories. So, if you want to keep your current categories and values, adding new ones, you should add them to the json body parameters. If you want to delete categories or values, you have to set the categories array only with the categories that you want for your playlist, obviating the ones that you don't need anymore</p>
