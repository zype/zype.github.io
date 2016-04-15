---
layout: api
title: Zype Developer Portal | Transactions
permalink: /api_docs/transactions/
---

## Transactions Collection
<hr>
### List Transactions
<pre><code>GET - https://api.zype.com/transactions/?page=page&per_page=per_page
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
consumer_id   | Filter records by a Consumer ID | String
id        | Filter records by ID | String
id!       | Exclude records by ID | String
page | The page number of records to return (Example: 1) | Integer
per_page | The number of records to return (Example: 10) | Integer
q         | Filter records by keyword | String

### Create a Transaction
<pre><code>POST - https://api.zype.com/transactions/{transaction}
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
provider | Value must be either 'stripe' or 'braintree'. Specifies whether you are using Stripe or Braintree for payments. *required* | String
transaction[consumer_id] | The id of the consumer making the transaction. *required* | String
transaction[video_id] | The id of the video the user is purchasing if purchasing a video. Required if the transaction is for a video. | String
transaction[playlist_id] | The id of the playlist the user is purchasing if purchasing a playlist. Required if the transaction is for a playlist. | String
transaction[pass_plan_id] | The id of the pass plan the user is purchasing if purchasing a pass plan. Required if the transaction is for a pass plan. | String
transaction[payment_nonce] | The payment nonce provided by Stripe or Braintree if using one of those platforms. *required* | String
amount | Must be formatted as a string included cent value, for example "1.99". *required* | String
transaction[transaction_type] | Must be either 'purchase' or 'rental'. *required* | String
transaction[currency] | Set currency type. This is optional. Default value is 'USD'. | String
description | Description of transaction. | String

###Retrieve a Transaction
<pre><code>GET - https://api.zype.com/transactions/{id}
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | String id of the Transaction to retrieve. Example: 5389352e69702d401b000000. | String

### Update a Transaction
<pre><code>PUT - https://api.zype.com/transactions/{id}
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
transaction[consumer_id] | The id of the consumer. | String
transaction[video_id] | The id of the video. | String
transaction[playlist_id] | The id of the playlist. | String
transaction[pass_plan_id] | The id of the pass plan. | String
transaction[payment_nonce] | The payment nonce. | String
transaction[amount] | Must be formatted as a string included cent value, for example "1.99".| String
transaction[transaction_type] | Must be either 'purchase' or 'rental'. | String
transaction[currency] | The currency type. | String
transaction[description] | Description of transaction. | String

### Delete a Transaction
<pre><code>DELETE - https://api.zype.com/transactions/{id}
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | String id of the Transaction to remove. Example: 5389352e69702d401b000000. | String

### Transaction Object

<pre>
{
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
</pre>
