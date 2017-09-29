---
layout: api
title: Zype Developer Portal | Videos
permalink: /api_docs/subtitles/
---

# Subtitles
---

## Overview
The Subtitles API is used to query, update, create, and delete subtitles in the Zype platform.

* [List Subtitles](#list-subtitles)
  * [Overview](#overview-1)
  * [Parameters](#parameters)
* [Retrieve a Subtitle](#retrieve-a-subtitle)
  * [Overview](#overview-2)
  * [Parameters](#parameters-1)
* [Create a Subtitle](#create-a-subtitle)
  * [Parameters](#parameters-2)
* [Update a Subtitle](#update-a-subtitle)
  * [Parameters](#parameters-3)
* [Delete a Subtitle](#delete-a-subtitle)
  * [Parameters](#parameters-4)
* [Subtitle Object (Example Response)](#subtitle-object)

## List Subtitles
```
GET https://api.zype.com/videos/[video_id]/subtitles
```

### Overview
Get an **array** of [subtitle objects](#subtitle-object) from a specific video.

**Note:** To retrieve a single subtitle by ID, the [Retrieve a Subtitle](#retrieve-a-subtitle) endpoint may be used rather by adding the `id` parameter.

### Parameters

Parameter | Function | Type
--------- | -------- | ----
video_id  | ID of the Video object that contains the subtitle (Example: `video_id=5389352e69702d401b000000`) | String 

## Retrieve a Subtitle
```
GET https://api.zype.com/videos/[video_id]/subtitles/[id]
```

### Overview
Get a single subtitle by ID.

### Parameters

Parameter | Function | Type
--------- | -------- | ----
video_id  | ID of the Video object that contains the subtitle (Example: `video_id=5389352e69702d401b000000`) | String 
id        | ID of the Subtitle record to retrieve (Example: `id=59c93e3a02eac40026000005`) | String

## Create a Subtitle
```
POST https://api.zype.com/videos/[video_id]/subtitles
```

### Parameters

Parameter | Function | Type | Required
--------- | -------- | ---- | --------
video_id | ID of the Video object that contains the subtitle | String | Yes
subtitle[active] | Whether or not the subtitle is active | Boolean | No
subtitle[language] | Language of the subtitle | String | Yes
subtitle[file] | Base64 encoded subtitle | String | Yes
subtitle[extension_type] | Original file extension of the subtitle (allowed formats: srt,vtt) | String | Yes

## Update a Subtitle
```
PUT https://api.zype.com/videos/[video_id]/subtitles/[id]
```

### Parameters

Parameter | Function | Type
--------- | -------- | ----
id | ID of the record to update (Example: `id=540731274c616e047a000000`) | String
video_id | ID of the Video object that contains the subtitle | String
subtitle[active] | Whether or not the subtitle is active | Boolean
subtitle[language] | Language of the subtitle | String

## Delete a Subtitle
```
DELETE https://api.zype.com/videos/[video_id]/subtitles/[id]
```

### Parameters

Parameter | Function | Type
--------- | -------- | ----
id | ID of the record to update (Example: `id=540731274c616e047a000000`) | String
video_id | ID of the Video object that contains the subtitle | String

## Subtitle Object

```
{
    "_id": "59ca6a6802eac4002600000e",
    "active": true,
    "extension_type": "vtt",
    "file_content_type": "text/plain",
    "file_file_name": "subtitle_2017-09-26T14_55_36_00_00.vtt",
    "file_file_size": 787,
    "file_fingerprint": "1721f4c80fbb135b4b1173f67e4d466b",
    "file_updated_at": "2017-09-26T10:55:36.796-04:00",
    "language": "pt"
}
```
