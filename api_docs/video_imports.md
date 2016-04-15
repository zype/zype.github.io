---
layout: api
title: Zype Developer Portal | Video Imports
permalink: /api_docs/video_imports/
---

## Video Imports Collection
Lists all Video Imports. Video Imports are created via video sources.
<hr>
### List all Video Imports
<hr>
<pre><code><b>GET</b> https://api.zype.com/video_imports?page=page&per_page=per_page&
q=q&keyword=keyword&status=status&active=active&
id=id&id!=id&video_source_id=video_source_id&q=q&keyword=keyword
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
page      | The page number of records to return (Example: 1) | Integer
per_page  | The number of records to return (Example: 10) | Integer
q         | Filter records by keyword | String
status    | Filters the records returned by status. Example: created | String
active    | Filter by active, inactive, or all records (Example: true) | String
type      | Filter records by type (Example: hulu, youtube, crunchyroll) | String
id        | Query for a video import by id | String
id!       | Exclude records by ID | String
video_source_id | Query by video source | String


#### Response
200
Content-Type: application/json

<pre><code>{
  "response"=> [
    {
      "_id"=>"5499c02d4c616e0545000000",
      "active"=>true,
      "created_at"=>"2014-12-23T14:19:09.369-05:00",
      "description"=>
        "She came to the Tiny Desk a little unsure, and left singing \"West Memphis\" with intensity and passion ...",
      "duration"=>1195,
      "episode"=>nil,
      "etag"=>"\"F9iA7pnxqNgrkOutjQAa9F2k8HY/RVSzO8IXeqRD4Xh1SisxwseyKvk\"",
      "keywords"=>[],
      "published_at"=>"2014-12-22T18:03:09.000-05:00",
      "season"=>nil,
      "site_id"=>"12345abcd",
      "status"=>"ready",
      "thumbnails"=>
      [
        {"aspect_ratio"=>nil,
        "height"=>90,
        "name"=>nil,
        "url"=>"https://i.ytimg.com/vi/mTu4cXW9H_Q/default.jpg",
        "width"=>120},
        ...
      ],
    "title"=>"Lucinda Williams: NPR Music Tiny Desk Concert",
    "updated_at"=>"2014-12-23T14:19:09.369-05:00",
    "upload_id"=>nil,
    "video_id"=>nil,
    "video_source_id"=>"5499c0274c616e04b8110000",
    "youtube_id"=>"mTu4cXW9H_Q"
  }],
  "pagination"=>{"current"=>1, "previous"=>nil, "next"=>2, "per_page"=>1, "pages"=>500}}
</code></pre>

<hr>
### Retrieve a Video Import
<hr>
<pre><code><b>GET</b> https://api.zype.com/video_imports/{id}
</code></pre>

#### Response
200
Content-Type: application/json
<pre><code>{
  "response": {
    "_id": "5499c0334c616e0545bd0200",
    "active": true,
    "created_at": "2014-12-23T14:19:15.926-05:00",
    "description": "The members of Real Estate are awfully young to pine for their lost youth, but nostalgia remains crucial ",
    "duration": 3117,
    "episode": null,
    "etag": "\"F9iA7pnxqNgrkOutjQAa9F2k8HY/OANWyL7bhxMQ9uLewq1i4tvdD6o\"",
    "published_at": "2014-03-25T16:39:22.000-04:00",
    "season": null,
    "site_id": "5468f40d4c616e0a770c0000",
    "status": "ready",
    "thumbnails": [
    {
      "aspect_ratio": null,
      "height": 90,
      "name": null,
      "url": "https://i.ytimg.com/vi/O2AeQDIw2j4/default.jpg",
      "width": 120
    },
    {
      "aspect_ratio": null,
      "height": 180,
      "name": null,
      "url": "https://i.ytimg.com/vi/O2AeQDIw2j4/mqdefault.jpg",
      "width": 320
    },
    {
      "aspect_ratio": null,
      "height": 360,
      "name": null,
      "url": "https://i.ytimg.com/vi/O2AeQDIw2j4/hqdefault.jpg",
      "width": 480
    }
    ],
      "title": "Real Estate, 'Atlas' | NPR MUSIC FRONT ROW",
      "updated_at": "2014-12-23T14:19:15.926-05:00",
      "upload_id": null,
      "video_id": null,
      "video_source_id": "5499c0274c616e04b8110000",
      "youtube_id": "O2AeQDIw2j4"
    }
  }

</code></pre>

<hr>
### Add Video from a Video Import
<hr>
<pre><code><b>PUT</b> https://api.zype.com/video_imports/{id}/add_video/&video_id=video_id
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
video_id  | ID of a video to add video import to (Example: 5389352e69702d401b000000) | String

#### Request

Content-Type: application/json

#### Response
201
Content-Type: application/json

<pre><code>{
  "response"=> {
    "_id"=>"549b3e8a4c616e04f4040000",
    "active"=>false,
    "country"=>nil,
    "created_at"=>"2014-12-24T17:30:34.674-05:00",
    "data_sources"=>
      [
      {"_id"=>"549b3e8a4c616e04f4050000",
    "active"=>true,
    "duration"=>1369,
    "status"=>"ready",
    "youtube_id"=>"G7NapIZ1xGE",
    "thumbnails"=>
      [
      {"_id"=>"5499c0344c616e05450f0300", "aspect_ratio"=>nil, "height"=>90, "name"=>nil, "url"=>"https://i.ytimg.com/vi/G7NapIZ1xGE/default.jpg", "width"=>120},
      {"_id"=>"5499c0344c616e0545100300", "aspect_ratio"=>nil, "height"=>180, "name"=>nil, "url"=>"https://i.ytimg.com/vi/G7NapIZ1xGE/mqdefault.jpg", "width"=>320},
      {"_id"=>"5499c0344c616e0545110300", "aspect_ratio"=>nil, "height"=>360, "name"=>nil, "url"=>"https://i.ytimg.com/vi/G7NapIZ1xGE/hqdefault.jpg", "width"=>480},
      {"_id"=>"5499c0344c616e0545120300", "aspect_ratio"=>nil, "height"=>480, "name"=>nil, "url"=>"https://i.ytimg.com/vi/G7NapIZ1xGE/sddefault.jpg", "width"=>640},
      {"_id"=>"5499c0344c616e0545130300", "aspect_ratio"=>nil, "height"=>720, "name"=>nil, "url"=>"https://i.ytimg.com/vi/G7NapIZ1xGE/maxresdefault.jpg", "width"=>1280}]}
      ],
    "description"=> "Angel Olsen came to the Tiny Desk on an odd autumn day ...",
    "duration"=>1369,
    "episode"=>nil,
    "featured"=>false,
    "foreign_id"=>nil,
    "keywords"=>[],
    "mature_content"=>false,
    "published_at"=>"2014-01-27T15:06:34.000-05:00",
    "rating"=>0.0,
    "related_playlist_ids"=>[],
    "request_count"=>0,
    "season"=>nil,
    "site_id"=>"5468f40d4c616e0a770c0000",
    "status"=>"created",
    "subscription_required"=>false,
    "title"=>"Angel Olsen: NPR Music Tiny Desk Concert",
    "updated_at"=>"2014-12-24T17:30:34.674-05:00",
    "zobject_ids"=>[],
    "thumbnails"=>
      [
        {"aspect_ratio"=>nil, "height"=>90, "name"=>nil, "url"=>"https://i.ytimg.com/vi/G7NapIZ1xGE/default.jpg", "width"=>120},
        {"aspect_ratio"=>nil, "height"=>180, "name"=>nil, "url"=>"https://i.ytimg.com/vi/G7NapIZ1xGE/mqdefault.jpg", "width"=>320},
        {"aspect_ratio"=>nil, "height"=>360, "name"=>nil, "url"=>"https://i.ytimg.com/vi/G7NapIZ1xGE/hqdefault.jpg", "width"=>480},
        {"aspect_ratio"=>nil, "height"=>480, "name"=>nil, "url"=>"https://i.ytimg.com/vi/G7NapIZ1xGE/sddefault.jpg", "width"=>640},
      {"aspect_ratio"=>nil, "height"=>720, "name"=>nil, "url"=>"https://i.ytimg.com/vi/G7NapIZ1xGE/maxresdefault.jpg", "width"=>1280}
    ]
  }
}
</pre></code>
