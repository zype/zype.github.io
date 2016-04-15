###List the segments of a Video
<hr>
<pre><b>GET</b> https://api.zype.com/videos/{id}/segments
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | ID of the Video. Example: 5389352e69702d401b000000. | String

#### Request
Content-Type: application/json

#### Response
200
Content-Type: application/json
<pre>{
  "response": [
    {"_id": "54c6cbe56368726454050000",
    "description": "theBest",
    "end": 112,
    "start": 90
    }
  ]
}
</pre>


<hr>  
###Find a specific segment
<hr>
<pre><b>GET</b> https://api.zype.com/videos/{id1}/segments/{id2}
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id1        | ID of the Video to which the segment belongs. Example: 5389352e69702d401b000000. | String
id2        | ID of the segment. Example: 5389352e69702d401b000000. | String

#### Request
Content-Type: application/json

#### Response
200
Content-Type: application/json
<pre>{
  "response": [
    {"_id": "54c6cbe56368726454050000",
    "description": "theBest",
    "end": 112,
    "start": 90
    }
  ]
}
</pre>

<hr>
###Add segments to a Video
<hr>
<pre><b>POST</b> https://api.zype.com/videos/{id}/segments
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
segment | A set of key value pairs that describe the segment. Example: segment[description]=description. | Hash
description | The description for the video segment | String
start | The point in the video where the segment begins | Integer
end | The point in the video where the segment ends | Integer

#### Request
Content-Type: application/json

#### Response
201
Content-Type: application/json
<pre>{
  "response": [
    {"_id": "54c6cbe56368726454050000",
    "description": "Sample Description",
    "end": 411,
    "start": 380
    }
  ]
}
</pre>

<hr>
###Remove segments from a Video
<hr>
<pre><b>DELETE</b> https://api.zype.com/videos/{id1}/segments/{id2}
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id1       | ID of the Video to which the segment belongs. Example: 5389352e69702d401b000000. | String
id2       | ID of the segment to be deleted. Example: 5389352e69702d401b000000. | String


#### Request
Content-Type: application/json

#### Response
204
Content-Type: application/json
<pre>{
  "response": No Content
}
</pre>

<hr>
###Update segments belonging to a video
<hr>
<pre><b>PUT</b> https://api.zype.com/videos/{id1}/segments/{id2}
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id1  | ID of the Video to which the segment belongs. Example: 5389352e69702d401b000000. | String
id2        | ID of the segment to be updated. Example: 5389352e69702d401b000000. | String
segment | A set of key value pairs that describe the segment. Example: segment[description]=description. | Hash
description | The description for the video segment | String
start | The point in the video where the segment begins | Integer
end | The point in the video where the segment ends | Integer

#### Request
Content-Type: application/json

#### Response
201
Content-Type: application/json
<pre>{
  "response": [
    {"_id": "54c6cbe56368726454050000",
    "description": "Sample Description",
    "end": 411,
    "start": 380
    }
  ]
}
</pre>
