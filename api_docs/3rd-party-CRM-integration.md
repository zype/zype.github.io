---
layout: api
title:  "3rd Party Payment Provider & Subscription Management Quickstart | Common API Examples"
permalink:  /api_docs/3rd-party-crm-integration/
---

# 3rd Party Payment Provider & Subscription Management Quickstart

What does this solution do?
Zype provides an effective way of importing and managing an external database of consumers within the Zype platform. This is useful if you are using a 3rd party payment processor to sell subscriptions or a 3rd party CRM tool to manage your customer database and would also like to import and track these customers in the Zype platform.
 
Once imported into the Zype platform, benefits include ensuring these customers have access to content across all of your distribution endpoints via Universal login.
 
This workflow involves use of Zype’s Consumer, Subscription, and Linked Devices APIs. This document provides details on how to integrate subscription customers and transactions processed via 3rd party payment processors.


### Prerequisites for Implementation

In order to utilize Zype’s RESTful API service to implement 3rd party payment & subscriber management, you need the following:

* Paid for and current Zype account
* Subscription plans created and configured in the Zype platform
* 3rd party database of consumers whom you’d like to import/consolidate into Zype
* Developer who can work with APIs for integration
* (Optional) 3rd party payment processor

### Steps to Implement Solution

Importing and managing consumers and subscriptions stored in a 3rd party database is easy to do with Zype, typically requiring only three steps:

1. Create a consumer user in your own platform’s database
 
2. Create corresponding Zype consumer user to match to your database consumer
 
3. Create a subscription for the Zype consumer

### Step 1: Create a consumer user in your own platform’s database

Consumers are used to represent users in the Zype platform. Consumer records can be used to store basic user login information, including email, name and password. Consumers can also be used to store subscription information, and if credentials are supplied, process payments and subscriptions from Stripe or Braintree.
 
Creating a consumer user in your database is typically handled prior to transaction processing, during your account sign up or account creation flow. This is not dependent on the Zype platform, but is required for importing or creating a consumer record in the Zype database.

### Step 2: Create the corresponding consumer user in Zype

Once you’ve created a consumer in your database, you should also create a consumer in the Zype platform via our Consumer API. This will ensure that you can track all consumers who are creating accounts via your 3rd party payment processors or CRMs, and that those consumers can have access to any subscription content they purchase directly through you.
 
Consumer objects are generally used in the following ways in the Zype platform:

* To store subscription, transaction, entitlement, and payment information about users.
* To enable linking a device for the user in order to access content on one of your OTT endpoints.
* To optionally provide login capabilities for your platform. Depending on your use case this may not be required, but if you’d like to utilize login capabilities simply provide a password for consumers when they are created.

The minimum required fields to create a user is their email address. You can also supply additional information including the consumer’s name, birthday, or gender by supplying values in the POST request. Although optional, typically all consumer objects include passwords upon creation (to enable login / authentication across your content distribution endpoints).
 
Once you create a consumer in Zype, you’ll want to create a relational record for the consumer between Zype and your own database. We suggest using the Zype consumer ID for this purpose. The consumer ID of a Zype created consumer is returned upon successful creation via API. (example consumer_id value: 54579a634c61450389000000)
 
To create consumers via API, you will need to supply your admin API key in the API request. 

Consumer API Endpoint
POST - https://api.zype.com/consumers/
 
Example Request:
{% highlight xml %} 
curl https://api.zype.com/consumers/  \
   -d api_key="[YOUR ADMIN KEY]" \
   -d consumer[email]="email@example.com" \
   -d consumer[name]="Example User" \
   -d consumer[password]="ExamplePassword"

Example Response:
 
{
  "response": {
    "_id": "54579a634c61450389000000",
    "created_at": "2014-11-03T15:08:19.675Z",
    "deleted_at": null,
    "email": "email@example.com",
    "name": "Example User",
    "site_id": "53e8d7f86970545b64010000",
    "subscription_count": 0,
    "updated_at": "2014-11-03T15:08:19.675Z"
  }
}
{% endhighlight %} 
For a full listed of supported API commands please visit our API documentation: [Zype Consumer API Documentation](http://dev.zype.com/api_docs/consumers/)


### Step 3: Create a subscription for a Zype consumer

Subscriptions are used to track that a consumer has subscribed to content on your platform and should have entitlement to your premium subscription library. There are three types of subscriptions available: Basic, Stripe or Braintree. 
 
Basic subscriptions are used to indicate that a user has subscribed to your content without having a Zype integrated payment provider to process payment. For any subscriptions purchased through your 3rd party payment processor, you’ll create Basic subscriptions via Zype’s Subscription API.

Stripe and Braintree subscriptions require a payment token be provided from the respective provider when creating the subscription. Zype will then process the payment through the respective provider on your behalf.
 
Subscriptions should be created after your users has provided payment details. If you would like to manage payment processing yourself use a “basic” subscription which will only track that a user is subscribed to a plan. Stripe or Braintree subscriptions can be utilized if you have Zype manage subscriptions on your behalf via our embeddable widgets.
 
Once a consumer purchases via your 3rd party payment processor, you’ll want to create a Basic subscription in the Zype platform. After creating the Basic subscription, you should create a relational record between the subscription record in Zype and your own database. We suggest using the Zype subscription ID for this purpose. The subscription ID of a Zype created subscription is returned upon successful creation of the subscription. (example subscription_id: 54579a634c61450389000000)
 
To create subscriptions you will need to supply your admin API key in the API request. You will also need to have a consumer and plan set up in the Zype platform to subscribe to.

Subscription API Endpoint
POST - https://api.zype.com/subscriptions 
 
Example Request:
{% highlight xml %}  
curl https://api.zype.com/subscriptions \
   -d api_key="[YOUR ADMIN KEY]" \
   -d subscription[third_party_id]=[THIRD PARTY ID IN YOUR PLAN]\
   -d subscription[plan_id]="54579a634c61450389000000" \
   -d subscription[consumer_id]="54579a634c61450389000000" \

Example Response:
 
{
  "response": {
    "_id": "54579a634c61450389000000",
    "amount": 5.00,
    "consumer_id": "54579a634c61450389000000",
    "currency": “USD”,
    "created_at": "2014-11-03T15:08:19.675Z",
    "deleted_at": null,
    "interval": "month",
    "interval_count": 1,
    "mrr": 5.00,
    "plan_id": "54579a634c61450389000000",
    "site_id": "53e8d7f86970545b64010000",
    "updated_at": "2014-11-03T15:08:19.675Z"
  }
}
{% endhighlight %} 
For a full list of supported API commands please visit our API documentation: 
[Zype Subcription API Documentation](http://dev.zype.com/api_docs/subscriptions/)


Reference Materials:
 
API Documentation: [Zype API Documentation](http://dev.zype.com/api_docs/intro/)
API Keys: [Zype Property API Keys](https://admin.zype.com/api_keys)
