---
layout: default
title: Zobjects
permalink: /zobjects/
---

## Zobjects Collection
<hr>
### List all Zobjects
<hr>
<pre><code>GET - https://api.zype.com/zobject/?zobject_type=zobject_type&page=page&per_page=per_page&keywords=keyword
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
zobject_type | The title of the zobject type. Required. Example: cards. | String
page      | The page number of records to return (zero indexed). Example: 0. | Number
per_page  | The number of records to return. Example: 10. | Number
keywords  | Filters the records returned by keyword. Example: comedy. | String

#### Response
200
Content-Type: application/json

<pre><code>{
    response : [
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
    ]
}
</code></pre>
<hr>
## Create a Zobject
<hr>

<pre><code>POST - https://api.zype.com/zobjects?page=page&per_page=per_page&keywords=keyword
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
    response: {
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
    }, ...
}
</code></pre>

## Zobject

Lists descriptive information about Zobjects.
<hr>
### Zobject
<hr>
<pre><code>GET - https://api.zype.com/zobjects/{id}/?zobject_type=zobject_type
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id | String id of the zobject to retrieve. Example: 5389352e69702d401b000000. | Number
zobject_type | The title of the zobject type. Required. Example:  | String

#### Response
200
Content-Type: application/json

<pre><code>{
    response :
        {
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

<pre><code>PUT - https://api.zype.com/zobjects/{id}
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
zobject   | A set of key value pairs that describe the zobject. | Hash

#### Request
Content-Type: application/json

#### Response
201
Content-Type: application/json

<pre><code>{
    response :
      {
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
### Remove a Zobject
<hr>

<pre><code>DELETE - https://api.zype.com/zobjects/{id}/?zobject_type=zobject_type
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id | String id of the zobject to remove. Example: 5389352e69702d401b000000. | Number
zobject_type | The title of the zobject type. Required. Example: cards. | String

#### Response
200
Content-Type: application/json

<pre><code>{
    response :
        {
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
