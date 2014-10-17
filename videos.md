---
layout: default
title: Zype Developer Portal | Videos
permalink: /api_docs/videos/
---

## Videos Collection
Lists all Videos. Video information includes descriptive information about the video,
but does not include player embed codes.
<hr>
### List all Videos
<hr>
<pre><code>GET - https://api.zype.com/videos?page=page&per_page=per_page&
keyword=keyword&status=status&active=true&type=type&category=category
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
page      | The page number of records to return (zero indexed). Example: 0. | Number
per_page  | The number of records to return. Example: 10. | Number
keyword   | Filters the records returned by keyword. Example: comedy. | String
status    | Filters the records returned by status. Example: created. | String
active    | Show active, inactive or all videos Example: true. | String
category  | An optional set of key value category pairs to filter the records returned by category. Example: category[color]=blue. | Hash

#### Response
200
Content-Type: application/json

<pre><code>{
    response : [
        {
            &#95;id: "5389352e69702d401a000000",
            active: true,
            ad_timings: [
                {
                    mode: "off",
                    time: 0,
                    type: "in"
                }
            ],
            created_at: "2014-05-31T01:49:49.388Z",
            description: null,
            duration: 1217,
            featured: false,
            foreign_id: null,
            keywords: [
                "example",
                "video"
            ],
            published_at: null,
            site_id: 1,
            thumbnails: [
                {
                    height: 240,
                    name: null,
                    width: 426,
                    url: "http://t1.zype.com/5389352e69702d401b000000/1/53a2f27069702d260f050000/00001.png"
                },
                {
                    height: 360,
                    name: null,
                    width: 640,
                    url: "http://t1.zype.com/5389352e69702d401b000000/1/53a2f9d069702d26cf000000/00001.png"
                },
                {
                    height: 480,
                    name: null,
                    width: 854,
                    url: "http://t1.zype.com/5389352e69702d401b000000/1/53a2f9fb69702d26cf010000/00001.png"
                }
            ],
            title: "Example Video",
            updated_at: "2014-06-19T20:27:53.958Z",
            upload_id: "5385c92c69702d589f170000",
            video_source_id: null
        ]
    },
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
### Create a Video
<hr>
<pre><code>POST - https://api.zype.com/videos?page=page&per_page=per_page&
keyword=keyword&status=status&active=true&type=type&category=category
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
Video     | A set of key value pairs that describe the Video. | Hash

#### Response
201
Content-Type: application/json

<pre><code>{
    response: {
        &#95;id: "5389352e69702d401a000000",
        active: true,
        ad_timings: [
            {
                mode: "off",
                time: 0,
                type: "in"
            }
        ],
        created_at: "2014-05-31T01:49:49.388Z",
        description: null,
        duration: 1217,
        featured: false,
        foreign_id: null,
        keywords: [
            "example",
            "video"
        ],
        published_at: null,
        site_id: 1,
        thumbnails: [
            {
                height: 240,
                name: null,
                width: 426,
                url: "http://t1.zype.com/5389352e69702d401b000000/1/53a2f27069702d260f050000/00001.png"
            },
            {
                height: 360,
                name: null,
                width: 640,
                url: "http://t1.zype.com/5389352e69702d401b000000/1/53a2f9d069702d26cf000000/00001.png"
            },
            {
                height: 480,
                name: null,
                width: 854,
                url: "http://t1.zype.com/5389352e69702d401b000000/1/53a2f9fb69702d26cf010000/00001.png"
            }
        ],
        title: "Example Video",
        updated_at: "2014-06-19T20:27:53.958Z",
        upload_id: "5385c92c69702d589f170000",
        video_source_id: null
    }
}
</code></pre>

## Video
Lists descriptive information about Videos
<hr>
###Retrieve a Video
<hr>
<pre><code>GET - https://api.zype.com/videos/{id}
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | String id of the Video to retrieve. Example: 5389352e69702d401b000000. | String

#### Request
Content-Type: application/json

#### Response
200
Content-Type: application/json

<pre><code>{
    response : {
        &#95;id: "5389352e69702d401a000000",
        active: true,
        ad_timings: [
            {
                mode: "off",
                time: 0,
                type: "in"
            }
        ],
        created_at: "2014-05-31T01:49:49.388Z",
        description: null,
        duration: 1217,
        featured: false,
        foreign_id: null,
        keywords: [
            "example",
            "video"
        ],
        published_at: null,
        site_id: 1,
        thumbnails: [
            {
                height: 240,
                name: null,
                width: 426,
                url: "http://t1.zype.com/5389352e69702d401b000000/1/53a2f27069702d260f050000/00001.png"
            },
            {
                height: 360,
                name: null,
                width: 640,
                url: "http://t1.zype.com/5389352e69702d401b000000/1/53a2f9d069702d26cf000000/00001.png"
            },
            {
                height: 480,
                name: null,
                width: 854,
                url: "http://t1.zype.com/5389352e69702d401b000000/1/53a2f9fb69702d26cf010000/00001.png"
            }
        ],
        title: "Example Video",
        updated_at: "2014-06-19T20:27:53.958Z",
        upload_id: "5385c92c69702d589f170000",
        video_source_id: null
    }
}
</code></pre>
<hr>
### Update a Video
<hr>
<pre><code>PUT - https://api.zype.com/videos/{id}
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
Video     | A set of key value pairs that describe the video. Example: video[description]=description. | Hash

#### Request

Content-Type: application/json

#### Response
201
Content-Type: application/json

<pre><code>{
    response : {
        &#95;id: "5389352e69702d401a000000",
        active: true,
        ad_timings: [
            {
                mode: "off",
                time: 0,
                type: "in"
            }
        ],
        created_at: "2014-05-31T01:49:49.388Z",
        description: null,
        duration: 1217,
        featured: false,
        foreign_id: null,
        keywords: [
            "example",
            "video"
        ],
        published_at: null,
        site_id: 1,
        thumbnails: [
            {
                height: 240,
                name: null,
                width: 426,
                url: "http://t1.zype.com/5389352e69702d401b000000/1/53a2f27069702d260f050000/00001.png"
            },
            {
                height: 360,
                name: null,
                width: 640,
                url: "http://t1.zype.com/5389352e69702d401b000000/1/53a2f9d069702d26cf000000/00001.png"
            },
            {
                height: 480,
                name: null,
                width: 854,
                url: "http://t1.zype.com/5389352e69702d401b000000/1/53a2f9fb69702d26cf010000/00001.png"
            }
        ],
        title: "Example Video",
        updated_at: "2014-06-19T20:27:53.958Z",
        upload_id: "5385c92c69702d589f170000",
        video_source_id: null
    }
}
</code></pre>
<hr>
###Remove a Video
<hr>
<pre><code>DELETE - https://api.zype.com/videos/{id}
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | String id of the Video to remove. Example: 5389352e69702d401b000000. | String

#### Request
Content-Type: application/json

#### Response
200
Content-Type: application/json

<pre><code>{
    response : {
        &#95;id: "5389352e69702d401a000000",
        active: true,
        ad_timings: [
            {
                mode: "off",
                time: 0,
                type: "in"
            }
        ],
        created_at: "2014-05-31T01:49:49.388Z",
        description: null,
        duration: 1217,
        featured: false,
        foreign_id: null,
        keywords: [
            "example",
            "video"
        ],
        published_at: null,
        site_id: 1,
        thumbnails: [
            {
                height: 240,
                name: null,
                width: 426,
                url: "http://t1.zype.com/5389352e69702d401b000000/1/53a2f27069702d260f050000/00001.png"
            },
            {
                height: 360,
                name: null,
                width: 640,
                url: "http://t1.zype.com/5389352e69702d401b000000/1/53a2f9d069702d26cf000000/00001.png"
            },
            {
                height: 480,
                name: null,
                width: 854,
                url: "http://t1.zype.com/5389352e69702d401b000000/1/53a2f9fb69702d26cf010000/00001.png"
            }
        ],
        title: "Example Video",
        updated_at: "2014-06-19T20:27:53.958Z",
        upload_id: "5385c92c69702d589f170000",
        video_source_id: null
    }
}
</code></pre>

## Player
Lists player content. You need to supply your player key in addition to your API key.
<hr>
### Retrieve a Player
<hr>
<pre><code>GET - https://api.zype.com/videos/{id}/player?autoplay=autoplay
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | String id of the Video to retrieve. Example: 5389352e69702d401b000000. | String
autoplay  | Optional boolean value to indicate whether the player should automatically start. Example: false. | Boolean

#### Request
Content-Type: application/json

#### Response
200
Content-Type: application/json

<pre><code>{
    response : {
        body: "[Video player embed code]"
    }

}
</code></pre>
