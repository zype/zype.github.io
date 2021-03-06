---
layout: api
title: Zype Developer Portal | Consumers
permalink: /api_docs/consumers/
redirect_to: https://docs.zype.com/reference#consumers
---

## Consumers
<hr />
### List Consumers
<pre>
<b>GET</b> https://api.zype.com/consumers
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
braintree_id | Filter records by Braintree ID | String
created_at, current_sign_in_at, last_sign_in_at | Filter records by date field using times in ISO8601 format (Example: 2017-01-01T00:00:00-00:00) or Unix timestamps (Example: 1483228800) <br />**Note**: Range filters can be applied by adding a suffix: '.gt', '.gte', '.lt', 'lte' (Example: created_at.gte) | Date
last_sign_in_ip, current_sign_in_ip | Filter records by IP address | String
email     | Filter records by email | String
id        | Filter records by ID | String
id!       | Exclude records by ID | String
page      | The page number of records to return (Example: 1) | Integer
pass_count| The number of passes that have been purchased or redeemed by the consumer. | Integer
password_token | The password token to use during reset password workflows. Filterable. | String
per_page  | The number of records to return (Example: 10) | Integer
playlist_count | The number of playlists a consumer is entitled to watch via purchase or pass plan.| Integer
q         | Filter records by keyword | String
remember_token | The password token to use during remember login workflows. Filterable. | String
rss_token | Filter records by RSS token | String
stripe_id | Filter records by Stripe ID | String
sign_in_count | Filter records by sign in count <br />**Note**: Range filters can be applied by adding a suffix: ‘.gt’, ‘.gte’, ‘.lt’, ‘lte’ (Example: sign_in_count.gte) | Integer
terms | Boolean field to store if the consumer has agreed to terms and conditions | Boolean
updates | Boolean field to store if the consumer has agreed to receive updates | Boolean
video_count | The number of videos a user is entitled to watch via purchase or pass plan. | Integer

### Create a Consumer
<pre><b>POST</b> https://api.zype.com/consumers
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
consumer[email] | The consumer's email address (must be unique) | String
consumer[password] | The password for the consumer. The password is used for consumer authentication | String
consumer[name] | The name of the consumer | String
consumer[sex] | The gender of the consumer | String
consumer[birthday] | The birthday of the consumer, | String
consumer[updates] | Boolean field to store if the consumer has agreed to receive updates | Boolean
consumer[terms] | Boolean field to store if the consumer has agreed to terms and conditions | Boolean
consumer[password_token] | The password token to use during password reset workflows | String
consumer[remember_token] | The password token to use during remember login workflows | String
consumer[super_watcher] | Boolean field to indicate that a consumer is exempt from content rules | String

### Retrieve a Consumer
<pre><b>GET</b> https://api.zype.com/consumers/[id]
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | ID of the record (Example: 5389352e69702d401b000000) | String

### Update a Consumer
<pre><b>PUT</b> https://api.zype.com/consumers/[id]</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id | ID of the record to update (Example: 540731274c616e047a000000) | String
consumer[email] | The consumer's email address (must be unique) | String
consumer[password] | The password for the consumer. The password is used for consumer authentication | String
consumer[name] | The name of the consumer | String
consumer[sex] | The gender of the consumer | String
consumer[birthday] | The birthday of the consumer, | String
consumer[updates] | Boolean field to store if the consumer has agreed to receive updates | Boolean
consumer[terms] | Boolean field to store if the consumer has agreed to terms and conditions | Boolean
consumer[password_token] | The password token to use during password reset workflows | String
consumer[remember_token] | The password token to use during remember login workflows | String
consumer[super_watcher] | Boolean field to indicate that a consumer is exempt from content rules | String

### Delete a Consumer
<pre><b>DELETE</b> https://api.zype.com/consumers/[id]
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id | ID of the record to be deleted. Example: 540731274c616e047a000000 | String

### Consumer Object

<pre>
{
  "_id": "54579a634c616e0389000000",
  "_keywords": [
    "com",
    "example",
    "test123"
  ],
  "created_at": "2014-11-03T15:08:19.675Z",
  "deleted_at": null,
  "email": "test123@example.com",
  "site_id": "53e8d7f869702d5b64010000",
  "stripe_id": "cus_54wKapCMCaqd9b1235",
  "subscription_count": 1,
  "subscription_ids": ["5aa92bf7248f1c3e6e000000"],
  "subscription_plans": [
    {
      "id":"5aa92602248f1c3fc8000000",
      "name":"Silver Plan",
      "entitlement_type":"tiered",
      "subscription_id":"5aa92bf7248f1c3e6e000000"
    }
  ]
  "updated_at": "2014-11-03T15:08:19.675Z"
}
</pre>
