---
layout: api
title: Zype Developer Portal | Videos
permalink: /api_docs/videos/
redirect_to: https://docs.zype.com/reference#videos
---

# Videos
---

## Overview
The Videos API is used to query, update, create, and delete videos in the Zype platform.

* [List Videos](#list-videos)
	* [Overview](#overview-1)
	* [Use Case](#use-case-1)
	* [Parameters](#parameters-1)
* [Retrieve a Video](#retrieve-a-video)
	* [Overview](#overview-2)
	* [Use Case](#use-case-2)
	* [Parameters](#parameters-2)
* [Create a Video](#create-a-video)
* [Update a Video](#update-a-video)
* [Delete a Video](#delete-a-video)
* [Add ZObject(s) To Video](#add-zobjects-to-video)
* [Remove ZObject(s) From Video](#remove-zobjects-from-video)
* [Download Source File](#download-source-file)
* [Video Object (Example Response)](#video-object)
* [Download Object (Example Response)](#download-object)

## List Videos
```
GET https://api.zype.com/videos
```

### Overview
Get an **array** of [video objects](#video-object) that meet the specified [parameters](#paremeters-1).

**Note:** To retrieve a single video by ID, the [Retrieve a Video](#retrieve-a-video) endpoint may be used rather than adding the `id` parameter.

### Use Case

Use this endpoint when a list of videos is required.

Examples: retrieve a list of recent videos, a list of videos from a specific category, or a list of videos from a certain date.

```
// List Recent Videos
GET https://api.zype.com/videos?active=true

// List Videos By Category
GET https://api.zype.com/videos?active=true&category[color]=blue

// List Videos From Certain Date
GET https://api.zype.com/videos?active=true&published_at.gte=2017-01-01T00:00:00-00:00
```


### Parameters

Parameter | Function | Type
--------- | -------- | ----
active    | Filter by active, inactive, or all records (Example: `active=true`, `active=false`, `active=all`) | String
category  | Filter records by category value (Example: `category[color]=blue`) | Hash
category! | Exclude records by category value (Example: `category![color]=blue`) | Hash
created_at | Filter records by created date using times in ISO8601 format (Example: `2017-01-01T00:00:00-00:00`) or Unix timestamps (Example: `1483228800`). <br><br>**Note**: Range filters can be applied by adding a suffix: `.gt`, `.gte`, `.lt`, `.lte` (Example: `created_at.gte=2017-01-01T00:00:00-00:00`) | Date
crunchyroll_id   | Filter records by a Crunchyroll ID | String
dpt       | Filter records by DPT conditions (Geo-location and device restrictions) | Boolean
featured  | Filter records that are featured | Boolean
friendly_title | Find records by URL friendly title for SEO purposes | String
hulu_id   | Filter records by a Hulu ID | String
id        | Filter records by ID | String
id!       | Exclude records by ID | String
mature_content    | Filter records that are flagged as mature content | Boolean
order     | Sort records in ascending or descending order (Example: `order=asc`, `order=desc`) | String
on_air    | Filter records that are either on or off air | Boolean
page | The page number of records to return (Example: `page=1`) | Integer
per_page | The number of records to return (Example: `per_page=10`) | Integer
published_at | Filter records by published date using times in ISO8601 format (Example: `2017-01-01T00:00:00-00:00`) or Unix timestamps (Example: `1483228800`) <br><br>**Note**: Range filters can be applied by adding a suffix: `.gt`, `.gte`, `.lt`, `.lte` (Example: `published_at.gte=2017-01-01T00:00:00-00:00`) | Date
q         | Filter records by keyword | String
sort      | Sort records on the specified field | String
source_id | Filter records by an optional source identifier | String
type      | Filter records by type (Examples: `zype`, `hulu`, `youtube`, `crunchyroll`) | String
updated_at | Filter records by last updated date using times in ISO8601 format (Example: `2017-01-01T00:00:00-00:00`) or Unix timestamps (Example: `1483228800`). <br><br>**Note**: Range filters can be applied by adding a suffix: `.gt`, `.gte`, `.lt`, `.lte` (Example: `updated_at.gte=2017-01-01T00:00:00-00:00`) | Date
vimeo_id   | Filter records by a Vimeo ID | String
youtube_id   | Filter records by a YouTube ID | String
zobject_id  | Filter records by Zobject ID | String
zobject_id! | Exclude records by Zobject ID | String

---

## Retrieve a Video
```
GET https://api.zype.com/videos/[id]
```
### Overview
Get a single video by ID.

### Use Case
Use this endpoint when a single video's details are required.

Example: a single video detail page where user interaction can occur. See the [Player API documentation](http://dev.zype.com/api_docs/players/) for how to load a video player.

```
// Retrieve a Video
GET https://api.zype.com/videos/5389352e69702d401b000000

// Load the Video Player (see Player API documentation for more)
GET https://player.zype.com/embed/[video_id].[format]
```

### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | ID of the record to retrieve (Example: `id=5389352e69702d401b000000`) | String

---
## Create a Video
```
POST https://api.zype.com/videos
```

### Parameters

Parameter | Function | Type
--------- | -------- | ----
video[title] | The title of the video | String
video[friendly_title] | The URL friendly title of the video. **Optional** — if left blank, it will be generated automatically. | String
video[description] | The description of the video | String
video[short_description] | The description of the video | String
video[published_at]  | The date and time that the video will appear to have been published | String
video[enable_at] | The date and time that the video will become active | String
video[disable_at] | The date and time the video will become inactive | String
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
video[custom_thumbnail] | Image as a file attachment

---

## Update a Video
```
PUT https://api.zype.com/videos/[id]
```

Note: When updating an array of objects (like `categories_attributes` and `images_attributes`] use `0` or whichever number corresponds to the resource you wish to update. It is index based and so will update the appropriate resource.

### Parameters

Parameter | Function | Type
--------- | -------- | ----
id | ID of the record to update (Example: `id=540731274c616e047a000000`) | String
video[title] | The title of the video | String
video[friendly_title] | The URL friendly title of the video. | String
video[description] | The description of the video | String
video[short_description] | The description of the video | String
video[published_at]  | The date and time that the video will appear to have been published | String
video[enable_at] | The date and time that the video will become active | String
video[disable_at] | The date and time the video will become inactive | String
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
video[categories_attributes][0][id] | ID of the category assigned to the video if you are updating its values | String
video[categories_attributes][0][category_id] | ID of the main [Category](/api_docs/categories) you wish to add to the video | String
video[categories_attributes][0][title] | Title of the category assigned to the video | String
video[categories_attributes][0][value][] | List of values you wish to add to the category | Array
video[images_attributes][0][id] | Pass the ID of the image you wish to update on a given video (optional) | String
video[images_attributes][0][title] | Title of the image | String
video[images_attributes][0][caption] | Caption of the image | String
video[images_attributes][0][attachment] | Image as a file attachment
video[images_attributes][0][layout] | Must be one of 'poster' or 'square'. Default is 'landscape' | String
video[images_attributes][0][_destroy] | Pass in 'true' if you wish to remove an image | String
video[custom_attributes][0][attribute_name] | Pairs of custom attributes with values that you wish to update on a given video | Array
video[custom_thumbnail] | Image as a file attachment
video[delete_custom_thumbnail] | Pass in '1' if you wish to remove the custom thumbnail | String


---

## Delete a Video
```
DELETE https://api.zype.com/videos/[id]
```

### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | ID of the record to delete (Example: 5389352e69702d401b000000) | String

---

## Add Zobject(s) to Video
```
PUT https://api.zype.com/videos/[id]/add_zobjects
```

### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | ID of the record (Example: 5389352e69702d401b000000) | String
zobject_id[] | The zobject IDs to add | Array

---

## Remove Zobject(s) from Video
```
PUT https://api.zype.com/videos/[id]/remove_zobjects
```

### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | ID of the record (Example: 5389352e69702d401b000000) | String
zobject_id[] | The zobject IDs to remove | Array

---

## Download Source File

For Zype Hosted videos you can download the original source file.

```
GET https://api.zype.com/videos/[id]/download
```

### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | ID of the record (Example: 5389352e69702d401b000000) | String

---

## Allow subscription customers to remove ads from videos

To allow consumers with valid subscription plans to remove ads from videos, you can create/update a video using the following parameters:

Parameter | Function | Type
--------- | -------- | ----
subscription_ads_enabled | Flag whether ads should be played when a subscription is present. Setting to true will display ads for videos with ad timings, regardless of subscription status. Setting to false will disable ads for customers with valid subscriptions. Default: **true** | Boolean

## Video Object

```
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
	"enable_at": null,
	"disable_at": null,
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
```

---
## Download Object

```
{
  response: {
    url: "https://zype-upload-prod.s3.amazonaws.com/uploads/57ae371e72289b0d7d00100e/upload.mp4?AWSAccessKeyId=AKIAJ246RBDWDIRI2DVA&Expires=1472064425&Signature=K8rgZ7X8A5ayqW1miUx%2FC4oxytM%3D",
    filesize: 208169473
  }
}
```
