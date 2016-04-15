---
layout: api
title: Zype Developer Portal | Categories
permalink: /api_docs/categories/
---

## Categories
<hr />
### List Categories
<pre>
<b>GET</b> https://api.zype.com/categories
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | Query for a category by ID | String
id!       | Exclude a category from the query | String
q         | A query string for searching for categories | String
title     | Filter categories by title | String
page | The page number of records to return (zero indexed). Example: 0. | Number
per_page | The number of records to return. Example: 10. | Number

###Retrieve a Category
<pre><b>GET</b> https://api.zype.com/categories/[id]
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | ID of the category. Example: 5389352e69702d401b000000. | String

###Create a Category
<pre><b>POST</b> https://api.zype.com/categories
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
category[title] | Title of the category | String
category[values] | Values for the category | Array

###Update a Category
<pre><b>PUT</b> https://api.zype.com/categories/[id]</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id | ID of the category to update. Example: 540731274c616e047a000000. | String
category[title] | Title of the category | String
category[values] | Values for the category | Array

###Delete a Category
<pre><b>DELETE</b> https://api.zype.com/categories/[id]
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id | ID of the category to be deleted. Example: 540731274c616e047a000000. | String

### Category Object

<pre>
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
</pre>