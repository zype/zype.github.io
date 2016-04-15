---
layout: api
title: Zype Developer Portal | Consumers
permalink: /api_docs/consumers/
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
page      | The page number of records to return (zero indexed). Example: 0. | Number
per_page  | The number of records to return. Example: 10. | Number
q         | A query string for searching for consumers | String
id        | Query for a consumer by id | String
id!       | Exclude a consumer from the query | String
email     | Filter consumers by email | String
rss_token | Filter consumers by RSS token | String
password_token | Filter consumers by password reset token | String
stripe_id | Filter consumers by Stripe ID | String
braintree_id | Filter consumers by Braintree ID | String
created_at | Filter the records returned by created date. You can use greater than or less than filters by adding a suffix: '.gt', '.gte', '.lt', 'lte'. Example: created_at.gte=2015-01-01 | Date

###Retrieve a Consumer
<hr>
<pre><b>GET</b> https://api.zype.com/consumers/[id]
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | ID of the consumer. Example: 5389352e69702d401b000000. | String

###Create a Consumer
<hr>
<pre><b>POST</b> https://api.zype.com/consumers
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
consumer[email] | The consumer's email address. (must be unique) | String
consumer[password] | The password for the consumer. The password is used for consumer authentication. | String
consumer[name] | The name of the consumer. | String
consumer[sex] | The gender of the consumer. | String
consumer[birthday] | The birthday of the consumer, | String
consumer[updates] | Boolean field to store if the consumer has agreed to receive updates. | Boolean
consumer[terms] | Boolean field to store if the consumer has agreed to terms and conditions. | Boolean

###Update a Consumer
<hr>
<pre><b>PUT</b> https://api.zype.com/consumers/[id]</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id | ID of the consumer to update. Example: 540731274c616e047a000000. | String
consumer[email] | The consumer's email address. (must be unique) | String
consumer[password] | The password for the consumer. The password is used for consumer authentication. | String
consumer[name] | The name of the consumer. | String
consumer[sex] | The gender of the consumer. | String
consumer[birthday] | The birthday of the consumer, | String
consumer[updates] | Boolean field to store if the consumer has agreed to receive updates. | Boolean
consumer[terms] | Boolean field to store if the consumer has agreed to terms and conditions. | Boolean
consumer[password_token] | The password token to use during password reset workflows. | String
consumer[remember_token] | The password token to use during remember login workflows. | String

###Delete a Consumer
<hr>
<pre><b>DELETE</b> https://api.zype.com/consumers/[id]
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id | ID of the consumer to be deleted. Example: 540731274c616e047a000000. | String

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
  "updated_at": "2014-11-03T15:08:19.675Z"
}
</pre>