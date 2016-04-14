---
layout: api
title: Zype Developer Portal | Redemption Codes
permalink: /api_docs/redemption_codes/
---

## Redemption Codes Collection
Lists all Redemption Codes.
<hr>
### List all Redemption Codes
<hr>
<pre><code>GET - https://api.zype.com/redemption_codes/?page=page&per_page=per_page
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
api_key      | The Admin api key for the account. *required* | String
page      | The page number of records to return (zero indexed). Example: 0. | Number
per_page  | The number of records to return. Example: 10. | Number
id        | Query for a redemption code by id | String
id!       | Exclude a redemption code from the query | String
code        | Query for a redemption code by code | String
video_id        | Query for a redemption code by video id string | String
playlist_id        | Query for a redemption code by playlist id string | String
plan_id        | Query for a redemption code by plan id string | String
pass_plan_id        | Query for a redemption code by pass plan id string | String
transaction_id        | Query for a redemption code by transaction id string | String
transaction_id        | Query for a redemption code by transaction id string | String
created_at | Filter the records returned by created date. You can use greater than or less than filters by adding a suffix: '.gt', '.gte', '.lt', 'lte'. Example: created_at.gte=2015-01-01 | Date
updated_at | Filter the records returned by updated date. You can use greater than or less than filters by adding a suffix: '.gt', '.gte', '.lt', 'lte'. Example: updated_at.gte=2015-01-01 | Date
expiration_date | Filter the records returned by expiration date. You can use greater than or less than filters by adding a suffix: '.gt', '.gte', '.lt', 'lte'. Example: expiration_date.gte=2015-01-01 | Date
redeemed_at | Filter the records returned by redeemed at date. You can use greater than or less than filters by adding a suffix: '.gt', '.gte', '.lt', 'lte'. Example: redeemed_at.gte=2015-01-01 | Date

#### Response
200
Content-Type: application/json


<pre><code>{
  "response": [
    {
      "_id": "570d5704f28347c1fd000000",
      "code": "123456",
      "created_at": "2016-04-12T16:14:21.015-04:00",
      "expiration_date": null,
      "pass_plan_id": null,
      "plan_id": null,
      "playlist_id": null,
      "redeemed_at": null,
      "site_id": "5468fd6569702d17ee500000",
      "transaction_id": null,
      "updated_at": "2016-04-12T16:14:21.015-04:00",
      "video_id": "5708044df2834741870000e1",
      "nice_code": "123-456",
      "available?": true,
      "redeemed?": false,
      "expired?": false,
      "unassigned?": false
    }
  ],
  "pagination": {
    "current": 1,
    "previous": null,
    "next": null,
    "per_page": 25,
    "pages": 1
  }
}

</code></pre>

<hr>
### Create a Redemption Code
<hr>
<pre><code>POST - https://api.zype.com/redemption_codes/{redemption code}
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
api_key      | The Admin api key for the account. *required* | String
redemption code | A set of key value pairs that describe the Redemption Code. *required* | Hash
code | Use this param to specify your own code. If no code is sent, one will automatically be generated. | String
expiration_date | Expiration date for the redemption code. Example: 2017-01-15 | Date
video_id | The id of the video that the user will be entitled to upon redeeming the code. Required if the redemption code is for a video. | String
playlist_id | The id of the playlist that the user will be entitled to upon redeeming the code. Required if the redemption code is for a playlist. | String
plan_id | The id of the subscription plan that the user will be subscribed to upon redeeming the code. Required if the redemption code is for a subscription. | String
pass_plan_id | The id of the pass plan that the user will have access to upon redeeming the code. Required if the redemption code is for a pass plan. | String

### Example

<pre><code>
{
  "api_key": "YOUR_ADMIN_KEY",
  "redemption_code": {
    "expiration_date": "2017-02-20",
    "video_id": "570fb456f283471ac3000007"
  }
}
</code></pre>


#### Response
201
Content-Type: application/json

<pre><code>
{
  "response": {
    "_id": "570fc5ddf283471ac300000a",
    "code": "123456",
    "created_at": "2016-04-14T12:31:25.271-04:00",
    "expiration_date": "2017-02-20T00:00:00.000-05:00",
    "pass_plan_id": null,
    "plan_id": null,
    "playlist_id": null,
    "redeemed_at": null,
    "site_id": "5468fd6569702d17ee500000",
    "transaction_id": null,
    "updated_at": "2016-04-14T12:31:25.271-04:00",
    "video_id": "570fb456f283471ac3000007",
    "nice_code": "123-456",
    "available?": true,
    "redeemed?": false,
    "expired?": false,
    "unassigned?": false
  }
}
</code></pre>

## Redemption Code
Lists descriptive information about a Redemption Code
<hr>
###Retrieve a Redemption Code
<hr>
<pre><code>GET - https://api.zype.com/redemption_codes/{id}
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | String id of the Redemption Code to retrieve. Example: 570fc5ddf283471ac300000a. *required* | String
api_key      | The Admin api key for the account. *required* | String

#### Request
Content-Type: application/json

#### Response
200
Content-Type: application/json

<pre><code>
{
  "response": {
    "_id": "570fc5ddf283471ac300000a",
    "code": "123456",
    "created_at": "2016-04-14T12:31:25.271-04:00",
    "expiration_date": "2017-02-20T00:00:00.000-05:00",
    "pass_plan_id": null,
    "plan_id": null,
    "playlist_id": null,
    "redeemed_at": null,
    "site_id": "5468fd6569702d17ee500000",
    "transaction_id": null,
    "updated_at": "2016-04-14T12:31:25.271-04:00",
    "video_id": "570fb456f283471ac3000007",
    "nice_code": "123-456",
    "available?": true,
    "redeemed?": false,
    "expired?": false,
    "unassigned?": false
  }
}
</code></pre>

<hr>
### Update a Redemption Code
<hr>
<pre><code>PUT - https://api.zype.com/redemption_codes/{id}
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
api_key      | The Admin api key for the account. *required* | String
redemption code | A set of key value pairs that describe the Redemption Code. *required* | Hash
code | Use this param to specify your own code. If no code is sent, one will automatically be generated. | String
expiration_date | Expiration date for the redemption code. Example: 2017-01-15 | Date
video_id | The id of the video that the user will be entitled to upon redeeming the code. Required if the redemption code is for a video. | String
playlist_id | The id of the playlist that the user will be entitled to upon redeeming the code. Required if the redemption code is for a playlist. | String
plan_id | The id of the subscription plan that the user will be subscribed to upon redeeming the code. Required if the redemption code is for a subscription. | String
pass_plan_id | The id of the pass plan that the user will have access to upon redeeming the code. Required if the redemption code is for a pass plan. | String


#### Request

Content-Type: application/json

#### Response
201
Content-Type: application/json

<pre><code>
{
  "response": {
    "_id": "570fc5ddf283471ac300000a",
    "code": "123456",
    "created_at": "2016-04-14T12:31:25.271-04:00",
    "expiration_date": "2017-02-21T00:00:00.000-05:00",
    "pass_plan_id": null,
    "plan_id": null,
    "playlist_id": null,
    "redeemed_at": null,
    "site_id": "5468fd6569702d17ee500000",
    "transaction_id": null,
    "updated_at": "2016-04-14T12:33:47.913-04:00",
    "video_id": "570fb456f283471ac3000007",
    "nice_code": "123-456",
    "available?": true,
    "redeemed?": false,
    "expired?": false,
    "unassigned?": false
  }
}
</code></pre>

<hr>
### Remove a Redemption Code
<hr>
<pre><code>DELETE - https://api.zype.com/redemption_codes/{id}
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | String id of the Redemption Code to remove. Example: 5389352e69702d401b000000. *required* | String
api_key      | The Admin api key for the account. *required* | String

#### Request
Content-Type: application/json

#### Response
204

<hr>
### Redeem a Redemption Code
<hr>
<pre><code>POST - https://api.zype.com/redemption_codes/redeem
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
access_token      | The access token of the authorized consumer. A consumer must have a valid access token to redeem a code. For more information on how to create an access token for a consumer, see the <a href="/api_docs/oauth/">OAuth documentation</a>. *required* | String
code      | The code string for the redemption code. *required* | String

#### Request
Content-Type: application/json

#### Success Response
200

