---
layout: api
title: Zype Developer Portal | Video Sources
permalink: /api_docs/video_sources/
redirect_to: https://docs.zype.com/reference#video-sources
---

## Video Sources Collection
<hr>
### List Video Sources
<pre><b>GET</b> https://api.zype.com/video_sources</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
page      | The page number of records to return (Example: 1) | Integer
per_page  | The number of records to return (Example: 10) | Integer
q         | Filter records by keyword | String
type      | The type of video sources to query. Example: self_hosted, zype, hulu, youtube, crunchyroll | String
id        | Query for a video source by id | String
id!       | Exclude records by ID | String

### Retrieve a Video Source
<pre><b>GET</b> https://api.zype.com/video_sources/[id]</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | ID of the record (Example: 5389352e69702d401b000000) | String

## Create a Video Source

<pre><b>POST</b> https://api.zype.com/videos_sources</pre>
Only MRSS and self-hosted video sources may be created via the API at this time.

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
video_source[name] | Name of the video source | String
video_source[url] | MRSS feed URL | String
video_source[category_id] | Category ID assigned to the video source | String
video_source[mrss_category_values][] | Assign values from a Category | Array
video_source[sync_interval] | How often this video source should sync with the MRSS feed (daily / hourly) | String
video_source[auto_add] | Automatically add new video imports to your video library as the feed is synced | Boolean
video_source[auto_activate] | Automatically activate new videos added to your video library | Boolean
video_source[auto_deactivate] | Automatically deactivate video data sources that are absent from this feed that have been previously imported | Boolean
video_source[sync_video_data_source] | Automatically update video source attributes such as thumbnails and video files | Boolean
type | Specify the type of Video Source. Options are 'self_hosted', 'mrss', 'hulu', 'crunchyroll', 'kaltura', 'vimeo', 'vimeo_pro', 'youtube', 'youtube_playlist', 'youtube_video', 'zype', and 'zype_msl' | String
video_source[import_from] | Exclude videos published before this date | Date
video_source[import_to] | Exclude videos published after this date | Date

## Update a Video Source

<pre><b>PUT</b> https://api.zype.com/videos_sources/[id]</pre>
Every video source can update its name and guid (if the source has one). Other attributes may only be updated for self-hosted and MRSS video sources as detailed below.

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
video_source[id] | ID of the record | String
video_source[name] | Updated name of the video source | String
video_source[guid] | Updated guid given for the video source | String

MRSS video sources also have the ability to update the following:

Parameter | Function | Type
--------- | -------- | ----
video_source[url] | MRSS feed URL | String
video_source[category_id] | Category ID assigned to the video source | String
video_source[mrss_category_values][] | Assign values from a Category | Array
video_source[sync_interval] | How often this video source should sync with the MRSS feed (daily / hourly) | String
video_source[auto_add] | Automatically add new video imports to your video library as the feed is synced | Boolean
video_source[auto_activate] | Automatically activate new videos added to your video library | Boolean
video_source[auto_deactivate] | Automatically deactivate video data sources that are absent from this feed that have been previously imported | Boolean
video_source[sync_video_data_source] | Automatically update video source attributes such as thumbnails and video files | Boolean
video_source[import_from] | Exclude videos published before this date | Date
video_source[import_to] | Exclude videos published after this date | Date

Self-hosted video sources also have the ability to update the following:

Parameter | Function | Type
--------- | -------- | ----
video_source[url] | Self-hosted URL | String
video_source[sync_interval] | How often this video source should sync with the source (daily / hourly) | String
video_source[auto_add] | Automatically add new video imports to your video library as the feed is synced | Boolean
video_source[auto_activate] | Automatically activate new videos added to your video library | Boolean
video_source[auto_deactivate] | Automatically deactivate video data sources that are absent from this feed that have been previously imported | Boolean
video_source[import_from] | Exclude videos published before this date | Date
video_source[import_to] | Exclude videos published after this date | Date

### Delete a Video Source
<pre><b>DELETE</b> https://api.zype.com/video_sources/[id]</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | ID of the record to delete (Example: 5389352e69702d401b000000) | String

### Video Source Object

<pre>
{
  "_id": "5468f40d4c616e0a770d0000",
  "created_at": "2014-11-16T13:59:25.420-05:00",
  "deleteable": false,
  "editable": false,
  "name": "Zype",
  "provider_id": "5429b1ca69702d2f7c190000",
  "refreshed_at": null,
  "site_id": "5468f40d4c616e0a770c0000",
  "updated_at": "2014-11-16T13:59:25.420-05:00",
  "video_count": 0
}
</pre>
