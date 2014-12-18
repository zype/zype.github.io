---
layout: api
title: Zype Developer Portal | Categories
permalink: /api_docs/categories/
---

## Categories Collection

Lists all Categories.
<hr>
### List all Categories
<hr>
<pre><code>GET - https://api.zype.com/categories?page=page&per_page=per_page
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
page | The page number of records to return (zero indexed). Example: 0. | Number
per_page | The number of records to return. Example: 10. | Number

#### Request
Content-Type: application/json

#### Response
200
Content-Type: application/json

<pre><code>{
  "response": [
  {
    "_id": "546782ee69702d2328350000",
    "_keywords": [
    "additional",
    "videos",
    "youtube"
    ],
    "created_at": "2014-11-15T11:44:30.700-05:00",
    "site_id": "5463c68e69702d24db490000",
    "title": "Additional Videos from YouTube",
    "updated_at": "2014-11-15T11:44:30.700-05:00",
    "values": [
    "Yes"
    ]
  },
  {
    "_id": "546763ee69702d4efa260000",
    "_keywords": [
      "series"
    ],
    "created_at": "2014-11-15T09:32:14.575-05:00",
    "site_id": "5463c68e69702d24db490000",
    "title": "series",
    "updated_at": "2014-11-15T11:02:59.329-05:00",
    "values": [
      "12 Monkeys",
      "13 Assassins",
      "2 Fast 2 Furious",
      "A Little Princess",
      "A Night at the Roxbury"
    ]
  },
  {
    "_id": "5463e49f69702d34ff0d0000",
    "_keywords": [
      "genre"
    ],
    "created_at": "2014-11-12T17:52:15.547-05:00",
    "site_id": "5463c68e69702d24db490000",
    "title": "Genre",
    "updated_at": "2014-11-15T09:53:12.784-05:00",
    "values": [
      "Adventure",
      "Comedy",
      "Horror"
    ]
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
### Create a Category
<hr>
<pre><code>POST - https://api.zype.com/categories?page=page&per_page=per_page
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
category | A set of key value pairs that describe the Category | Hash

#### Request
Content-Type: application/json

#### Response
201
Content-Type: application/json

<pre><code>{  
  "response":
  {  
    "_id": "54907f944c616e20e7270000",
    "_keywords":
    [
    "favorite",
    "pizza",
    "toppings"
    ],
    "created_at": "2014-12-16T13:53:08.564-05:00",
    "site_id": "545932274c616e2359000000",
    "title": "Favorite Pizza Toppings",
    "updated_at": "2014-12-16T13:53:08.564-05:00",
    "values":
    [
      "Mushroom,
      Pepperoni"
    ]
  }
}
</code></pre>

## Category

Lists descriptive information about a Category.
<hr>
### Retrieve a Category
<hr>
<pre><code>GET - https://api.zype.com/categories/{id}
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id | String id of the Category to retrieve. Example: 540731274c616e047a000000. | String

#### Request
Content-Type: application/json

### Response
200
Content-Type: application/json

<pre><code>{
  "response":
  {
    "_id": "548f5b8e4c616e8031010000",
    "_keywords":
    [
      "Over",
      "9000"
    ],
    "created_at": "2014-12-15T17:07:10.481-05:00",
    "site_id": "545932274c616e2359000000",
    "title": "Is it over 9000?",
    "updated_at": "2014-12-15T17:07:10.481-05:00",
    "values":
    [
      "yes",
      "no"
    ]
  }
}
</code></pre>
<hr>
### Update a Catgeory
<hr>
<pre><code>PUT - https://api.zype.com/categories/{id}
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id | String id of the Category to update. Example: 5389352e69702d401b000000. | String

#### Request
Content-Type: application/json

#### Response
201
Content-Type: application/json

<pre><code>
{
  "response":
  {
    "_id": "548f5b8e4c616e8031010000",
    "_keywords":
    [
      "Definitely",
      "Over",
      "9000"
    ],
    "created_at": "2014-12-15T17:07:10.481-05:00",
    "site_id": "545932274c616e2359000000",
    "title": "Definitely Over 9000",
    "updated_at": "2014-12-16T13:53:08.266-05:00",
    "values":
    [
      "yes",
      "no"
    ]
  }
}
</code></pre>
<hr>
### Remove a Category
<hr>
<pre><code>DELETE - https://api.zype.com/categories/{id}
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id | String id of the Category to remove. Example: 5389352e69702d401b000000. | Number

#### Request
Content-Type: application/json

#### Response
204

No Content
