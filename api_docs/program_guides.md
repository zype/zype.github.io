---
layout: api
title: Zype Developer Portal | Program Guides
permalink: /api_docs/program_guides/
---

## Program Guides
<hr />
### List Program Guides
<pre>
<b>GET</b> https://api.zype.com/program_guides
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | Filter records by ID | String
id!       | Exclude records by ID | String
created_at | Filter records by created date using times in ISO8601 format (Example: 2017-01-01T00:00:00-00:00) or Unix timestamps (Example: 1483228800) <br />**Note**: Range filters can be applied by adding a suffix: '.gt', '.gte', '.lt', 'lte' (Example: created_at.gte) | Date
order     | Sort records in ascending or descending order (Example: asc/desc) | String
page | The page number of records to return (Example: 1) | Integer
per_page | The number of records to return (Example: 10) | Integer
q         | Filter records by keyword | String
sort      | Sort records on the specified field | String
title     | Filter records by title | String

### Retrieve a Program Guide
<pre><b>GET</b> https://api.zype.com/program_guides/[id]
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | ID of the record (Example: 5389352e69702d401b000000) | String

### Create a Program Guide
<pre><b>POST</b> https://api.zype.com/program_guides
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
program_guide[name] | Title of the program guide | String
program_guide[url] | Source URL used to sync content for the program guide | String
program_guide[language] | Language used to import content for the program guide | Array
program_guide[time_zone] | Time zone offset for the program guide | Array

### Update a Program Guide
<pre><b>PUT</b> https://api.zype.com/program_guides/[id]</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id | ID of the record to update (Example: 540731274c616e047a000000) | String
program_guide[name] | Title of the program guide | String
program_guide[url] | Source URL used to sync content for the program guide | String
program_guide[language] | Language used to import content for the program guide | Array
program_guide[time_zone] | Time zone offset for the program guide | Array

### Delete a Program Guide
<pre><b>DELETE</b> https://api.zype.com/program_guides/[id]
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id | ID of the record to delete (Example: 540731274c616e047a000000) | String

### List Program Guide Entries
<pre>
<b>GET</b> https://api.zype.com/program_guides/[id]/entries
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | Filter records by ID | String
id!       | Exclude records by ID | String
created_at | Filter records by created date using times in ISO8601 format (Example: 2017-01-01T00:00:00-00:00) or Unix timestamps (Example: 1483228800) <br />**Note**: Range filters can be applied by adding a suffix: '.gt', '.gte', '.lt', 'lte' (Example: created_at.gte) | Date
end_time | Filter records by end time using times in ISO8601 format (Example: 2017-01-01T00:00:00-00:00) or Unix timestamps (Example: 1483228800) <br />**Note**: Range filters can be applied by adding a suffix: '.gt', '.gte', '.lt', 'lte' (Example: end_time.gte) | Date
order     | Sort records in ascending or descending order (Example: asc/desc) | String
page | The page number of records to return (Example: 1) | Integer
per_page | The number of records to return (Example: 10) | Integer
q         | Filter records by keyword | String
sort      | Sort records on the specified field | String
start_time | Filter records by start time using times in ISO8601 format (Example: 2017-01-01T00:00:00-00:00) or Unix timestamps (Example: 1483228800) <br />**Note**: Range filters can be applied by adding a suffix: '.gt', '.gte', '.lt', 'lte' (Example: start_time.gte) | Date
title     | Filter records by title | String

### Program Guide Object

<pre>
{
  "_id": "548f5b8e4c616e8031010000",
  "created_at": "2016-11-10T14:22:33.751-05:00",
  "language": "en",
  "name": "test",
  "program_guide_entry_count": 123,
  "refreshed_at": 2016-11-14T16:06:00.313-05:00,
  "site_id": "545932274c616e2359000000",
  "status": "synced",
  "status_reason": null,
  "time_zone": "Eastern Time (US & Canada)",
  "updated_at": "2016-11-14T16:06:00.314-05:00",
  "url": "http://example.com/epg",
}
</pre>

### Program Guide Entry Object

<pre>
{
  "_id":"5829f9930983881db400077b",
  "category":[
    "action",
    "adventure",
    "sci-fi"
  ],
  "created_at":"2016-11-14T12:51:15.029-05:00",
  "description": "A continuation of the saga created by George Lucas set thirty years after Star Wars: Episode VI - Return of the Jedi (1983).",
  "duration":2580,
  "end_time":"2016-11-29T00:38:00.000-05:00",
  "program_guide_id":"548f5b8e4c616e8031010000",
  "start_time":"2016-11-28T23:55:00.000-05:00",
  "subtitle":null,
  "time_zone":"Eastern Time (US & Canada)",
  "title": "Star Wars: Episode VII - The Force Awakens",
  "updated_at":"2016-11-14T12:51:15.029-05:00",
  "start_time_with_offset":"2016-11-28T20:55:00.000-08:00",
  "end_time_with_offset":"2016-11-28T21:38:00.000-08:00"
}
</pre>