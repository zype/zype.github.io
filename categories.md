---
layout: default
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
    response : [
        {
            &#95;id: "540731274c616e047a000000",
            &#95;keywords: [
                "type",
                "video"
            ],
            created_at: "2014-08-05T16:17:29.670Z",
            site_id: "53fe307f4c616e914e000000",
            title: "video_type",
            updated_at: "2014-08-26T18:26:54.461Z",
            values: [
                "Film",
                "TV",
                "Originals"
            ]
        }
    ],
    pagination: {
        current: 1,
        previous: null,
        next: 2,
        per_page: 10,
        pages: 1
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
    response: {
        &#95;id: "540731274c616e047a000000",
        &#95;keywords: [
            "type",
            "video"
        ],
        created_at: "2014-08-05T16:17:29.670Z",
        site_id: "53fe307f4c616e914e000000",
        title: "video_type",
        updated_at: "2014-08-26T18:26:54.461Z",
        values: [
            "Film",
            "TV",
            "Originals"
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
id | String id of the Category to retrieve. Example: 540731274c616e047a000000. | Number

#### Request
Content-Type: application/json

### Response
200
Content-Type: application/json

<pre><code>{
    response : {
        &#95;id: "540731274c616e047a000000",
        &#95;keywords: [
            "type",
            "video"
        ],
        created_at: "2014-08-05T16:17:29.670Z",
        site_id: "53fe307f4c616e914e000000",
        title: "video_type",
        updated_at: "2014-08-26T18:26:54.461Z",
        values: [
            "Film",
            "TV",
            "Originals"
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
id | String id of the Category to update. Example: 5389352e69702d401b000000. | Number

#### Request
Content-Type: application/json

#### Response
201
Content-Type: application/json

<pre><code>{
    response : [
        {
            &#95;id: "540731274c616e047a000000",
            &#95;keywords: [
                "type",
                "video"
            ],
            created_at: "2014-08-05T16:17:29.670Z",
            site_id: "53fe307f4c616e914e000000",
            title: "video_type",
            updated_at: "2014-08-26T18:26:54.461Z",
            values: [
                "Film",
                "TV",
                "Originals"
            ]
        }
    ]
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
200
Content-Type: application/json

<pre><code>{
    response : [
        {
            &#95;id: "540731274c616e047a000000",
            &#95;keywords: [
                "type",
                "video"
            ],
            created_at: "2014-08-05T16:17:29.670Z",
            site_id: "53fe307f4c616e914e000000",
            title: "video_type",
            updated_at: "2014-08-26T18:26:54.461Z",
            values: [
                "Film",
                "TV",
                "Originals"
            ]
        }
    ]
}
</code></pre>
