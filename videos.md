---
layout: default
title: Videos
permalink: /videos/
---

## Videos

**Videos Collection** - lists all Videos

Video information includes descriptive information about the video but does not include player embed codes.

### List all Videos
<pre><code>
GET - http://zype.apiary-mock.com/videos?page=page&
per_page=per_page&keyword=keyword&status=status&
active=true&type=type&category=category
</code></pre>

#### Parameters

##### page
The page number of records to return (zero indexed). Example: 0. (Number)

##### per_page
The number of records to return. Example: 10. (Number)

##### keyword
Filters the records returned by keyword. Example: comedy. (String)

##### status
Filters the records returned by status. Example: created. (String)

##### active
Show active, inactive or all videos Example: true. (String)

##### type
Show videos of the specified type (zype, youtube, hulu) Example: zype. (String)

##### category
An optional set of key value category pairs to filter the records returned by category. Example: category[color]=blue. (Hash)

#### Request & Response

<pre><code>
200
Content-Type: application/json
{
    response : [
        {
            _id: "5389352e69702d401a000000",
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

### Create a Video

<pre><code>
POST - http://zype.apiary-mock.com/videos?page=page&
per_page=per_page&keyword=keyword&status=status&
active=true&type=type&category=category
</code></pre>

#### Parameters

##### Video
A set of key value pairs that describe the Video. (Hash)

**Video Lists** descriptive information about Videos

t Video

Update a Video

Remove a Video

**Player Lists** - player content

You need to supply your player key in addition to your API key.
