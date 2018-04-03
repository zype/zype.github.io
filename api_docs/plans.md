---
layout: api
title: Zype Developer Portal | Subscription Plans
permalink: /api_docs/plans/
---

# Subscription Plans

Subscription plans are required for enabling subscription monetization for your video business. Subscription plans establish the base cost, payment interval frequency, interval type and duration, currency type, and more.

There are two types of plans:
* **Global** - Global plans are the default plan type for Zype subscriptions and allow customers to have access to any videos that are subscription monetized, regardless of which plan they purchase. Global plans are easier to configure and manage and therefore recommended for most video businesses as they allow you to offer simple, easy to understand payment offerings to your customer base. Typically businesses will configure global plans at different prices based on the interval type and duration: for example, a Monthly Plan at $9.99 vs an Annual Plan at $99.99
* **Tiered** - Tiered plans are an optional plan configuration for Zype subscriptions and allow consumers to only have access to videos that are associated with a specific tiered plan.  Tiered plans are generally only recommended if you have a very large video library or a selection of premium tier content that you only want to make available for certain customers. For example, you might create a Silver Plan at $4.99/month with access to a portion of your library, a Gold Plan at $7.99/month with access to a greater portion of your library, and a Platinum Plan at $9.99/month with access to your entire video library.

Read on to learn about creating and managing plans in Zype. If you've already finished creating plans, you can learn about creating and managing subscription entitlements for your consumers in [our subscriptions article](http://dev.zype.com/api_docs/subscriptions/).

<hr>
### List Subscription Plans
<pre><b>GET</b> https://api.zype.com/plans</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
page      | The page number of records to return (Example: 1) | Integer
per_page  | The number of records to return (Example: 10) | Integer
q         | Filter records by keyword | String
id        | Filter records by ID | String
id!       | Exclude records by ID | String

---

### Retrieve a Subscription Plan
<pre><b>GET</b> https://api.zype.com/plans/[id]</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | ID of the record to retrieve (Example: 5389352e69702d401b000000) | String

---

## Create a Subscription Plan
```
POST https://api.zype.com/plans
```

Note: If a video is currently monetized with a purchase, rental, or pass plan, and your property does NOT support multiple monetization, then adding that video to a playlist within a tiered subscription will disable the existing purchase, rental, or pass plan paywall and switch the paywall monetization on the video to the tiered subscription plan.

### Parameters

Parameter | Function | Type
--------- | -------- | ----
plan[name] | The name of the Plan. - **Required** | String
plan[description] | A description for the Plan. | String
plan[amount] | The amount to charge to subscribe to this Plan. - **Required** | Float
plan[currency] | The currency to charge with. - **Required** | String
plan[interval]  | The unit of time a subscriptions should last before the next charge cycle (*month,year,lifetime*). - **Required** | String
plan[interval_count] | How many *intervals* a subscription should last before the next charge cycle. - **Required** | Integer
plan[trial_period_days] | How many trial days to provide for the subscription (only for Stripe or Braintree Plans) | Integer
plan[active] | Whether or not the Plan is active - **Default:** false | Boolean
plan[stripe_id] | The Stripe Plan ID to use for this Plan - **Required for Stripe Plans** | String
plan[braintree_id] | The Braintree Plan ID to use for this Plan - **Required for Braintree Plans** | String
plan[amazon_id] | The Amazon Plan ID to use for this Plan - **Required for Amazon Plans** | String
plan[third_party_id] | An ID from a third-party payment gateway to use for this Plan | String
plan[entitlement_type] | The entitlement type for this Plan, used to change configure a plan as global or tiered (*global,tiered*) - **Default:** global | String
plan[playlist_ids] | A list of Playlist IDs to associate with a Tiered Plan - **Required for** *entitlement_type: tiered* | Array

---

## Update a Subscription Plan
```
PUT https://api.zype.com/videos/[id]
```

Note: When updating an array of objects (like `playlist_ids`] use `0` or whichever number corresponds to the resource you wish to update. It is index based and so will update the appropriate resource.

### Parameters

Parameter | Function | Type
--------- | -------- | ----
plan[name] | The name of the Plan. - **Required** | String
plan[description] | A description for the Plan. | String
plan[amount] | The amount to charge to subscribe to this Plan. - **Required** | Float
plan[currency] | The currency to charge with. - **Required** | String
plan[interval]  | The unit of time a subscriptions should last before the next charge cycle (*month,year,lifetime*). - **Required** | String
plan[interval_count] | How many *intervals* a subscription should last before the next charge cycle. - **Required** | Integer
plan[trial_period_days] | How many trial days to provide for the subscription (only for Stripe or Braintree Plans) | Integer
plan[active] | Whether or not the Plan is active - **Default:** false | Boolean
plan[stripe_id] | The Stripe Plan ID to use for this Plan - **Required for Stripe Plans** | String
plan[braintree_id] | The Braintree Plan ID to use for this Plan - **Required for Braintree Plans** | String
plan[amazon_id] | The Amazon Plan ID to use for this Plan - **Required for Amazon Plans** | String
plan[third_party_id] | An ID from a third-party payment gateway to use for this Plan | String
plan[entitlement_type] | The entitlement type for this Plan, used to change configure a plan as global or tiered (*global,tiered*)
plan[playlist_ids] | A list of Playlist IDs to associate with a Tiered Plan - **Required for** *entitlement_type: tiered* | Array

---

## Add Playlists to a Tiered Subscription Plan
```
PUT https://api.zype.com/plans/[id]/add_playlists
```
This operation is only used for Tiered Subscription Plans (i.e., plans that have entitle_type=tiered). This operation is used to determine which videos belonging to playlists in your library should be accessible to each Tiered Subscription Plan.

Once you add a playlist to a Tiered Plan, any child playlists (and videos belonging to those child playlists) will also inherit the subscription requirements from that Tiered Plan.

Note: This operation will only add the specified Playlists to the Tiered Plan, it won't remove any of the
 existing Playlists associated to it.

Note: If a video is currently monetized with a purchase, rental, or pass plan, and your property does NOT support multiple monetization, then adding that video to a playlist within a tiered subscription will disable the existing purchase, rental, or pass plan paywall and switch the paywall monetization on the video to the tiered subscription plan.

### Parameters

Parameter | Function | Type
--------- | -------- | ----
playlist_ids | A list of Playlist IDs to associate with the Plan - **Required** | Array

---

## Remove Playlists from a Subscription Plan
```
PUT https://api.zype.com/plans/[id]/remove_playlists
```

Note: This operation will only remove the specified Playlists to the Plan, if they exist.

### Parameters

Parameter | Function | Type
--------- | -------- | ----
playlist_ids | A list of Playlist IDs to remove from the Plan - **Required** | Array

---

## Delete a Subscription Plan
```
DELETE https://api.zype.com/plans/[id]
```

Note: Tiered Plans cannot be deleted.

### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | ID of the record to delete (Example: 5389352e69702d401b000000) | String

---

### Subscription Plan Object
<pre>
{
  "_id": "544813e74c616e0dc0000000",
  "_keywords": [],
  "active": true,
  "amount": "7.99",
  "created_at": "2014-10-22T20:30:31.792Z",
  "currency": "USD",
  "description": 'Description for the plan',
  "interval": "month",
  "name": "Zype Monthly Subscription",
  "stripe_id": "zype-monthly",
  "stripe_public_key": "pk_test_123456",
  "trial_period_days": 0,
  "updated_at": "2014-10-23T13:02:20.075Z",
  "entitlement_type": "tiered | global"
}
</pre>
