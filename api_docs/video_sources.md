---
layout: api
title: Zype Developer Portal | Video Sources
permalink: /api_docs/video_sources/
---

## Video Sources Collection
<hr>
### List all Video Sources
<hr>
<pre><code><b>GET</b> https://api.zype.com/video_sources?page=page&per_page=per_page&
keyword=keyword
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
page      | The page number of records to return (Example: 1) | Integer
per_page  | The number of records to return (Example: 10) | Integer
q         | Filter records by keyword | String
type      | The type of video sources to query. Example: zype, hulu, youtube, crunchyroll | String
id        | Query for a video source by id | String
id!       | Exclude records by ID | String

#### Response
200
Content-Type: application/json


<pre><code>{
  "response": [
  {
    "_id": "5468f40d4c616e0a770d0000",
    "_keywords": [
    "videosource",
    "zype"
    ],
    "created_at": "2014-11-16T13:59:25.420-05:00",
    "deleteable": false,
    "editable": false,
    "name": "Zype",
    "provider_id": "5429b1ca69702d2f7c190000",
    "refreshed_at": null,
    "site_id": "5468f40d4c616e0a770c0000",
    "updated_at": "2014-11-16T13:59:25.420-05:00",
    "video_count": 0
    },
    {
      "_id": "5499c0274c616e04b8110000",
      "created_at": "2014-12-23T14:19:04.025-05:00",
      "deleteable": true,
      "editable": true,
      "guid": "UC4eYXhJI4-7wSWc8UNRwD4A",
      "name": "YouTube",
      "provider_id": "5429b1cb69702d2f7c1a0000",
      "refreshed_at": "2014-12-23T14:19:04.156-05:00",
      "site_id": "5468f40d4c616e0a770c0000",
      "updated_at": "2014-12-23T14:19:45.552-05:00",
      "video_count": 0
      },
      {
        "_id": "549b4dac4c616e3a3e000000",
        "_keywords": [
        "hbo",
        "john",
        "oliver",
        "show",
        "videosource",
        "youtube"
        ],
        "created_at": "2014-12-24T18:35:08.982-05:00",
        "deleteable": true,
        "editable": true,
        "guid": "UC3XTzVzaHQEd30rQbuvCtTQ",
        "name": "John Oliver HBO Show!!!",
        "provider_id": "5429b1cb69702d2f7c1a0000",
        "refreshed_at": null,
        "site_id": "5468f40d4c616e0a770c0000",
        "updated_at": "2014-12-24T18:42:03.155-05:00",
        "video_count": 0
      }
      ],
      "pagination": {
        "current": 1,
        "previous": null,
        "next": null,
        "per_page": 10,
        "pages": 1
      }
    }
</code></pre>

<hr>
### Create a Video Source
<hr>
<pre><code><b>POST</b> https://api.zype.com/video_sources/?source=source&video_source[attributes]=attributes
</code></pre>

Parameter | Function | Type
--------- | -------- | ----
source    | The source of the video sources. Example: hulu, youtube, crunchyroll | String
video_source[name] | Name of the video source | String
video_source[guid] | Guid of the video source | String


#### Response
201
Content-Type: application/json

<pre><code>{
  "response"=>
  {
    "_id"=>"549b4dac4c616e3a3e000000",
    "created_at"=>"2014-12-24T18:35:08.982-05:00",
    "deleteable"=>true,
    "editable"=>true,
    "guid"=>"UC3XTzVzaHQEd30rQbuvCtTQ",
    "name"=>"John Oliver HBO Show",
    "provider_id"=>"5429b1cb69702d2f7c1a0000",
    "refreshed_at"=>nil,
    "site_id"=>"5468f40d4c616e0a770c0000",
    "updated_at"=>"2014-12-24T18:35:08.982-05:00",
    "video_count"=>0
  }
}
</code></pre>

<hr>
### Retrieve a Single Video Source
<hr>
<pre><code><b>GET</b> https://api.zype.com/video_sources/{id}/
</code></pre>

#### Response
200
Content-Type: application/json

<pre><code>{
  "response"=>
    {
      "_id"=>"549b4dac4c616e3a3e000000",
      "created_at"=>"2014-12-24T18:35:08.982-05:00",
      "deleteable"=>true,
      "editable"=>true,
      "guid"=>"UC3XTzVzaHQEd30rQbuvCtTQ",
      "name"=>"John Oliver HBO Show",
      "provider_id"=>"5429b1cb69702d2f7c1a0000",
      "refreshed_at"=>nil,
      "site_id"=>"5468f40d4c616e0a770c0000",
      "updated_at"=>"2014-12-24T18:35:08.982-05:00",
      "video_count"=>0
    }
}
</code></pre>

<hr>
### Update a Video Source
<hr>
<pre><code><b>PUT</b> https://api.zype.com/video_sources/{id}/?video_source[attributes]=attributes
</code></pre>

Parameter | Function | Type
--------- | -------- | ----
video_source[name] | Name of the video source | String
video_source[guid] | Guid of the video source | String


#### Response
201
Content-Type: application/json

<pre><code>{
  "response"=>
  {
    "_id"=>"549b4dac4c616e3a3e000000",
    "created_at"=>"2014-12-24T18:35:08.982-05:00",
    "deleteable"=>true,
    "editable"=>true,
    "guid"=>"UC3XTzVzaHQEd30rQbuvCtTQ",
    "name"=>"John Oliver HBO Show - UPDATED",
    "provider_id"=>"5429b1cb69702d2f7c1a0000",
    "refreshed_at"=>nil,
    "site_id"=>"5468f40d4c616e0a770c0000",
    "updated_at"=>"2014-12-24T18:35:08.982-05:00",
    "video_count"=>0
  }
}
</code></pre>

<hr>
### Delete a Video Source
<hr>
Note, you cannot delete a Zype video source.

<pre><code><b>DELETE</b> https://api.zype.com/video_sources/{id}/
</code></pre>

#### Response
204

No content
