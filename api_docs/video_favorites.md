---
layout: api
title: Zype Developer Portal | Video Favorites
permalink: /api_docs/video_favorites/
---

# Video Favorites

---

## Overview
The Video Favorites API is used to query, create, and delete Video Favorites for [authenticated Consumers](http://dev.zype.com/api_docs/oauth).

A Video Favorite is a collection of videos designated by a Consumer as "favorites". Much like bookmarking a web page, Video Favorites allow a Consumer to add and remove bookmarks for videos within an app for easy access at a later time.

A Consumer's Video Favorites are stored in the Zype platform and are accessible from any endpoint the functionality has been implemented on. Currently, Video Favorites functionality can be found in the following Zype SDKs: iOS, Android, Roku, Amazon Fire TV, and Apple TV (local, on-device support only).

Developers may implement Video Favorites on their endpoint of choice if they wish to allow Consumers to bookmark videos for easy access across all app endpoints.

* [List Video Favorite Objects](#list-video-favorite-objects)
* [Create a Video Favorite Object](#create-a-video-favorite-object)
* [Delete a Video Favorite Object](#delete-a-video-favorite-object)
* [Video Favorite Object (Example Response)](#video-favorite-object)

## List Video Favorite Objects

```
GET https://api.zype.com/consumers/[consumer_id]/video_favorites
```
### Overview
Get an **array** of Video Favorite Objects for the specified Consumer.

### Use Case
Use this endpoint to retrieve and/or display a Consumer's Video Favorites.

**Example 1**  
List a Consumer's Video Favorites in one area of an app for convenient access.

```
/**
 * List Consumer's Video Favorites
 * 
 * @NOTE Pseudocode 
 */

// Get Video Favorites
var video_favorites = GET https://api.zype.com/consumers/[consumer_id]/video_favorites;

// Get Video Details for each Video Favorite
for (var i = 0; i < video_favorites.length; i++) {
  // Get the Video Favorite video_id
  var video_id = video_favorites[i].video_id;
	
  // Get Video by ID
  var video = GET https://api.zype.com/videos/[video_id]
  
  // Do something with retrieved video
}
```
**Example 2**  
Visually designate a Consumer's Video Favorites inline with a [List Videos](http://dev.zype.com/api_docs/videos/#list-videos) query.

```
/**
 * Display Video Favorites Inline
 * 
 * @NOTE Pseudocode 
 */

// Get Video Favorites
GET https://api.zype.com/consumers/[consumer_id]/video_favorites

// Get Videos
GET https://api.zype.com/videos

// Map Video Favorites IDs with Video IDs
```


### Macros

Macro | Function | Type
--------- | -------- | ----
[consumer_id] | ID of the customer object (Example: `5389321e69702d401b120000`)  | String

---

## Create a Video Favorite Object
```
POST https://api.zype.com/consumers/[consumer_id]/video_favorites
```

### Macros

Macro | Function | Type
--------- | -------- | ----
[consumer_id] | ID of the customer object (Example: `5389321e69702d401b120000`)  | String

### Parameters

Parameter | Function | Type
--------- | -------- | ----
video_id | ID of the video object (Example: `56d7594a0f8asd081208e4`)  | String

---
## Delete a Video Favorite Object
```
DELETE https://api.zype.com/consumers/[consumer_id]/video_favorites/[video_favorite_id]

/**
 * @NOTE Some client-side languages / libraries (JavaScript, jQuery, etc.) 
 *       must use POST with `_method=delete` parameter and value specifed.
 */
 
POST https://api.zype.com/consumers/[consumer_id]/video_favorites/[video_favorite_id]?_method=delete
```

### Macros

Macro | Function | Type
--------- | -------- | ----
[consumer_id] | ID of the customer object (Example: `5389321e69702d401b120000`)  | String
[video_favorite_id] | ID of the video favorite object (Example: `57cbb0a375jf9asd87011259`)  | String

### Parameters (Optional: Client-Side Languages)

Parameter | Function | Type
--------- | -------- | ----
_method | Passes delete command via parameter (Example: `_method=delete`)| String

---
## Video Favorite Object

```
{
  "_id": "57cbb1231c4f960kj2015812",
  "consumer_id": "57cbg120e43f9aa981018199",
  "created_at": "2016-09-04T01:26:59.480-04:00",
  "deleted_at": null,
  "updated_at": "2016-09-04T01:26:59.480-04:00",
  "video_id": "56d7594a8f7aca08aabbc8e3"
}
```