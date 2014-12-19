---
layout: api
title: Zype Developer Portal | Devices
permalink: /api_docs/devices/
---

## Devices
<hr>
### List all Devices
<hr>
<pre><code>GET - https://api.zype.com/devices?page=page&per_page=per_page&search=search
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
page | The page number of records to return (zero indexed). Example: 0. | Number
per_page | The number of records to return. Example: 10. | Number
search | Performs a full text search for the term and returns records that match. Example: Android | String

#### Response
200
Content-Type: application/json

<pre><code>{
"response": [
  {
    id": "54204805636261f298090000",
    keywords": [
      "accessed",
      "android",
      "chrome",
      "html5",
      "via"
    ],

    "created_at": "2014-09-22T16:02:13.578Z",
    "description": "Accessed via Chrome",
    "device_category_id": "54204804636261f298050000",
    "image_content_type": "image/png",
    "image_file_name": "mobile.png",
    "image_file_size": 18671,
    "image_fingerprint": "070c15b95b315a6f472a6efb6c3b898c",
    "image_updated_at": "2014-09-22T16:02:13.558+00:00",
    "name": "Chrome Android (HTML5)",
    "player_ids": [
      "54204808636261f298110000",
      "54204808636261f298100000"
    ],
    "updated_at": "2014-09-22T16:02:13.578Z"
},
  {
    id": "54204805636261f298080000",
    keywords": [
      "accessed",
      "html5",
      "ios",
      "safari",
      "via"
    ],
    "created_at": "2014-09-22T16:02:13.340Z",
    "description": "Accessed via Safari",
    "device_category_id": "54204804636261f298050000",
    "image_content_type": "image/png",
    "image_file_name": "ipod.png",
    "image_file_size": 18751,
    "image_fingerprint": "8e0e0c15cd7149f35eb3c6c17f1b5a7b",
    "image_updated_at": "2014-09-22T16:02:13.320+00:00",
    "name": "Safari iOS (HTML5)",
    "player_ids": [
      "54204808636261f298110000",
      "54204808636261f298100000"
    ],
    "updated_at": "2014-09-22T16:02:13.340Z"
},
  id": "54204804636261f298070000"keywords": [
      "accessed",
      "browser",
      "desktop",
      "html5",
      "via",
      "web"
    ],
    "created_at": "2014-09-22T16:02:13.057Z",
    "description": "Accessed via desktop HTML5 web browser",
    "device_category_id": "54204803636261f298040000",
    "image_content_type": "image/png",
    "image_file_name": "desktop.png",
    "image_file_size": 19347,
    "image_fingerprint": "a661d27f5003bcf1523f75e3686f6b24",
    "image_updated_at": "2014-09-22T16:02:13.036+00:00",
    "name": "Desktop Browser (HTML5)",
    "player_ids": [
      "54204808636261f298110000",
      "54204808636261f298100000",
      "54204808636261f2980f0000"
    ],
    "updated_at": "2014-09-22T16:02:13.057Z"
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
### Retrieve a Device
<hr>

<pre><code>GET - https://api.zype.com/devices/{id}
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id | String id of the Device to retrieve. Example: 5389352e69702d401b000000. | String

#### Response
200
Content-Type: application/json

<pre><code>{
  "response": {
    "id": "54204805636261f298090000",
    "keywords": [
      "accessed",
      "android",
      "chrome",
      "html5",
      "via"
    ],
    "created_at": "2014-09-22T16:02:13.578Z",
    "description": "Accessed via Chrome",
    "device_category_id": "54204804636261f298050000",
    "image_content_type": "image/png",
    "image_file_name": "mobile.png",
    "image_file_size": 18671,
    "image_fingerprint": "070c15b95b315a6f472a6efb6c3b898c",
    "image_updated_at": "2014-09-22T16:02:13.558+00:00",
    "name": "Chrome Android (HTML5)",
    "player_ids": [
      "54204808636261f298110000",
      "54204808636261f298100000"
    ],
    "updated_at": "2014-09-22T16:02:13.578Z"
  }
}
</code></pre>
