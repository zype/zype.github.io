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
All-In-One embeddable subscription Widget</a>
</div>
<div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
<a href="#2">
Overriding the subscription embed</a>
</div>
<div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
<a href="#3">
Creating a subscription</a>
</div>
<div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
<a href="#4">
Viewing subscriptions</a>
</div>
<div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
<a href="#5">
Canceling a subscription</a>
</div>
</div>

<hr id="1">
## Setting up a Subscription Video Widget
To get started using SVOD with Zype, login to your account and click on 'Monetization' in the sidebar.

Click 'Setup My Subscription Service' and follow the prompts to get everything set up.

![stripe settings]({{site.url}}assets/subscription_setup/monetization.png)

Your subscription payments are processed by Stripe so you'll need a Stripe account to complete this process.

[Click here](https://dashboard.stripe.com/register) to sign up for an account or [click here](https://dashboard.stripe.com/account/apikeys) to sign in and get your Stripe API Keys.

Once you've got everything setup, you'll either be shown an example embed code for the first video you added or a prompt to add videos if you haven't done that already.

When you return to the Monetization page, you'll now see a breakdown of your subscriptions, consumers and plans. Click on any one of these to find out more about your subscription business through Zype.

<hr id="2">

## Overriding the subscription embed

You are able to override the default subscription embed settings on a per embed basis using JavaScript.
For example, when you copy your subscription embed code, you can add additional JS inside
your script tag.

The following are variables that you enter to overwrite:

Variable | Example | Description
--------- | -------- | ----
backgroundColor | zype.backgroundColor = '#264547'; | Hexcolor of background if no video thumbnail
autoPlay | zype.autoPlay = true;   | Whether or not videos should autoplay
appName | zype.appName = 'My app name'; | Name of your app
showZype | zype.showZype = true; | Whether or not to show "Powered by Zype"

<hr id="3">

## Creating a subscription
You will need to [use our API](http://dev.zype.com/api_docs/subscriptions/) to create a subscription.

<hr id="4">

## Viewing subscriptions
To view subscriptions, go to the [subscriptions page](https://admin.zype.com/subscriptions).

![viewing subscriptions]({{site.url}}assets/Connecting Stripe/consumer_details.png)

You can search by subscription and see each subscription's consumer, plan, amount, currency,
interval, trial period, and when it was created.

<hr id="5">

## Canceling a subscription
To cancel a subscription, click on the
"Subscription" on the left hand menu and click on subscriptions to get to the [subscriptions page](https://admin.zype.com/subscriptions).
Then, click the red button for the subscription that you want to cancel.

![canceling a subscription]({{site.url}}assets/Connecting Stripe/delete_cust.png)

This will remove the subscription from Stripe.
