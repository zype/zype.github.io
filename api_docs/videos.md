---
layout: api
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
q         | A query string for searching for videos | String
keyword   | Filters the records returned by keyword. Example: comedy. | String
status    | Filters the records returned by status. Example: created. | String
active    | Show active, inactive or all videos Example: true. | String
type      | The type of videos to query. Example: Zype, Hulu, Youtube, Crunchyroll | String
id        | Query for a video by id | String
id!       | Exclude a video from the query | String
category  | An optional set of key value category pairs to filter the records returned by category. Example: category[color]=blue. | Hash
category! | Exclude a category from the query. Example: category![color] = blue | Hash
zobject_id  | Query for videos with a specific zobject associated with them | String
zobject_id! | Exclude videos with a specfific zobject associated with them | String
created_at | Filter the records returned by created date. You can use greater than or less than filters by adding a suffix: '.gt', '.gte', '.lt', 'lte'. Example: created_at.gte=2015-01-01 | Date
published_at | Filter the records returned by published date. You can use greater than or less than filters by adding a suffix: '.gt', '.gte', '.lt', 'lte'. Example: published_at.gte=2015-01-01 | Date

#### Response
200
Content-Type: application/json

<pre><code>{
  "response": [
  {
    "_id": "547b4dca69702d070dca0000",
    "active": true,
    "categories": [
      {
        "title": "Additional Videos from YouTube",
        "value": []
      },
      {
        "title": "Genre",
        "value": [
          "Adventure"
        ]
      },
      {
        "title": "series",
        "value": []
      }
    ],
    "country": "",
    "created_at": "2014-11-30T12:03:06.783-05:00",
    "description": "A continuation of the saga created by George Lucas set thirty years after Star Wars: Episode VI - Return of the Jedi (1983).",
    "duration": 91,
    "episode": null,
    "featured": false,
    "foreign_id": null,
    "keywords": [],
    "highlights": [],
    "mature_content": false,
    "published_at": "2014-11-30T12:01:32.000-05:00",
    "rating": 0,
    "related_playlist_ids": [
      "5464084f69702d76c1770000"
    ],
    "request_count": 14,
    "season": null,
    "site_id": "5463c68e69702d24db490000",
    "status": "created",
    "subscription_required": false,
    "title": "Star Wars: Episode VII - The Force Awakens Official Teaser Trailer",
    "updated_at": "2014-12-17T23:00:03.649-05:00",
    "video_zobjects": [
      {
        "_id": "547b4e6f69702d070dd30000",
        "description": "",
        "title": "Harrison Ford",
        "zobject_type_title": "actor"
      },
      {
        "_id": "547b4e9369702d070edc0000",
        "description": "",
        "title": "J.J. Abrams",
        "zobject_type_title": "director"
      },
      {
        "_id": "54808d6a69702d18b51d0000",
        "description": "",
        "title": "John Boyega",
        "zobject_type_title": "actor"
      }
    ],
    "zobject_ids": [
      "547b4e6f69702d070dd30000",
      "547b4e9369702d070edc0000",
      "54808d6a69702d18b51d0000"
    ],
    "thumbnails": [
      {
        "aspect_ratio": null,
        "height": 90,
        "name": null,
        "url": "https://i.ytimg.com/vi/PlFckE98xN4/default.jpg",
        "width": 120
      },
      {
        "aspect_ratio": null,
        "height": 180,
        "name": null,
        "url": "https://i.ytimg.com/vi/PlFckE98xN4/mqdefault.jpg",
        "width": 320
      },
      {
        "aspect_ratio": null,
        "height": 360,
        "name": null,
        "url": "https://i.ytimg.com/vi/PlFckE98xN4/hqdefault.jpg",
        "width": 480
      }
    ]
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
Video     | A set of key value pairs that describe the video | Hash
title | The title of the video | String
description | The description of the video | String
published_at  | The date and time that the video will appear to have been published | String
episode | The video's episode number | Integer
season | The video's season number | Integer
country | The country the video was created in | String
active | Whether or not the video is active | Boolean
featured | Whether or not the video is featured | Boolean
keywords | Keywords for the video | Array
subscription_required | Whether or not the video requires a subscription to view | Boolean
mature_content | Whether or not the video requires the viewer to be 18+ to view | Boolean

#### Response
201
Content-Type: application/json

<pre><code>{
  "response":
  {
    "_id": "549336916362613cf51f0000",
    "active": true,
    "country": nil,
    "created_at": "2014-12-18T15:18:25.744-05:00",
    "description": "Sample Description",
    "duration": nil,
    "episode": 1,
    "featured": false,
    "foreign_id": nil,
    "keywords": [],
    "highlights": [],
    "mature_content": false,
    "published_at": nil,
    "rating": 0.0,
    "related_playlist_ids": [],
    "request_count": 0,
    "season": 1,
    "site_id": "53c4296a69702d25ca000000",
    "status": "created",
    "subscription_required": false,
    "title": "Sample Video Title",
    "updated_at": "2014-12-18T15:18:25.744-05:00",
    "zobject_ids": [],
    "thumbnails": []
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
  "response":
  {
    "_id": "546529b669702d534fb00000",
    "active": true,
    "categories": [
      {
        "title": "Genre",
        "value": [
          "Adventure"
        ]
      },
      {
        "title": "Additional Videos from YouTube",
        "value": []
      },
      {
        "title": "series",
        "value": []
      }
    ],
    "country": "",
    "created_at": "2014-11-13T16:59:18.970-05:00",
    "description": "New trailer for Marvel's Avengers: The Age of Ultron!",
    "duration": 151,
    "episode": null,
    "featured": true,
    "foreign_id": null,
    "keywords": [],
    "highlights": [],
    "mature_content": false,
    "published_at": "2014-11-13T16:57:02.000-05:00",
    "rating": 0,
    "related_playlist_ids": [],
    "request_count": 39,
    "season": null,
    "site_id": "5463c68e69702d24db490000",
    "status": "created",
    "subscription_required": false,
    "title": "Avengers: Age of Ultron",
    "updated_at": "2014-12-17T23:00:14.215-05:00",
    "zobject_ids": [],
    "thumbnails": [
      {
      "aspect_ratio": null,
      "height": 90,
      "name": null,
      "url": "https://i.ytimg.com/vi/Kno4FTxWycI/default.jpg",
      "width": 120
      },
      {
      "aspect_ratio": null,
      "height": 180,
      "name": null,
      "url": "https://i.ytimg.com/vi/Kno4FTxWycI/mqdefault.jpg",
      "width": 320
      },
      {
        "aspect_ratio": null,
        "height": 360,
        "name": null,
        "url": "https://i.ytimg.com/vi/Kno4FTxWycI/hqdefault.jpg",
        "width": 480
      }
    ]
  }
}
</code></pre>
<hr>
### Update a Video
<hr>
<pre><code>PUT - https://api.zype.com/videos/{id}/&video[parameter]=value
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
video | A set of key value pairs that describe the video. Example: video[description]=description. | Hash
title | The title of the video | String
description | The description of the video | String
published_at  | The date and time that the video will appear to have been published | String
episode | The video's episode number | Integer
season | The video's season number | Integer
country | The country the video was created in | String
active | Whether or not the video is active | Boolean
featured | Whether or not the video is featured | Boolean
keywords | Keywords for the video | Array
subscription_required | Whether or not the video requires a subscription to view | Boolean
mature_content | Whether or not the video requires the viewer to be 18+ to view | Boolean

#### Request

Content-Type: application/json

#### Response
201
Content-Type: application/json

<pre><code>{
  "response":
  {
    "_id": "549336916362613cf51f0000",
    "active": true,
    "country": nil,
    "created_at": "2014-12-18T15:18:25.744-05:00",
    "description": "Sample Description",
    "duration": nil,
    "episode": 1,
    "featured": false,
    "foreign_id": nil,
    "keywords": [],
    "mature_content": false,
    "published_at": nil,
    "rating": 0.0,
    "related_playlist_ids": [],
    "request_count": 0,
    "season": 1,
    "site_id": "53c4296a69702d25ca000000",
    "status": "created",
    "subscription_required": false,
    "title": "Updated Video Title",
    "updated_at": "2014-12-18T15:54:11.787-05:00",
    "zobject_ids": [],
    "thumbnails": []
  }
}
</code></pre>

<hr>
###List the highlights of a Video
<hr>
<pre><code>GET - https://api.zype.com/videos/{id}/highlights
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | String id of the Video. Example: 5389352e69702d401b000000. | String

#### Request
Content-Type: application/json

#### Response
200
Content-Type: application/json
<pre><code>{
  "response": [
    {"_id": "54c6cbe56368726454050000",
    "description": "theBest",
    "end": 112,
    "start": 90
    }
  ]
}
</code></pre>


<hr>
###Find a specific highlight
<hr>
<pre><code>GET - https://api.zype.com/videos/{id}/highlights/{id}
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | String id of the Highlight. Example: 5389352e69702d401b000000. | String
video_id        | String id of the Video to which the highlight belongs. Example: 5389352e69702d401b000000. | String

#### Request
Content-Type: application/json

#### Response
200
Content-Type: application/json
<pre><code>{
  "response": [
    {"_id": "54c6cbe56368726454050000",
    "description": "theBest",
    "end": 112,
    "start": 90
    }
  ]
}
</code></pre>

<hr>
###Add highlights to a Video
<hr>
<pre><code>POST - https://api.zype.com/videos/{id}/highlights
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
highlight | A set of key value pairs that describe the highlight. Example: highlight[description]=description. | Hash
description | The description for the video highlight | String
start | The point in the video where the highlight begins | Integer
end | The point in the video where the highlight ends | Integer

#### Request
Content-Type: application/json

#### Response
201
Content-Type: application/json
<pre><code>{
  "response": [
    {"_id": "54c6cbe56368726454050000",
    "description": "Sample Description",
    "end": 411,
    "start": 380
    }
  ]
}
</code></pre>

<hr>
###Remove highlights from a Video
<hr>
<pre><code>DELETE - https://api.zype.com/videos/{id}/highlights/{id}
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | String id of the Highlight to be deleted. Example: 5389352e69702d401b000000. | String
video_id        | String id of the Video to which the highlight belongs. Example: 5389352e69702d401b000000. | String

#### Request
Content-Type: application/json

#### Response
204
Content-Type: application/json
<pre><code>{
  "response": No Content
}
</code></pre>

<hr>
###Update highlights belonging to a video
<hr>
<pre><code>PUT - https://api.zype.com/videos/{id}/highlights/{id}
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | String id of the Highlight to be updated. Example: 5389352e69702d401b000000. | String
video_id  | String id of the Video to which the highlight belongs. Example: 5389352e69702d401b000000. | String
highlight | A set of key value pairs that describe the highlight. Example: highlight[description]=description. | Hash
description | The description for the video highlight | String
start | The point in the video where the highlight begins | Integer
end | The point in the video where the highlight ends | Integer

#### Request
Content-Type: application/json

#### Response
201
Content-Type: application/json
<pre><code>{
  "response": [
    {"_id": "54c6cbe56368726454050000",
    "description": "Sample Description",
    "end": 411,
    "start": 380
    }
  ]
}
</code></pre>

<hr>
###Associate Zobjects with a Video
<hr>
<pre><code>PUT - https://api.zype.com/videos/{id}/add_zobjects&zobject_id=[id00001, id00002]
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | String id of the Video. Example: 5389352e69702d401b000000. | String
zobject_id | An array containing all of the zobject id's that you want to add to the video. | Array of Strings

#### Request
Content-Type: application/json

#### Response
200
Content-Type: application/json
<pre><code>{
  "response": {
    "_id": "549dc599636872c09d1a0000",
    "active": false,
    "country": nil,
    "created_at": "2014-12-26T15:31:22.121-05:00",
    "data_sources":
    [
      {"_id": "549dc59a636872c09d1b0000",
      "active": true,
      "duration": 493,
      "status": "ready",
      "youtube_id": "J7f26d-AIrM",
      "thumbnails":
        [
          {"_id": "549dc594636872c09d150000",
          "aspect_ratio": nil,
          "height": 90,
          "name": nil,
          "url": "https://i.ytimg.com/vi/J7f26d-AIrM/default.jpg",
          "width": 120},
          {"_id": "549dc594636872c09d160000",
          "aspect_ratio": nil,
          "height": 180,
          "name": nil,
          "url": "https://i.ytimg.com/vi/J7f26d-AIrM/mqdefault.jpg",
          "width": 320},
          {"_id": "549dc594636872c09d170000",
          "aspect_ratio": nil,
          "height": 360,
          "name": nil,
          "url": "https://i.ytimg.com/vi/J7f26d-AIrM/hqdefault.jpg",
          "width": 480},
          {"_id": "549dc594636872c09d180000",
          "aspect_ratio": nil,
          "height": 480,
          "name": nil,
          "url": "https://i.ytimg.com/vi/J7f26d-AIrM/sddefault.jpg",
          "width": 640},
          {"_id": "549dc594636872c09d190000",
          "aspect_ratio": nil,
          "height": 720,
          "name": nil,
          "url": "https://i.ytimg.com/vi/J7f26d-AIrM/maxresdefault.jpg",
          "width": 1280}
        ]
      }
    ],
    "description": "Conan brings the magic of the blues to Chicago's youngest, and most adorable generation.",
    "duration": 493,
    "episode": nil,
    "featured": false,
    "foreign_id": nil,
    "keywords": [],
    "mature_content": false,
    "published_at": nil,
    "rating": 0.0,
    "related_playlist_ids": [],
    "request_count": 0,
    "season": nil,
    "site_id": "549dc583636872c09d110000",
    "status": "created",
    "subscription_required": false,
    "title": "Conan Writes Chicago Blues Songs With School Kids - CONAN on TBS",
    "updated_at": "2014-12-26T16:20:46.324-05:00",
    "zobject_ids": ["549dc72d636872c09d1f0000"],
    "thumbnails":
    [
      {"aspect_ratio": nil, "height": 90, "name": nil, "url": "https://i.ytimg.com/vi/J7f26d-AIrM/default.jpg", "width": 120},
      {"aspect_ratio": nil, "height": 180, "name": nil, "url": "https://i.ytimg.com/vi/J7f26d-AIrM/mqdefault.jpg", "width": 320},
      {"aspect_ratio": nil, "height": 360, "name": nil, "url": "https://i.ytimg.com/vi/J7f26d-AIrM/hqdefault.jpg", "width": 480},
      {"aspect_ratio": nil, "height": 480, "name": nil, "url": "https://i.ytimg.com/vi/J7f26d-AIrM/sddefault.jpg", "width": 640},
      {"aspect_ratio": nil, "height": 720, "name": nil, "url": "https://i.ytimg.com/vi/J7f26d-AIrM/maxresdefault.jpg", "width": 1280}
    ]
  }
}
</code></pre>

<hr>
###Remove Associated Zobjects from a Video
<hr>
<pre><code>PUT - https://api.zype.com/videos/{id}/remove_zobjects&zobject_id=[id00001, id00002]
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | String id of the Video. Example: 5389352e69702d401b000000. | String
zobject_id | An array containing all of the zobject id's that you want to dissociate from the video. | Array of Strings

#### Request
Content-Type: application/json

#### Response
200
Content-Type: application/json

<pre><code>{
  "response": {
    "_id": "549dc599636872c09d1a0000",
    "active": false,
    "country": nil,
    "created_at": "2014-12-26T15:31:22.121-05:00",
    "data_sources":
      [
        {"_id": "549dc59a636872c09d1b0000",
        "active": true,
        "duration": 493,
        "status": "ready",
        "youtube_id": "J7f26d-AIrM",
        "thumbnails":
          [
            {"_id": "549dc594636872c09d150000",
            "aspect_ratio": nil,
            "height": 90,
            "name": nil,
            "url": "https://i.ytimg.com/vi/J7f26d-AIrM/default.jpg",
            "width": 120},
            {"_id": "549dc594636872c09d160000",
            "aspect_ratio": nil,
            "height": 180,
            "name": nil,
            "url": "https://i.ytimg.com/vi/J7f26d-AIrM/mqdefault.jpg",
            "width": 320},
            {"_id": "549dc594636872c09d170000",
            "aspect_ratio": nil,
            "height": 360,
            "name": nil,
            "url": "https://i.ytimg.com/vi/J7f26d-AIrM/hqdefault.jpg",
            "width": 480},
            {"_id": "549dc594636872c09d180000",
            "aspect_ratio": nil,
            "height": 480,
            "name": nil,
            "url": "https://i.ytimg.com/vi/J7f26d-AIrM/sddefault.jpg",
            "width": 640},
            {"_id": "549dc594636872c09d190000",
            "aspect_ratio": nil,
            "height": 720,
            "name": nil,
            "url": "https://i.ytimg.com/vi/J7f26d-AIrM/maxresdefault.jpg",
            "width": 1280}
          ]
        }
      ],
    "description": "Conan brings the magic of the blues to Chicago's youngest, and most adorable generation.",
    "duration": 493,
    "episode": nil,
    "featured": false,
    "foreign_id": nil,
    "keywords": [],
    "mature_content": false,
    "published_at": nil,
    "rating": 0.0,
    "related_playlist_ids": [],
    "request_count": 0,
    "season": nil,
    "site_id": "549dc583636872c09d110000",
    "status": "created",
    "subscription_required": false,
    "title": "Conan Writes Chicago Blues Songs With School Kids - CONAN on TBS",
    "updated_at": "2014-12-26T16:20:46.324-05:00",
    "zobject_ids": [],
  "thumbnails":
  [
    {"aspect_ratio": nil, "height": 90, "name": nil, "url": "https://i.ytimg.com/vi/J7f26d-AIrM/default.jpg", "width": 120},
    {"aspect_ratio": nil, "height": 180, "name": nil, "url": "https://i.ytimg.com/vi/J7f26d-AIrM/mqdefault.jpg", "width": 320},
    {"aspect_ratio": nil, "height": 360, "name": nil, "url": "https://i.ytimg.com/vi/J7f26d-AIrM/hqdefault.jpg", "width": 480},
    {"aspect_ratio": nil, "height": 480, "name": nil, "url": "https://i.ytimg.com/vi/J7f26d-AIrM/sddefault.jpg", "width": 640},
    {"aspect_ratio": nil, "height": 720, "name": nil, "url": "https://i.ytimg.com/vi/J7f26d-AIrM/maxresdefault.jpg", "width": 1280}
    ]
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
  "response":
  {
    "body": "<div style=\"position: relative; padding-bottom: 56.25%; padding-top: 0; height: 0; overflow: hidden;\">\n<iframe id=\"_video_546529b669702d534fb00000\" type=\"text/html\" src=\"https://www.youtube.com/embed/Kno4FTxWycI?autoplay=false&showinfo=0&modestbranding=1\" frameborder=\"0\" style=\"position: absolute; top: 0; left: 0; width: 100%; height: 100%;\"></iframe>\n</div>\n",
    "device": {
      "_id": "5429b1c569702d2f7c080000",
      "description": "Accessed via desktop HTML5 web browser",
      "name": "Desktop"
    },
    "revenue_model": {
      "_id": "5429b1c269702d2f7c010000",
      "description": "Advertising Video On Demand",
      "name": "AVOD"
    },
    "player": {
      "_id": "5429b1cb69702d2f7c1d0000",
      "name": "Youtube Player"
    },
    "provider": {
      "_id": "5429b1cb69702d2f7c1a0000",
      "name": "Youtube"
    },
    "user_agent": {
      "_id": "547e0d6569702d1bfaa00a00",
      "user_agent": "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_9_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/39.0.2171.71 Safari/537.36"
    }
  }
}
</code></pre>
