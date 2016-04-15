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
braintree_id | Filter records by Braintree ID | String
created_at | Filter the records returned by created date. Greater or less than filters can be used by adding a suffix (Example: created_at.gte) | Date
email     | Filter records by email | String
id        | Filter records by ID | String
id!       | Exclude records by ID | String
page      | The page number of records to return (Example: 1) | Number
password_token | Filter records by password reset token | String
per_page  | The number of records to return (Example: 10) | Number
q         | Filter records by keyword | String
rss_token | Filter records by RSS token | String
stripe_id | Filter records by Stripe ID | String

###Retrieve a Consumer
<pre><b>GET</b> https://api.zype.com/consumers/[id]
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | ID of the record (Example: 5389352e69702d401b000000) | String

###Create a Consumer
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

###Update a Consumer
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

###Delete a Consumer
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
  "updated_at": "2014-11-03T15:08:19.675Z"
}
</pre>