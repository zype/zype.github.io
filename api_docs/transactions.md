---
layout: api
title: Zype Developer Portal | Transactions
permalink: /api_docs/transactions/
---

## Transactions Collection
<hr>
### List Transactions
<pre><b>GET</b> https://api.zype.com/transactions
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
consumer_id   | Filter records by a consumer ID | String
id        | Filter records by ID | String
id!       | Exclude records by ID | String
page | The page number of records to return (Example: 1) | Integer
per_page | The number of records to return (Example: 10) | Integer
q         | Filter records by keyword | String

### Create a Transaction
<pre><b>POST</b> https://api.zype.com/transactions/[id]
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
provider | Value must be either 'stripe' or 'braintree'. Specifies whether you are using Stripe or Braintree for payments | String
transaction[amount] | Must be formatted as a string included cent value, for example "1.99" | String
transaction[currency] | Set currency type. This is optional. Default value is 'USD' | String
transaction[consumer_id] | The ID of the consumer making the transaction | String
transaction[description] | Description of transaction | String
transaction[pass_plan_id] | The ID of the pass plan the user is purchasing if purchasing a pass plan. Required if the transaction is for a pass plan | String
transaction[payment_nonce] | The payment nonce provided by Stripe or Braintree if using one of those platforms | String
transaction[playlist_id] | The ID of the playlist the user is purchasing if purchasing a playlist. Required if the transaction is for a playlist | String
transaction[transaction_type] | Must be either 'purchase' or 'rental' | String
transaction[video_id] | The ID of the video the user is purchasing if purchasing a video. Required if the transaction is for a video | String

###Retrieve a Transaction
<pre><b>GET</b> https://api.zype.com/transactions/[id]
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | ID of the record to retrieve (Example: 5389352e69702d401b000000) | String

### Update a Transaction
<pre><b>PUT</b> https://api.zype.com/transactions/[id]
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
transaction[consumer_id] | The ID of the consumer | String
transaction[video_id] | The ID of the video | String
transaction[playlist_id] | The ID of the playlist | String
transaction[pass_plan_id] | The ID of the pass plan | String
transaction[payment_nonce] | The payment nonce | String
transaction[amount] | Must be formatted as a string included cent value, for example "1.99".| String
transaction[transaction_type] | Must be either 'purchase' or 'rental' | String
transaction[currency] | The currency type | String
transaction[description] | Description of transaction | String

### Delete a Transaction
<pre><b>DELETE</b> https://api.zype.com/transactions/[id]
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | ID of the record to delete (Example: 5389352e69702d401b000000) | String

### Transaction Object

<pre>
{
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
</pre>