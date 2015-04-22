---
layout: api
title: Zype Developer Portal | Distribution Endpoints
permalink: /api_docs/distribution_endpoints/
---

## Distribution Endpoints
<hr>
### List all Distribution Endpoints
<hr>
<pre><code>GET - https://api.zype.com/distribution_endpoints?page=page&per_page=per_page
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
page | The page number of records to return (zero indexed). Example: 0. | Number
per_page | The number of records to return. Example: 10. | Number

#### Response
200
Content-Type: application/json

<pre><code>{
"response": [
    {
      "_id":"5536b4fc636261a7821b0000",
      "_keywords":
        [
          "beats",
          "brooklyn",
          "publishingendpoint",
          "vhx"
        ],
      "access_token": "451a682f9d6661b8c10a49bc114fad8860234212db4ec56fefb9a80fc58511db",
      "created_at": "2015-04-21T16:37:17.056-04:00",
      "deleted_at": null,
      "editable": true,
      "expires_at": 1429741238,
      "name": "Brooklyn Beats",
      "package_id": null,
      "refresh_token": "d19a53cc0115484d2bf42d26a169d2ae602e884821064d33e342725d18173d60",
      "refreshed_at": null,
      "site_id": "53c0457969702d4d66000000",
      "updated_at": "2015-04-22T16:20:38.919-04:00",
      "vhx_site_id": 11208
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

### Retrieve a Distribution Endpoint
<hr>
<pre><code>GET - https://api.zype.com/distribution_endpoints/{id}?page=page&per_page=per_page
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id | String id of the Distribution Endpoint to retrieve. Example: 5389352e69702d401b000000. | String


#### Response
200
Content-Type: application/json

<pre><code>{
"response":
  {
    "_id": "5536b4fc636261a7821b0000",
    "_keywords": [
      "beats",
      "brooklyn",
      "publishingendpoint",
      "vhx"
    ],
    "access_token": "451a682f9d6661b8c10a49bc114fad8860234212db4ec56fefb9a80fc58511db",
    "created_at": "2015-04-21T16:37:17.056-04:00",
    "deleted_at": null,
    "editable": true,
    "expires_at": 1429741238,
    "name": "Brooklyn Beats",
    "package_id": null,
    "refresh_token": "d19a53cc0115484d2bf42d26a169d2ae602e884821064d33e342725d18173d60",
    "refreshed_at": null,"site_id":"53c0457969702d4d66000000",
    "updated_at": "2015-04-22T16:20:38.919-04:00",
    "vhx_site_id": 11208
  }
}
