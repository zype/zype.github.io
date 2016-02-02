---
layout: platform
title: Zype Developer Portal | Platform Docs
permalink: /platform_docs/subscriptions/
---
## Subscriptions
Subscriptions combine consumers and plans and allow you to make money from your videos.
The Zype Platform supports Stripe and Braintree for credit card processing of consumers.

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
Coupons</a>
</div>
<div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
<a href="#4">
Creating a subscription</a>
</div>
<div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
<a href="#5">
Viewing subscriptions</a>
</div>
<div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
<a href="#6">
Canceling a subscription</a>
</div>
<div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
<a href="#subscription_settings">
Subscription Settings</a>
</div>
</div>

<hr id="1">
## Setting up a Subscription Video Widget
To get started using SVOD with Zype, login to your account and click on 'Monetization' in the sidebar.

Click 'Setup My Subscription Service' and follow the prompts to get everything set up.

![stripe settings]({{site.url}}/assets/subscription_setup/monetization.png)

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
couponsEnabled | zype.couponsEnabled = true | Whether or not to have the coupon code field on new subscription sign ups

<hr id='3'>

## Subscription Coupons

You can provide coupon codes to offer discounts to future subscribers when they subscribe
to your content.

![coupon code]({{site.url}}/assets/coupons/pay_with_coupons.png)

Currently, to enable coupons, you need to do two things. First, you need to enable coupons
on in the Zype Platform.

![enable coupons]({{site.url}}/assets/coupons/zype_enable.png)

Then, you need to create your coupons on Stripe. To create coupons on Stripe, go to your Stripe Dashboard [coupon screen](https://dashboard.stripe.com/coupons) and click on "+ New".

![add coupons]({{site.url}}/assets/coupons/stripe_add_coupon.png)

This will pop up the form to create your coupon. There are multiple coupon combinations to
choose from. You can choose to have a coupon be a percentage off or an amount off of your
subscription price. You can also choose to have a coupon be applied for one pay period, multiple
monthly pay periods, or forever. In addition, you can choose to have a maximum number of times
a coupon can be redeemed and you can choose to have a redemption deadline for your coupon.

![add coupons]({{site.url}}/assets/coupons/create_coupon.png)

When you fill out your coupon form in Stripe, keep track of your ID (Code). This is the
coupon code that you can give to people who want to subscribe to your content.

Once you click "Create Coupon", share your coupon code out to future subscribers! Feel
free to create as many coupons as you would like, they can be applied to any subscription
plan that you offer.

<hr id="4">

## Creating a subscription
You will need to [use our API](http://dev.zype.com/api_docs/subscriptions/) to create a subscription.

<hr id="5">

## Viewing subscriptions
To view subscriptions, go to the [subscriptions page](https://admin.zype.com/subscriptions).

![viewing subscriptions]({{site.url}}/assets/Connecting Stripe/consumer_details.png)

You can search by subscription and see each subscription's consumer, plan, amount, currency,
interval, trial period, and when it was created.

<hr id="6">

## Canceling a subscription
To cancel a subscription, click on the
"Subscription" on the left hand menu and click on subscriptions to get to the [subscriptions page](https://admin.zype.com/subscriptions).
Then, click the red button for the subscription that you want to cancel.

![canceling a subscription]({{site.url}}/assets/Connecting Stripe/delete_cust.png)

This will remove the subscription from Stripe.

<hr id="subscription_settings">

## Subscription Settings

In order to manage your subscription settings:

- In the nav on the left, click <b>Make Money</b>.
- Click the <b>Manage Subscription Settings</b> button.

![Settings]({{site.url}}/assets/Connecting Stripe/settings.png)

### Logo

This logo will be displayed when users are interacting with your subscription service.

### Background Color

This color will be displayed in your player if the video being shown does not have a thumbnail.

### Contact Email

The email that messages to your customers will be sent from.

### Terms of Service

If you have a TOS that users must agree to before subscribing, add a link to it here.

### Privacy policy

We recommend a Privacy Policy URL that allows you to reflect the privacy policy of your service.

### Coupons Enabled

Determines whether or not subscribers can use coupons.

### Statement Description

This is what your customers will see on their credit card statement (22 character limit). Stripe only.

### Show Zype Branding

By default we display a Zype logo at the bottom of your subscription embeds. To hide it, switch off this setting.

![Powered by Zype]({{site.url}}/assets/Connecting Stripe/powered-by-zype.jpg)