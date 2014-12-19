---
layout: api
title: Zype Developer Portal | Zobject Types
permalink: /api_docs/zobject_types/
---

## Zobject Types Collection
<hr>
### List all Zobject Types
<hr>
<pre><code>GET - https://api.zype.com/zobject_types?page=page&per_page=per_page&keywords=keyword
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
page      | The page number of records to return (zero indexed). Example: 0. | Number
per_page  | The number of records to return. Example: 10. | Number
keywords  | Filters the records returned by keyword. Example: comedy. | String

#### Response
200
Content-Type: application/json

<pre><code>{
  "response": [
  {
    "_id":"546cd8124c616e043d010000",
    "_keywords": ["actor"],
    "created_at": "2014-11-19T12:49:06.385-05:00",
    "description": "",
    "site_id": "545932274c616e2359000000",
    "title": "actor",
    "updated_at": "2014-11-19T12:49:06.385-05:00",
    "videos_enabled": true,
    "zobject_count": 2
  },
  {
    "_id": "546cd8324c616e043d020000",
    "_keywords": ["director"],
    "created_at": "2014-11-19T12:49:38.521-05:00",
    "description": "",
    "site_id": "545932274c616e2359000000",
    "title": "director",
    "updated_at": "2014-11-19T12:49:38.521-05:00",
    "videos_enabled": true,
    "zobject_count": 2
  }
  ],
  "pagination":
  {
    "current": 1,
    "previous": null,
    "next": null,
    "per_page": 10,
    "pages": 1
  }
}
</code></pre>
<hr>
### Create a Zobject Type
<hr>

<pre><code>POST - https://api.zype.com/zobject_types?page=page&per_page=per_page&keywords=keyword
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
zobject_type | A set of key value pairs that describe the Zobject Type. | Hash

#### Request
Content-Type: application/json

#### Response
201
Content-Type: application/json

<pre><code>{
  "response": {
    "_id":"54908d574c616e20e73b0000",
    "_keywords":
    [
      "new",
      "type",
      "zobject"
    ],
    "created_at":"2014-12-16T14:51:51.302-05:00",
    "description":null,
    "site_id":"545932274c616e2359000000",
    "title":"new zobject type!",
    "updated_at":"2014-12-16T14:51:51.302-05:00",
    "videos_enabled":true,
    "zobject_count":0
  }
}
</code></pre>

Lists descriptive information about a Zobject type.
<hr>
### Retrieve a Zobject Type
<hr>
<pre><code>GET - https://api.zype.com/zobject_types/{id}
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id | String id of the Zobject Type to retrieve. Example: 5389352e69702d401b000000. | String

#### Response
200
Content-Type: application/json

<pre><code>{
  "response": [
    {
      "_id": "5464f94569702d5349720000",
      "_keywords": [
      "actor"
      ],
      "created_at": "2014-11-13T13:32:37.284-05:00",
      "description": "",
      "site_id": "5463c68e69702d24db490000",
      "title": "actor",
      "updated_at": "2014-11-14T14:14:12.757-05:00",
      "videos_enabled": true,
      "zobject_attributes": [
        {
          "_id": "5464f94569702d5349730000",
          "created_at": "2014-11-13T13:32:37.284-05:00",
          "description": "The actor's name.",
          "field_name": "name",
          "field_type": "String",
          "show_list": true,
          "updated_at": "2014-11-13T13:32:37.284-05:00"
        }
      ],
      "zobject_count": 7
    }
  ]
}
</code></pre>
<hr>
### Update a Zobject Type
<hr>

<pre><code>PUT - https://api.zype.com/zobject_types/{id}
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
zobject_type   | A set of key value pairs that describe the Zobject Type. | Hash

#### Request
Content-Type: application/json

#### Response
201
Content-Type: application/json

<pre><code>{
  "response": [
    {
      "_id": "5464f94569702d5349720000",
      "_keywords": [
      "actor"
      ],
      "created_at": "2014-11-13T13:32:37.284-05:00",
      "description": "",
      "site_id": "5463c68e69702d24db490000",
      "title": "actor",
      "updated_at": "2014-11-14T14:14:12.757-05:00",
      "videos_enabled": true,
      "zobject_attributes": [
      {
        "_id": "5464f94569702d5349730000",
        "created_at": "2014-11-13T13:32:37.284-05:00",
        "description": "The actor's name.",
        "field_name": "name",
        "field_type": "String",
        "show_list": true,
        "updated_at": "2014-11-13T13:32:37.284-05:00"
      }
      ],
      "zobject_count": 7
    }
  ]
}
</code></pre>
<hr>
### Delete a Zobject Type
<hr>

<pre><code>DELETE - https://api.zype.com/zobject_types/{id}
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id | String id of the Zobject Type to remove. Example: 5389352e69702d401b000000. | String

#### Response
204

No Content
