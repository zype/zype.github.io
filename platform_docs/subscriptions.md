---
layout: platform
title: Zype Developer Portal | Platform Docs
permalink: /platform_docs/subscriptions/
---
## Subscriptions
Subscriptions combine consumers and plans and allow you to make money from your videos.
The Zype Platform supports Stripe for credit card processing of consumers.

<div style="width: 100%;">
<div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
<a href="#1">
Connecting Stripe</a>
</div>
<div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
<a href="#2">
Creating a Subscription</a>
</div>
<div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
<a href="#3">
Viewing Subscriptions</a>
</div>
<div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
<a href="#4">
Cancelling a Subscription</a>
</div>
</div>

<hr id="1">

## Connecting Stripe
Before creating a subscription, you will need to link your Stripe Account to the Zype Platform.
In the Zype Platform, navigate to settings and enter your Stripe Secret Key.
Your Stripe Secret Key can be found under your Stripe [account settings](https://dashboard.stripe.com/account/apikeys).


![stripe settings]({{site.url}}assets/Connecting Stripe/stripe_key.png)

<hr id="2">

## Creating a Subscription
You will need to [use our API](http://dev.zype.com/api_docs/subscriptions/) to create a subscription.

<hr id="3">

## Viewing Subscriptions
To view subscriptions, go to the [subscriptions page](https://admin.zype.com/subscriptions).

![viewing subscriptions]({{site.url}}assets/Connecting Stripe/customer_details.png)

You can search by subscription and see each subscription's consumer, plan, amount, currency,
interval, trial period, and when it was created.

<hr id="4">

## Cancelling a Subscription
To cancel a subscription, click on the
"Subscription" on the left hand menu and click on subscriptions to get to the [subscriptions page](https://admin.zype.com/subscriptions).
Then, click the red button for the subscription that you want to cancel.

![cancelling a subscription]({{site.url}}assets/Connecting Stripe/delete_cust.png)

This will remove the subscription from Stripe.
