---
layout: default
title: Zype Developer Portal | Device Categories
permalink: /api_docs/device_categories/
---

## Device Categories
<hr>
### List all Device Categories
<hr>

<pre><code>GET - https://api.zype.com/device_categories?page=page&per_page=per_page&search=search
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
page | The page number of records to return (zero indexed). Example: 0. | Number
per_page | The number of records to return. Example: 10. | Number
search | Performs a full text search for the term and returns records that match. Example: Mobile | String

#### Response
200
Content-Type: application/json

<pre><code>{
  "response": [
    {
      "&#95;id": "541b14f6636261c814040000",
      "&#95;keywords": [
      "desktop"
      ],

      "created_at": "2014-09-22T16:02:11.113Z",
      "image_content_type": "image/png",
      "image_file_name": "desktop.png",
      "image_file_size": 19347,
      "image_fingerprint": "a661d27f5003bcf1523f75e3686f6b24",
      "image_updated_at": "2014-09-22T16:02:11.041+00:00",
      "name": "Desktop",
      "updated_at": "2014-09-22T16:02:11.113Z"
      },
{
    "&#95;id": "54204804636261f298050000",
    "&#95;keywords": [
    "mobile"
    ],

    "created_at": "2014-09-22T16:02:12.319Z",
    "image_content_type": "image/png",
    "image_file_name": "mobile.png",
    "image_file_size": 18671,
    "image_fingerprint": "070c15b95b315a6f472a6efb6c3b898c",
    "image_updated_at": "2014-09-22T16:02:12.299+00:00",
    "name": "Mobile",
    "updated_at": "2014-09-22T16:02:12.319Z"
},
{
    "&#95;id": "54204804636261f298060000",
    "&#95;keywords": [
    "ott"
    ],

    "created_at": "2014-09-22T16:02:12.578Z",
    "image_content_type": "image/png",
    "image_file_name": "desktop.png",
    "image_file_size": 19347,
    "image_fingerprint": "a661d27f5003bcf1523f75e3686f6b24",
    "image_updated_at": "2014-09-22T16:02:12.558+00:00",
    "name": "OTT",
    "updated_at": "2014-09-22T16:02:12.578Z"
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
### Retrieve a Device Category
<hr>

<pre><code>GET - https://api.zype.com/device_categories/{id}
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id | String id of the Device Category to retrieve. Example: 5389352e69702d401b000000. | String

#### Response
200
Content-Type: application/json

<pre><code>{
  "response": {
    "&#95;id": "54204803636261f298040000",
    "&#95;keywords": [
      "desktop"
    ],
    "created_at": "2014-09-22T16:02:11.113Z",
    "image_content_type": "image/png",
    "image_file_name": "desktop.png",
    "image_file_size": 19347,
    "image_fingerprint": "a661d27f5003bcf1523f75e3686f6b24",
    "image_updated_at": "2014-09-22T16:02:11.041+00:00",
    "name": "Desktop",
    "updated_at": "2014-09-22T16:02:11.113Z"
  }
}
