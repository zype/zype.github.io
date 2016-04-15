---
layout: api
title: Zype Developer Portal | Zobjects
permalink: /api_docs/zobjects/
---

## Zobjects Collection
<hr>
### List all Zobjects
<hr>
<pre><code><b>GET</b> https://api.zype.com/zobjects/?zobject_type=zobject_type&page=page&per_page=per_page&keywords=keyword
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
zobject_type | The title of the zobject type. Required. Example: card. | String
page      | The page number of records to return (zero indexed). Example: 0. | Number
per_page  | The number of records to return. Example: 10. | Number
keywords  | Filters the records returned by keyword. Example: comedy. | String

#### Response
200
Content-Type: application/json

<pre><code>{
  "response": [
  {
    "_id": "5464f99369702d5349750000",
    "active": true,
    "created_at": "2014-11-13T13:33:55.435-05:00",
    "description": "",
    "friendly_title": "steve-carell",
    "keywords": [],
    "name": "Steve Carell",
    "site_id": "5463c68e69702d24db490000",
    "title": "Steve Carell",
    "updated_at": "2014-11-14T14:15:33.490-05:00",
    "video_ids": [
      "5463d2d369702d0ece500000"
    ],
    "zobject_type_id": "5464f94569702d5349720000",
    "zobject_type_title": "actor"
  },
  {
    "_id": "5464f92869702d7c9c540000",
    "active": true,
    "created_at": "2014-11-13T13:32:08.903-05:00",
    "description": "",
    "friendly_title": "jack-black",
    "keywords": [],
    "name": "Jack Black",
    "site_id": "5463c68e69702d24db490000",
    "title": "Jack Black",
    "updated_at": "2014-11-14T14:15:33.497-05:00",
    "video_ids": [
      "5463d4df69702d51f1140000"
    ],
    "zobject_type_id": "5464f94569702d5349720000",
    "zobject_type_title": "actor"
    }
  ]
}
</code></pre>
<hr>
### Create a Zobject
<hr>

<pre><code><b>POST</b> https://api.zype.com/zobjects?page=page&per_page=per_page&keywords=keyword
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
zobject | A set of key value pairs that describe the Zobject. | Hash

#### Request
Content-Type: application/json

#### Response
201
Content-Type: application/json

<pre><code>{
  "response": {
    "_id": "542b182c69702d73796d1100",
    "active": true,
    "alternate_name": "-",
    "attack": 1500,
    "created_at": "2014-09-30T20:53:00.926Z",
    "defense": 800,
    "description": null,
    "featured": false,
    "friendly_name": "blackland-fire-dragon",
    "friendly_title": "blackland-fire-dragon",
    "keywords": [],
    "level": "4",
    "rank": "-",
    "site_id": "12345abcde",
    "sort_order": 0,
    "tgc_link": "http://www.db.yugioh-card.com/yugiohdb/card_search.action?ope=2&cid=4016",
    "title": "Blackland Fire Dragon",
    "title_jp": "暗黒の竜王",
    "tv_only": false,
    "updated_at": "2014-09-30T20:53:00.926Z",
    "video_ids": [],
    "zobject_type_id": "53a4788c69702d5995630300",
    "zobject_type_title": "card"
  }
}
</code></pre>

## Zobject

Lists descriptive information about Zobjects.
<hr>
### Retrieve a Zobject
<hr>
<pre><code><b>GET</b> https://api.zype.com/zobjects/{id}/?zobject_type=zobject_type
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id | ID of the zobject to retrieve. Example: 5389352e69702d401b000000. | String
zobject_type | The title of the zobject type. Required. Example: card.  | String

#### Response
200
Content-Type: application/json

<pre><code>{
  "response": {
    "_id": "542b182c69702d73796d1100",
    "active": true,
    "alternate_name": "-",
    "attack": 1500,
    "created_at": "2014-09-30T20:53:00.926Z",
    "defense": 800,
    "description": null,
    "featured": false,
    "friendly_name": "blackland-fire-dragon",
    "friendly_title": "blackland-fire-dragon",
    "keywords": [],
    "level": "4",
    "rank": "-",
    "site_id": "12345abcde",
    "sort_order": 0,
    "tgc_link": "http://www.db.yugioh-card.com/yugiohdb/card_search.action?ope=2&cid=4016",
    "title": "Blackland Fire Dragon",
    "title_jp": "暗黒の竜王",
    "tv_only": false,
    "updated_at": "2014-09-30T20:53:00.926Z",
    "video_ids": [],
    "zobject_type_id": "53a4788c69702d5995630300",
    "zobject_type_title": "card"
  }
}
</code></pre>
<hr>
### Update a Zobject
<hr>

<pre><code><b>PUT</b> https://api.zype.com/zobjects/{id}
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id | ID of the zobject to retrieve. Example: 5389352e69702d401b000000. | String
zobject   | A set of key value pairs that describe the zobject. | Hash


#### Request
Content-Type: application/json

#### Response
201
Content-Type: application/json

<pre><code>{
  "response": {
    "_id": "542b182c69702d73796d1100",
    "active": true,
    "alternate_name": "-",
    "attack": 1500,
    "created_at": "2014-09-30T20:53:00.926Z",
    "defense": 800,
    "description": null,
    "featured": false,
    "friendly_name": "blackland-fire-dragon",
    "friendly_title": "blackland-fire-dragon",
    "keywords": [],
    "level": "4",
    "rank": "-",
    "site_id": "12345abcde",
    "sort_order": 0,
    "tgc_link": "http://www.db.yugioh-card.com/yugiohdb/card_search.action?ope=2&cid=4016",
    "title": "Blackland Fire Dragon",
    "title_jp": "暗黒の竜王",
    "tv_only": false,
    "updated_at": "2014-09-30T20:53:00.926Z",
    "video_ids": [],
    "zobject_type_id": "53a4788c69702d5995630300",
    "zobject_type_title": "card"
  }
}
</code></pre>

<hr>
### Associate Videos with a Zobject
<hr>

<pre><code><b>PUT</b> https://api.zype.com/zobjects/{id}/add_videos?zobject_type=type&video_id=[id00001, id00002]
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id | ID of the zobject to retrieve. Example: 5389352e69702d401b000000. | String
zobject_type | The title of the zobject type. Required. Example: card.  | String
video_id | An array containing the id's of the video you want to associate with this zobject | Array of Strings

#### Request
Content-Type: application/json

#### Response
201
Content-Type: application/json
<pre><code>{
  "response": {
    "_id": "549dc72d636872c09d1f0000",
    "active": true,
    "created_at": "2014-12-26T15:38:05.447-05:00",
    "description": "",
    "friendly_title": "jamie-foxx",
    "keywords": [],
    "site_id": "549dc583636872c09d110000",
    "title": "Jamie Foxx",
    "updated_at": "2014-12-26T16:40:03.670-05:00",
    "video_ids": ["549dc599636872c09d1a0000"],
    "zobject_type_id": "549dc71f636872c09d1d0000",
    "zobject_type_title": "actor"
  }
}
</code></pre>

<hr>
### Remove Associated Videos from a Zobject
<hr>

<pre><code><b>PUT</b> https://api.zype.com/zobjects/{id}//remove_videos?zobject_type=type&video_id=[id00001, id00002]
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id | ID of the zobject to retrieve. Example: 5389352e69702d401b000000. | String
zobject_type | The title of the zobject type. Required. Example: card.  | String
video_id | An array containing the id's of the videos you want to dissociate from this zobject | Array of Strings

#### Request
Content-Type: application/json

#### Response
200

Content-Type: application/json
<pre><code>{
  "response":
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
}
</code></pre>

<hr>
### Remove a Zobject
<hr>
<pre><code><b>DELETE</b> https://api.zype.com/zobjects/{id}/?zobject_type=type
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id | ID of the zobject to remove. Example: 5389352e69702d401b000000. | String
zobject_type | The title of the zobject type. Required. Example: card.  | String

#### Request
Content-Type: application/json

#### Response
204

No Content
