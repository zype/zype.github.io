---
layout: default
title: Revenue Models
permalink: /api_docs/revenue_models/
---

## Revenue Models
<hr>
### List all Revenue Models
<hr>
<pre><code>GET - https://api.zype.com/revenue_models?page=page&per_page=per_page&search=search
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
page | The page number of records to return (zero indexed). Example: 0. | Number
per_page | The number of records to return. Example: 10. | Number
search | Performs a full text search for the term and returns records that match. Example: SVOD | String

#### Response
200
Content-Type: application/json

<pre><code>{
"response": [
  {
    "&#95;id": "54204802636261f298030000",
    "&#95;keywords": [
      "free"
    ],
    "created_at": "2014-09-22T16:02:10.785Z",
    "description": "Free",
    "name": "Free",
    "updated_at": "2014-09-22T16:02:10.785Z"
  },
  {
    "&#95;id": "54204802636261f298020000",
    "&#95;keywords": [
      "demand",
      "subscription",
      "svod",
      "video"
    ],
    "created_at": "2014-09-22T16:02:10.783Z",
    "description": "Subscription Video On Demand",
    "name": "SVOD",
    "updated_at": "2014-09-22T16:02:10.783Z"
  },
  {
    "&#95;id": "54204802636261f298010000",
    "&#95;keywords": [
      "advertising",
      "avod",
      "demand",
      "video"
    ],
    "created_at": "2014-09-22T16:02:10.781Z",
    "description": "Advertising Video On Demand",
    "name": "AVOD",
    "updated_at": "2014-09-22T16:02:10.781Z"
  },
  {
    "&#95;id": "54204802636261f298000000",
    "&#95;keywords": [
      "electronic",
      "est",
      "sell",
      "through"
    ],
    "created_at": "2014-09-22T16:02:10.778Z",
    "description": "Electronic sell-through",
    "name": "EST",
    "updated_at": "2014-09-22T16:02:10.778Z"
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
### Retrieve a Revenue Model
<hr>

<pre><code>GET - https://api.zype.com/revenue_models/{id}
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id | String id of the Revenue Model to retrieve. Example: 5389352e69702d401b000000. | Number

#### Response
200
Content-Type: application/json

<pre><code>{
  "response": {
    "&#95;id": "54204802636261f298030000",
    "&#95;keywords": [
      "free"
    ],
    "created_at": "2014-09-22T16:02:10.785Z",
    "description": "Free",
    "name": "Free",
    "updated_at": "2014-09-22T16:02:10.785Z"
  }
}
</code></pre>
