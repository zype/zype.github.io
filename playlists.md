---
layout: default
title: Playlists
permalink: /playlists/
---

## Playlists Collection

Lists all Playlists. Playlist information includes descriptive information about the playlist.
<hr>
### List all Playlists
<hr>
<pre><code>GET - https://api.zype.com/playlists?page=page&per_page=per_page&
active=active&keyword=keyword&category=category
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
page | The page number of records to return (zero indexed). Example: 0. | Number
per_page | The number of records to return. Example: 10. | Number
keyword | Filters the records returned by keyword. Example: comedy. | String
active | Filters the records by whether active or not. Example: true. | String
category | An optional set of key value category pairs to filter the records returned by category. Example: category[color]=blue. | Hash

#### Response
200
Content-Type: application/json

<pre><code>{
    response: [
        {
            &#95;id: "540735534c616e047a030000",
            &#95;keywords: [
                "first",
                "playlist"
            ],
            active: true,
            "categories": [
                {
                    "title": "color",
                    "value": "green"
                }
            ],
            created_at: "2014-09-03T15:35:47.328Z",
            description: "This is the first playlist",
            site_id: "53fe307f4c616e914e000000",
            title: "First Playlist",
            updated_at: "2014-09-03T15:36:22.172Z"
        }
    ],
    pagination: {
        current: 1,
        previous: null,
        next: null,
        per_page: 10,
        pages: 1
    }
}
</code></pre>
<hr>
### Create a Playlist
<hr>
<pre><code>POST - https://api.zype.com/playlists?page=page&per_page=per_page&
active=active&keyword=keyword&category=category
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
playlist | A set of key value pairs that describe the Playlist | Hash

#### Request

Content-Type: application/json

#### Response
201
Content-Type: application/json

<pre><code>{
    response: {
        &#95;id: "540735534c616e047a030000",
        &#95;keywords: [
            "first",
            "playlist"
        ],
        active: true,
        "categories": [
            {
                "title": "color",
                "value": "green"
            }
        ],
        created_at: "2014-09-03T15:35:47.328Z",
        description: "This is the first playlist",
        site_id: "53fe307f4c616e914e000000",
        title: "First Playlist",
        updated_at: "2014-09-03T15:36:22.172Z"
    }
}
</code></pre>

## Playlist

Lists descriptive information about Playlist.

<hr>
### Retrieve a Playlist
<hr>
<pre><code>GET - https://api.zype.com/playlists/{id}
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id | String id of the Playlist to retrieve. Example: 5389352e69702d401b000000. | Number

#### Request
Content-Type: application/json

#### Response
200
Content-Type: application/json

<pre><code>{
    response: {
        &#95;id: "540735534c616e047a030000",
        &#95;keywords: [
            "first",
            "playlist"
        ],
        active: true,
        "categories": [
            {
                "title": "color",
                "value": "green"
            }
        ],
        created_at: "2014-09-03T15:35:47.328Z",
        description: "This is the first playlist",
        site_id: "53fe307f4c616e914e000000",
        title: "First Playlist",
        updated_at: "2014-09-03T15:36:22.172Z"
    }
}
</code></pre>

<hr>
### Update a Playlist
<hr>
<pre><code>PUT - https://api.zype.com/playlists/{id}
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
playlist | A set of key value pairs that describe the playlist. | Hash

#### Request
Content-Type: application/json

#### Response
201
Content-Type: application/json

<pre><code>{
    response: [
        {
            &#95;id: "540735534c616e047a030000",
            &#95;keywords: [
                "first",
                "playlist"
            ],
            active: true,
            "categories": [
                {
                    "title": "color",
                    "value": "green"
                }
            ],
            created_at: "2014-09-03T15:35:47.328Z",
            description: "This is the first playlist",
            site_id: "53fe307f4c616e914e000000",
            title: "First Playlist",
            updated_at: "2014-09-03T15:36:22.172Z"
        }
    ]
}
</code></pre>
<hr>
### Remove a Playlist
<hr>
<pre><code>DELETE - https://api.zype.com/playlists/{id}
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id | String id of the Playlist to remove. Example: 5389352e69702d401b000000. | Number

#### Request
Content-Type: application/json

#### Response
200
Content-Type: application/json

<pre><code>{
    response: [
        {
            &#95;id: "540735534c616e047a030000",
            &#95;keywords: [
                "first",
                "playlist"
            ],
            active: true,
            "categories": [
                {
                    "title": "color",
                    "value": "green"
                }
            ],
            created_at: "2014-09-03T15:35:47.328Z",
            description: "This is the first playlist",
            site_id: "53fe307f4c616e914e000000",
            title: "First Playlist",
            updated_at: "2014-09-03T15:36:22.172Z"
        }
    ]
}
</code></pre>
