---
layout: default
title: Device Categories
permalink: /device_categories/
---

## Device Categories
<hr>
### List all Device Categories
<hr>

<pre><code>
GET - http://zype.apiary-mock.com/device_categories?page=page&per_page=per_page&search=search
</code></pre>

#### Parameters

##### page
The page number of records to return (zero indexed). Example: 0. (Number)

##### per_page
The number of records to return. Example: 10. (Number)

##### search
Performs a full text search for the term and returns records that match. Example: Mobile (String)

#### Response
200
Content-Type: application/json
<pre><code>
{
  "response": [
    {
      "_id": "541b14f6636261c814040000",
      "_keywords": [
      "desktop"
      ],

      "created_at": "2014-09-18T17:23:02.270Z",
      "image_content_type": null,
      "image_file_name": null,
      "image_file_size": null,
      "image_fingerprint": null,
      "image_updated_at": null,
      "name": "Desktop",
      "updated_at": "2014-09-18T17:23:02.270Z"
  },
  {
      "_id": "541b14f6636261c814050000",
      "_keywords": [
      "mobile"
      ],

      "created_at": "2014-09-18T17:23:02.273Z",
      "image_content_type": null,
      "image_file_name": null,
      "image_file_size": null,
      "image_fingerprint": null,
      "image_updated_at": null,
      "name": "Mobile",
      "updated_at": "2014-09-18T17:23:02.273Z"
  },
  {
      "_id": "541b14f6636261c814060000",
      "_keywords": [
      "ott"
      ],

      "created_at": "2014-09-18T17:23:02.275Z",
      "image_content_type": null,
      "image_file_name": null,
      "image_file_size": null,
      "image_fingerprint": null,
      "image_updated_at": null,
      "name": "OTT",
      "updated_at": "2014-09-18T17:23:02.275Z"
  }
  ],
  
  "pagination": {
  "current": 1,
  "previous": null,
  "next": null,
  "per_page": 10,
  "pages": 1
  }
}_
</code></pre>

<hr>
### Retrieve a Device Category
<hr>

<pre><code>
GET - http://zype.apiary-mock.com/device_categories/id
</code></pre>

#### Parameters

##### id

String id of the Video to retrieve. Example: 5389352e69702d401b000000. (Number)

#### Response
200
Content-Type: application/json
<pre><code>
{
  "response": {
      "_id": "541b14f6636261c814040000",
      "_keywords": [
      "desktop"
      ],

      "created_at": "2014-09-18T17:23:02.270Z",
      "image_content_type": null,
      "image_file_name": null,
      "image_file_size": null,
      "image_fingerprint": null,
      "image_updated_at": null,
      "name": "Desktop",
      "updated_at": "2014-09-18T17:23:02.270Z"
  }
}_
</code></pre>
