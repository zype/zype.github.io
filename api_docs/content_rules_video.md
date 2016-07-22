---
layout: api
title: Zype Developer Portal | Video Content Rules
permalink: /api_docs/content_rules_video/
---

## Video Content Rules
<hr />
### List Content Rules For Video
<pre>
<b>GET</b> https://api.zype.com/videos/[video_id]/content_rules
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
video_id | Lists content rules for the video (Example: 5389352e69702d401b000001) | String

### Retrieve a Content Rule
<pre><b>GET</b> https://api.zype.com/videos/[video_id]/content_rules/[id]
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | ID of the record (Example: 5389352e69702d401b000000) | String
video_id | Video ID the content rule is associated with (Example: 5389352e69702d401b000001) | String

### Create a Content Rule for a Video
<pre><b>POST</b> https://api.zype.com/videos/[video_id]/content_rules
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
video_id | Video ID the content rule is associated with (Example: 5389352e69702d401b000001) | String
content_rule[name] | The name for the content rule | String
content_rule[priority] | The priority of the content rule. Default *1* | Integer
content_rule[stackable] | The gender of the content rule. Default *true* | Boolean
content_rule[policy] | 'allow' will allow the content to be accessed if the rule matches. ‘deny’ will deny the content from being accessed if the rule matches. Valid policies are "allow" or "deny". Default *"deny"* | String
content_rule[geographies[countries]] | An array of country abbreviation codes. For example ["US", "GB"] | Array

#### Example JSON for POST create

<pre>
  {
    "api_key": "[ADMIN_KEY]",
    "content_rule": {
      "enabled": true,
      "geographies": [
        {
          "countries": [
            "GB"
          ]
        }
      ],
      "name": "My new content rule",
      "policy": "deny",
      "priority": 1,
      "stackable": true
    }
  }
</pre>



### Update a Content Rule
<pre><b>PUT</b> https://api.zype.com/videos/[video_id]/content_rules/[id]</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id | ID of the record to update (Example: 540731274c616e047a000000) | String
video_id | Video ID the content rule is associated with (Example: 5389352e69702d401b000001) | String
content_rule[name] | The name for the content rule | String
content_rule[priority] | The priority of the content rule. Default *1* | Integer
content_rule[stackable] | The gender of the content rule. Default *true* | Boolean
content_rule[policy] | 'allow' will allow the content to be accessed if the rule matches. ‘deny’ will deny the content from being accessed if the rule matches. Valid policies are "allow" or "deny". Default *"deny"* | String
content_rule[geographies[countries]] | An array of country abbreviation codes. For example ["US", "GB"] | Array

### Delete a Content Rule
<pre><b>DELETE</b> https://api.zype.com/videos/[video_id]/content_rules/[id]
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id | ID of the record to be deleted. Example: 540731274c616e047a000000 | String

### Content Rule Object

<pre>
{
  "response": {
    "_id": "577528faf283470887000009",
    "created_at": "2016-06-30T10:13:14.555-04:00",
    "enabled": true,
    "geographies": [
      {
        "_id": "577529daf28347088700000a",
        "countries": [
          "GB"
        ]
      }
    ],
    "name": "My new content rule",
    "policy": "deny",
    "priority": 1,
    "stackable": true,
    "updated_at": "2016-06-30T10:16:58.651-04:00"
  }
}
</pre>
