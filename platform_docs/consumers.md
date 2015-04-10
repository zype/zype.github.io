---
layout: platform
title: Zype Developer Portal | Platform Docs
permalink: /platform_docs/consumers/
---
## Consumers
Zype can manage the end users of your application.
You can store metadata of your end users including name, address,
birthday. Moreover, Zype consumers can be used as an authentication end point for your
end users using your application.

<div style="width: 100%;">
<div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
<a href="#1">
Creating a Consumer</a>
</div>

<div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
<a href="#2">
Getting a Consumer's Details</a>
</div>

<div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
<a href="#3">
Removing a Consumer</a>
</div>

<div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
<a href="#4">
Connecting Stripe</a>
</div>
</div>

<hr id="1">

## Creating a Consumer

To create a consumer on the Zype Platform, navigate to the [subscriptions dashboard](https://admin.zype.com/subscription_overview) and click on consumers.

![subscriptions dashboard]({{site.url}}assets/consumers/dashboard.png)

Then, click on the "New Consumer" button and fill out your consumer's information!

![subscription new]({{site.url}}assets/consumers/new_consumer.png)

![subscription form]({{site.url}}assets/consumers/form.png)

<hr id="2">

## Getting a Consumer's Details
You can use the Zype Platform to get details about a consumer. To get a consumer's details, go to the [consumers page](https://admin.zype.com/consumers) and click on the appropriate consumer.
Information includes a consumer's email and his or her subscriptions.

![consumer information]({{site.url}}assets/Connecting Stripe/customer_details.png)

<hr id='3'>

## Removing a Consumer
You can remove a consumer from the Zype Platform. To do so, navigate to the [consumers' page](https://admin.zype.com/consumers)
and click on the red delete button for the appropriate consumer.

![delete consumer]({{site.url}}assets/Connecting Stripe/delete_cust.png)

Note, deleting a consumer will also cancel all of his or her subscriptions.

<hr id="4">

## Connecting Stripe
If you want to have your consumers pay with Stripe, you will need to link
your Stripe account to the Zype Platform. To do this, navigate to your
[settings](https://admin.zype.com/site/edit) and click on the "Monetization" tab. You can find your Stripe secret key via [account settings](https://dashboard.stripe.com/account/apikeys).

![stripe settings]({{site.url}}assets/Connecting Stripe/stripe_key.png)
