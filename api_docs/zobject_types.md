---
layout: api
title: Zype Developer Portal | Zobject Types
permalink: /api_docs/zobject_types/
redirect_to: https://docs.zype.com/reference#zobject-types
---

## Zobject Types
<hr />
### List Zobject Types
<pre>
<b>GET</b> https://api.zype.com/zobject_types
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | Filter records by ID | String
id!       | Exclude records by ID | String
page | The page number of records to return (Example: 1) | Integer
per_page | The number of records to return (Example: 10) | Integer
q         | Filter records by keyword | String


### Retrieve a Zobject Type
<pre><b>GET</b> https://api.zype.com/zobject_types/[id]
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | ID of the record (Example: 5389352e69702d401b000000) | String

### Create a Zobject Type
<pre><b>POST</b> https://api.zype.com/zobject_types
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
zobject_type[title] | Title of the zobject type (must be unique) | String
zobject_type[description] | Description of the zobject type | String
zobject_type[videos_enabled] | Indicates whether videos can be associated with instances of the zobject type | String
zobject_type[zobject_attributes] | An indexed collection specifying the custom attributes for the zobject type | Array
zobject_type[zobject_attributes][x][field_name] | Name of the zobject type custom attribute | String
zobject_type[zobject_attributes][x][field_type] | Type of the zobject type custom attribute. Example: integer | String
zobject_type[zobject_attributes][x][description] | Description of the zobject type custom attribute | String

### Update a Zobject Type
<pre><b>PUT</b> https://api.zype.com/zobject_types/[id]</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id | ID of the record to update (Example: 540731274c616e047a000000) | String
zobject_type[title] | Title of the zobject type (must be unique) | String
zobject_type[description] | Description of the zobject type | String
zobject_type[videos_enabled] | Indicates whether videos can be associated with instances of the zobject type | String
zobject_type[zobject_attributes] | An indexed collection specifying the custom attributes for the zobject type | Array
zobject_type[zobject_attributes][x][id] | ID of the record to update | String
zobject_type[zobject_attributes][x][field_name] | Name of the zobject type custom attribute | String
zobject_type[zobject_attributes][x][field_type] | Type of the zobject type custom attribute. Example: integer | String
zobject_type[zobject_attributes][x][description] | Description of the zobject type custom attribute | String

### Delete a Zobject Type
<pre><b>DELETE</b> https://api.zype.com/zobject_types/[id]
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id | ID of the record to be deleted. Example: 540731274c616e047a000000 | String

### Zobject Type Object

<pre>
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
}
</pre>


