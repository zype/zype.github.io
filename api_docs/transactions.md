---
layout: api
title: Zype Developer Portal | Transactions
permalink: /api_docs/transactions/
---

## Transactions Collection
Lists all Transactions.
<hr>
### List all Transactions
<hr>
<pre><code>GET - https://api.zype.com/transactions/?page=page&per_page=per_page
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
page      | The page number of records to return (zero indexed). Example: 0. | Number
per_page  | The number of records to return. Example: 10. | Number
q         | A query string for searching for transactions | String
id        | Query for a transaction by id | String
id!       | Exclude a transaction from the query | String
consumer_id        | Query for a transaction by Consumer ID | String

#### Response
200
Content-Type: application/json


<pre><code>{
  "response": [
    {
    "_id": "56de07fbf28347a322000010",
    "_keywords": [
      "example",
      "test"
    ],
      "amount": "4.99",
      "braintree_id": "5fqzgc",
      "consumer_id": "56de07e0f28347a32200000e",
      "created_at": "2016-03-07T18:00:11.069-05:00",
      "currency": "USD",
      "deleted_at": null,
      "description": "",
      "expires_at": null,
      "pass_plan_id": null,
      "payment_nonce": "b74d90f6-4eb9-49b7-ab33-cdb350992d52",
      "playlist_id": null,
      "site_id": "5468fd6569702d17ee500000",
      "status": "authorized",
      "transaction_type": "purchase",
      "updated_at": "2016-03-07T18:00:11.069-05:00",
      "video_id": "553297a769702d081dca96b2"
    },
  ],
  "pagination": {
    current: 2,
    previous: 1,
    next: 3,
    per_page: 10,
    pages: 1
  }
}
</code></pre>

<hr>
### Create a Transaction
<hr>
<pre><code>POST - https://api.zype.com/transactions/{transaction}
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
provider | Value must be either 'stripe' or 'braintree'. Specifies whether you are using Stripe or Braintree for payments. *required* | String
transaction | A set of key value pairs that describe the Transaction. *required* | Hash
consumer_id | The id of the consumer making the transaction. *required* | String
video_id | The id of the video the user is purchasing if purchasing a video. Required if the transaction is for a video. | String
playlist_id | The id of the playlist the user is purchasing if purchasing a playlist. Required if the transaction is for a playlist. | String
pass_plan_id | The id of the pass plan the user is purchasing if purchasing a pass plan. Required if the transaction is for a pass plan. | String
payment_nonce | The payment nonce provided by Stripe or Braintree if using one of those platforms. *required* | String
amount | Must be formatted as a string included cent value, for example "1.99". *required* | String
transaction_type | Must be either 'purchase' or 'rental'. *required* | String
currency | Set currency type. This is optional. Default value is 'USD'. | String
description | Description of transaction. | String

### Example

<pre><code>{
  "api_key": "YOUR_ADMIN_KEY",
  "transaction": {
    "consumer_id": "56fecbf1f28347637b000020",
    "video_id": "56fbe4b5f28347c9f4000ae3",
    "transaction_type": "purchase",
    "amount": "4.99",
    "payment_nonce": "YOUR_PAYMENT_NONCE"
  },
  "provider": "braintree"
}
</code></pre>


#### Response
201
Content-Type: application/json

<pre><code>{
  "response": {
    "_id": "5706b865f283477023000065",
    "_keywords": [
      "example",
      "video"
    ],
    "amount": "4.99",
    "braintree_id": "b5wkgx",
    "consumer_id": "56fecbf1f28347637b000020",
    "created_at": "2016-04-07T15:43:33.617-04:00",
    "currency": "USD",
    "deleted_at": null,
    "description": null,
    "expires_at": null,
    "pass_plan_id": null,
    "payment_nonce": "fake-valid-nonce",
    "playlist_id": null,
    "site_id": "5468fd6569702d17ee500000",
    "status": "authorized",
    "transaction_type": "purchase",
    "updated_at": "2016-04-07T15:43:33.617-04:00",
    "video_id": "56fbe4b5f28347c9f4000ae3"
  }
}
</code></pre>

## Transaction
Lists descriptive information about a Transaction
<hr>
###Retrieve a Transaction
<hr>
<pre><code>GET - https://api.zype.com/transactions/{id}
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | String id of the Transaction to retrieve. Example: 5389352e69702d401b000000. | String

#### Request
Content-Type: application/json

#### Response
200
Content-Type: application/json

<pre><code>{
  "response": {
    "_id": "5706b865f283477023000065",
    "_keywords": [
      "example",
      "video"
    ],
    "amount": "4.99",
    "braintree_id": "b5wkgx",
    "consumer_id": "56fecbf1f28347637b000020",
    "created_at": "2016-04-07T15:43:33.617-04:00",
    "currency": "USD",
    "deleted_at": null,
    "description": null,
    "expires_at": null,
    "pass_plan_id": null,
    "payment_nonce": "fake-valid-nonce",
    "playlist_id": null,
    "site_id": "5468fd6569702d17ee500000",
    "status": "authorized",
    "transaction_type": "purchase",
    "updated_at": "2016-04-07T15:43:33.617-04:00",
    "video_id": "56fbe4b5f28347c9f4000ae3"
  }
}
</code></pre>

<hr>
### Update a Transaction
<hr>
<pre><code>PUT - https://api.zype.com/transactions/{id}
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
transaction | A set of key value pairs that describe the Transaction. *required* | Hash
consumer_id | The id of the consumer. | String
video_id | The id of the video. | String
playlist_id | The id of the playlist. | String
pass_plan_id | The id of the pass plan. | String
payment_nonce | The payment nonce. | String
amount | Must be formatted as a string included cent value, for example "1.99".| String
transaction_type | Must be either 'purchase' or 'rental'. | String
currency | The currency type. | String
description | Description of transaction. | String


#### Request

Content-Type: application/json

#### Response
201
Content-Type: application/json

<pre><code>{
  "response": {
    "_id": "5706b865f283477023000065",
    "_keywords": [
      "asdfasfds",
      "com",
      "lkjalskjdflkajs"
    ],
    "amount": "4.99",
    "braintree_id": "b5wkgx",
    "consumer_id": "56fecbf1f28347637b000020",
    "created_at": "2016-04-07T15:43:33.617-04:00",
    "currency": "USD",
    "deleted_at": null,
    "description": "My cool transaction",
    "expires_at": null,
    "pass_plan_id": null,
    "payment_nonce": "fake-valid-nonced",
    "playlist_id": null,
    "site_id": "5468fd6569702d17ee500000",
    "status": "authorized",
    "transaction_type": "purchase",
    "updated_at": "2016-04-07T15:51:17.275-04:00",
    "video_id": "56fbe4b5f28347c9f4000ae3"
  }
}
</code></pre>

<hr>
### Remove a Transaction
<hr>
<pre><code>DELETE - https://api.zype.com/transactions/{id}
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | String id of the Transaction to remove. Example: 5389352e69702d401b000000. | String

#### Request
Content-Type: application/json

#### Response
204

