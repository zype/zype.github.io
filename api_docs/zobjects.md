---
layout: api
title: Zype Developer Portal | Zobjects
permalink: /api_docs/zobjects/
---

## Zobjects Collection
<hr>
### List Zobjects
<pre><b>GET</b> https://api.zype.com/zobjects</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
custom    | Filter records by custom attribues (Example: color=blue) | String
order     | Sort records in ascending or descending order (Example: asc/desc) | String
page | The page number of records to return (Example: 1) | Integer
per_page | The number of records to return (Example: 10) | Integer
q         | Filter records by keyword | String
sort      | Sort records on the specified field | String
zobject_type | The type of zobject (Example: guest) | String

### Create a Zobject
<pre><b>POST</b> https://api.zype.com/zobjects</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
zobject_type | The type of zobject | String
zobject[active] | Whether or not the zobject is active | Boolean
zobject[custom]    | Custom attributes for the zobject (Example: zobject[color]=blue) | String
zobject[description] | The description of the zobject | String
zobject[friendly_title] | The friendly title of the zobject | String
zobject[keywords] | Keywords for the zobject | Array
zobject[title] | The title of the zobject | String

### Retrieve a Zobject
<pre><b>GET</b> https://api.zype.com/zobjects/[id]</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id | ID of the record to retrieve (Example: 5389352e69702d401b000000) | String
zobject_type | The type of zobject (Example: guest) | String

### Update a Zobject
<pre><b>PUT</b> https://api.zype.com/zobjects/[id]</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id | ID of the record to update (Example: 540731274c616e047a000000) | String
zobject_type | The type of zobject | String
zobject[active] | Whether or not the zobject is active | Boolean
zobject[custom][custom_attribute]    | Custom attributes for the zobject (Example: zobject[custom][color]=blue) | String
zobject[description] | The description of the zobject | String
zobject[friendly_title] | The friendly title of the zobject | String
zobject[keywords] | Keywords for the zobject | Array
zobject[title] | The title of the zobject | String

### Delete a Zobject
<pre><b>DELETE</b> https://api.zype.com/zobjects/[id]</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id | ID of the record to delete (Example: 5389352e69702d401b000000) | String
zobject_type | The type of zobject (Example: guest) | String


### Add Videos(s) to Zobject
<pre><b>PUT</b> https://api.zype.com/zobjects/[id]/add_videos</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | ID of the record (Example: 5389352e69702d401b000000) | String
video_id[] | The video IDs to add | Array
zobject_type | The type of zobject (Example: guest) | String

### Remove Videos(s) from Zobject
<pre><b>PUT</b> https://api.zype.com/zobjects/[id]/remove_videos</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | ID of the record (Example: 5389352e69702d401b000000) | String
video_id[] | The video IDs to remove | Array
zobject_type | The type of zobject (Example: guest) | String

### Zobject Object
<pre>
{
  "_id": "549dc72d636872c09d1f0000",
  "active": true,
  "created_at": "2014-12-26T15:38:05.447-05:00",
  "description": "",
  "friendly_title": "jamie-foxx",
  "keywords": [],
  "site_id": "549dc583636872c09d110000",
  "title": "Jamie Foxx",
  "updated_at": "2014-12-26T16:45:30.419-05:00",
  "video_ids": [],
  "zobject_type_id": "549dc71f636872c09d1d0000",
  "zobject_type_title": "actor"
}
</pre>