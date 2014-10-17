---
layout: default
title: Zype Developer Portal | Zobject Types
permalink: /api_docs/zobject_types/
---

## Zobject Types Collection
<hr>
### List all Zobject Types
<hr>
<pre><code>GET - https://api.zype.com/zobject_types?page=page&per_page=per_page&keywords=keyword
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
page      | The page number of records to return (zero indexed). Example: 0. | Number
per_page  | The number of records to return. Example: 10. | Number
keywords  | Filters the records returned by keyword. Example: comedy. | String

#### Response
200
Content-Type: application/json

<pre><code>{
    response : [
        {
            &#95;id: "5407412b4c616e047a0f0000",
            &#95;keywords: [
                "Actor"
            ],
            created_at: "2014-09-03T16:26:19.680Z",
            description: "Actor Card",
            site_id: "53fe307f4c616e914e000000",
            title: "Actor
            updated_at: "2014-09-03T16:26:19.680Z",
            videos_enabled: true,
            zobject_attributes: [
                {
                    &#95;id: "5407412b4c616e047a100000",
                    created_at: "2014-09-03T16:26:19.680Z",
                    description: "name of actor",
                    field_name: "name",
                    field_type: "String",
                    show_list: false,
                    updated_at: "2014-09-03T16:26:19.680Z"
                }
            ],
            "zobject_count": 2
        },
        pagination: {
            current: 1,
            previous: null,
            next: 2,
            per_page: 10,
            pages: 1
        }
    ]
}
</code></pre>
<hr>
## Create a Zobject Type
<hr>

<pre><code>POST - https://api.zype.com/zobject_types?page=page&per_page=per_page&keywords=keyword
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
zobject_type | A set of key value pairs that describe the Zobject Type. | Hash

#### Request
Content-Type: application/json

#### Response
201
Content-Type: application/json

<pre><code>{
    response: {
        &#95;id: "5407412b4c616e047a0f0000",
        &#95;keywords: [
            "Actor"
        ],
        created_at: "2014-09-03T16:26:19.680Z",
        description: "Actor Card",
        site_id: "53fe307f4c616e914e000000",
        title: "ctor
        updated_at: "2014-09-03T16:26:19.680Z",
        videos_enabled: true,
        zobject_attributes: [
            {
                &#95;id: "5407412b4c616e047a100000",
                created_at: "2014-09-03T16:26:19.680Z",
                description: "name of actor",
                field_name: "name",
                field_type: "String",
                show_list: false,
                updated_at: "2014-09-03T16:26:19.680Z"
            } ...
        ],
        "zobject_count": 2
    }
}
</code></pre>

## Zobject Type

Lists descriptive information about Zobjects.
<hr>
### Zobject Type
<hr>
<pre><code>GET - https://api.zype.com/zobject_types/{id}
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id | String id of the Zobject Type to retrieve. Example: 5389352e69702d401b000000. | String

#### Response
200
Content-Type: application/json

<pre><code>{
    response :
        {
            &#95;id: "5407412b4c616e047a0f0000",
            &#95;keywords: [
                "Actor"
            ],
            created_at: "2014-09-03T16:26:19.680Z",
            description: "Actor Card",
            site_id: "53fe307f4c616e914e000000",
            title: "ctor
            updated_at: "2014-09-03T16:26:19.680Z",
            videos_enabled: true,
            zobject_attributes: [
                {
                    &#95;id: "5407412b4c616e047a100000",
                    created_at: "2014-09-03T16:26:19.680Z",
                    description: "name of actor",
                    field_name: "name",
                    field_type: "String",
                    show_list: false,
                    updated_at: "2014-09-03T16:26:19.680Z"
                } ...
            ],
            "zobject_count": 2
        }
}
</code></pre>
<hr>
### Update a Zobject Type
<hr>

<pre><code>PUT - https://api.zype.com/zobject_types/{id}
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
zobject_type   | A set of key value pairs that describe the Zobject Type. | Hash

#### Request
Content-Type: application/json

#### Response
201
Content-Type: application/json

<pre><code>{
    response :
        {
            &#95;id: "5407412b4c616e047a0f0000",
            &#95;keywords: [
                "Actor"
            ],
            created_at: "2014-09-03T16:26:19.680Z",
            description: "Actor Card",
            site_id: "53fe307f4c616e914e000000",
            title: "ctor
            updated_at: "2014-09-03T16:26:19.680Z",
            videos_enabled: true,
            zobject_attributes: [
                {
                    &#95;id: "5407412b4c616e047a100000",
                    created_at: "2014-09-03T16:26:19.680Z",
                    description: "name of actor",
                    field_name: "name",
                    field_type: "String",
                    show_list: false,
                    updated_at: "2014-09-03T16:26:19.680Z"
                } ...
            ],
            "zobject_count": 2
        }
}
</code></pre>
<hr>
### Remove a Zobject Type
<hr>

<pre><code>DELETE - https://api.zype.com/zobject_types/{id}
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id | String id of the Zobject Type to remove. Example: 5389352e69702d401b000000. | String

#### Response
200
Content-Type: application/json

<pre><code>{
    response :
        {
            &#95;id: "5407412b4c616e047a0f0000",
            &#95;keywords: [
                "Actor"
            ],
            created_at: "2014-09-03T16:26:19.680Z",
            description: "Actor Card",
            site_id: "53fe307f4c616e914e000000",
            title: "ctor
            updated_at: "2014-09-03T16:26:19.680Z",
            videos_enabled: true,
            zobject_attributes: [
                {
                    &#95;id: "5407412b4c616e047a100000",
                    created_at: "2014-09-03T16:26:19.680Z",
                    description: "name of actor",
                    field_name: "name",
                    field_type: "String",
                    show_list: false,
                    updated_at: "2014-09-03T16:26:19.680Z"
                }
            ],
            "zobject_count": 2
        }
}
</code></pre>
