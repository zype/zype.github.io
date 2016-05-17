---
layout: api
title: Zype Developer Portal | Redemption Codes
permalink: /api_docs/redemption_codes/
---

## Redemption Codes
<hr>
### List Redemption Codes
<pre><code><b>GET</b> https://api.zype.com/redemption_codes
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
api_key      | The Admin api key for the account. *required* | String
code        | Query for record by code | String
created_at | Filter the records returned by created date. You can use greater than or less than filters by adding a suffix: '.gt', '.gte', '.lt', 'lte'. Example: created_at.gte=2015-01-01 | Date
expiration_date | Filter the records returned by expiration date. You can use greater than or less than filters by adding a suffix: '.gt', '.gte', '.lt', 'lte'. Example: expiration_date.gte=2015-01-01 | Date
id        | Filter records by ID | String
id!       | Exclude records by ID | String
page | The page number of records to return (Example: 1) | Integer
pass_plan_id        | Filter records by a pass plan ID | String
per_page | The number of records to return (Example: 10) | Integer
plan_id        | Filter records by a plan ID | String
playlist_id        | Filter records by a playlist ID | String
q         | Filter records by keyword | String
redeemed_at | Filter the records returned by redeemed at date. You can use greater than or less than filters by adding a suffix: '.gt', '.gte', '.lt', 'lte'. Example: redeemed_at.gte=2015-01-01 | Date
transaction_id        | Filter records by a transaction ID | String
updated_at | Filter the records returned by updated date. You can use greater than or less than filters by adding a suffix: '.gt', '.gte', '.lt', 'lte'. Example: updated_at.gte=2015-01-01 | Date
video_id        | Filter records by a video ID | String

### Create a Redemption Code
<pre><code><b>POST</b> https://api.zype.com/redemption_codes/[redemption_code]
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
api_key      | The Admin api key for the account. *required* | String
redemption_code[code] | Use this param to specify your own code. If no code is sent, one will automatically be generated. | String
redemption_code[expiration_date] | Expiration date for the redemption code. Example: 2017-01-15 | Date
redemption_code[video_id] | The id of the video that the user will be entitled to upon redeeming the code. Required if the redemption code is for a video. | String
redemption_code[playlist_id] | The id of the playlist that the user will be entitled to upon redeeming the code. Required if the redemption code is for a playlist. | String
redemption_code[plan_id] | The id of the subscription plan that the user will be subscribed to upon redeeming the code. Required if the redemption code is for a subscription. | String
redemption_code[pass_plan_id] | The id of the pass plan that the user will have access to upon redeeming the code. Required if the redemption code is for a pass plan. | String

Note: A video_id, playlist_id, plan_id, *OR* a pass_plan_id is required.

### Bulk Create Redemption Codes
<pre><code><b>POST</b> https://api.zype.com/redemption_codes/bulk_create/[redemption_codes]
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
api_key      | The Admin api key for the account. *required* | String
amount      | The number of codes to create. *required* | Integer
redemption_codes[expiration_date] | Expiration date for the redemption code. Example: 2017-01-15 | Date
redemption_codes[video_id] | The id of the video that the user will be entitled to upon redeeming the code. Required if the redemption codes are for a video. | String
redemption_codes[playlist_id] | The id of the playlist that the user will be entitled to upon redeeming the code. Required if the redemption codes are for a playlist. | String
redemption_codes[plan_id] | The id of the subscription plan that the user will be subscribed to upon redeeming the code. Required if the redemption codes are for a subscription. | String
redemption_codes[pass_plan_id] | The id of the pass plan that the user will have access to upon redeeming the code. Required if the redemption codes are for a pass plan. | String

Note: A video_id, playlist_id, plan_id, *OR* a pass_plan_id is required.

## Redemption Code
Lists descriptive information about a Redemption Code

### Retrieve a Redemption Code
<pre><code><b>GET</b> https://api.zype.com/redemption_codes/[id]
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | String id of the Redemption Code to retrieve. Example: 570fc5ddf283471ac300000a. *required* | String
api_key      | The Admin api key for the account. *required* | String

### Update a Redemption Code
<pre><code><b>PUT</b> https://api.zype.com/redemption_codes/[id]
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
api_key      | The Admin api key for the account. *required* | String
redemption_code[code] | Use this param to specify your own code. If no code is sent, one will automatically be generated. | String
redemption_code[expiration_date] | Expiration date for the redemption code. Example: 2017-01-15 | Date
redemption_code[video_id] | The id of the video that the user will be entitled to upon redeeming the code. Required if the redemption code is for a video. | String
redemption_code[playlist_id] | The id of the playlist that the user will be entitled to upon redeeming the code. Required if the redemption code is for a playlist. | String
redemption_code[plan_id] | The id of the subscription plan that the user will be subscribed to upon redeeming the code. Required if the redemption code is for a subscription. | String
redemption_code[pass_plan_id] | The id of the pass plan that the user will have access to upon redeeming the code. Required if the redemption code is for a pass plan. | String

### Remove a Redemption Code
<pre><code><b>DELETE</b> https://api.zype.com/redemption_codes/[id]
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | String id of the Redemption Code to remove. Example: 5389352e69702d401b000000. *required* | String
api_key      | The Admin api key for the account. *required* | String

### Redeem a Redemption Code
<pre><code><b>POST</b> https://api.zype.com/redemption_codes/redeem
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
access_token      | The access token of the authorized consumer. A consumer must have a valid access token to redeem a code. For more information on how to create an access token for a consumer, see the <a href="/api_docs/oauth/">OAuth documentation</a>. *required* | String
code      | The code string for the redemption code. *required* | String

### Redemption Code Object

<pre>
  {
    "response": {
      "_id": "57165ffff283475d1e000002",
      "code": "RQMJQJB5JX5V6JQ5",
      "content_title": "Spaceballs 2: The Search For More Money",
      "content_type": "video",
      "created_at": "2016-04-19T12:42:39.369-04:00",
      "expiration_date": null,
      "pass_plan_id": null,
      "plan_id": null,
      "playlist_id": null,
      "redeemed_at": null,
      "site_id": "5468fd6569702d17ee500000",
      "transaction_id": null,
      "updated_at": "2016-04-19T12:42:39.369-04:00",
      "video_id": "570dabc8f28347ccfc02e939",
      "nice_code": "RQMJ-QJB5-JX5V-6JQ5",
      "available": true,
      "redeemed": false,
      "expired": false,
      "as_qr_code_html_l": "...",
      "as_qr_code_html_b": "..."
    }
  }
</pre>

