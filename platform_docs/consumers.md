---
layout: platform
title: Zype Developer Portal | Platform Docs
permalink: /platform_docs/consumers/
---
##All About Consumers
Consumers are the backbone of Zype's Subscription Service. Consumers, with a plan,
create a subscription. The Zype Platform supports Stripe for credit card processing of consumers.

<div style="width: 100%;">
<div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
<a href="#1">
Connecting Stripe</a>
</div>
<div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
<a href="#2">
Creating a Consumer</a>
</div>
<div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
<a href="#3">
Getting a Consumer's Details</a>
</div>
<div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
<a href="#4">
Removing a Consumer</a>
</div>
</div>

<hr id="1">

## Connecting Stripe
Before creating a consumer, you will need to link your Stripe Account to the Zype Platform.
In the Zype Platform, navigate to settings and enter your Stripe Secret Key. Your Stripe Secret Key can be found under your Stripe [account settings](https://dashboard.stripe.com/account/apikeys).

![stripe settings]({{site.url}}assets/Connecting Stripe/stripe_key.png)

<hr id="2">

## Creating a Consumer
You will need to [use our API](http://dev.zype.com/api_docs/consumers/) to create consumers.

<hr id='3'>

## Getting a Consumer's Details
You can use the Zype Platform to get details about a consumer. To get a consumer's details, go to the [consumers page](https://admin.zype.com/consumers) and click on the appropriate consumer.
Information includes a consumer's email and his or her subscriptions.

![consumer information]({{site.url}}assets/Connecting Stripe/customer_details.png)

<hr id="4">

## Removing a Consumer
You can remove a consumer from the Zype Platform. To do so, navigate to the [consumers' page](https://admin.zype.com/consumers)
and click on the red delete button for the appropriate consumer.

![delete consumer]({{site.url}}assets/Connecting Stripe/delete_cust.png)

Note, deleting a consumer will also cancel all of his or her subscriptions.
