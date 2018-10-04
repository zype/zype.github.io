---
layout: platform
title: Zype Developer Portal | Platform Docs
permalink: /platform_docs/plans/
redirect_to: https://support.zype.com/hc/en-us/sections/203010468-Subscription-Plans
---
## Plans
To require your consumers to pay for access to your videos, you will need to create subscription plans.
The Zype Platform supports Stripe for credit card processing.

<div style="width: 100%;">
<div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
<a href="#1">
Connecting Stripe</a>
</div>
<div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
<a href="#2">
Creating a plan</a>
</div>
<div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
<a href="#3">
Deactivating a plan</a>
</div>
</div>

<hr id="1">

## Connecting Stripe
Before creating a plan, you will need to link your Stripe Account to the Zype Platform.
In the Zype Platform, navigate to settings and enter your Stripe Secret Key.
Your Stripe Secret Key can be found under your Stripe [account settings](https://dashboard.stripe.com/account/apikeys).

![stripe settings]({{site.url}}/assets/Plan/stripe_key.png)

<hr id="2">

## Creating a plan
Once you have your Stripe Secret Key in the Zype Platform, you can create plans from the
Zype Platform that connect to your Stripe Account. To create a plan, go to the [plans page](https://admin.zype.com/plans).

![new plan]({{site.url}}/assets/Plan/new_plan.png)

You will be prompted to enter the name, plan id, statement description, trial period days,
amount, currency type, interval, and whether or not the plan is active. Note, the Plan ID has to
be a unique identifier for the plans and is what Stripe uses in its API queries.

![new plan form]({{site.url}}/assets/Plan/plan_details.png)

If your plan is active, you will be ready to have consumers subscribe to your plan!

<hr id="3">

## Deactivating a plan
You can make a plan inactive by navigating to your plan and toggling the plan to be
inactive.

![deactivate plan]({{site.url}}/assets/Plan/activate_plan.png)

Note, deactivating a plan does not affect any current subscribers to the plan.
It means that new subscribers can't be added to that plan.
