---
layout: api
title: Zype Developer Portal | Plans
permalink: /api_docs/plans/
---

## Plans Collection

<hr>
### List Plans
<pre><b>GET</b> https://api.zype.com/plans</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
page      | The page number of records to return (Example: 1) | Integer
per_page  | The number of records to return (Example: 10) | Integer
q         | Filter records by keyword | String
id        | Filter records by ID | String
id!       | Exclude records by ID | String

### Retrieve a Plan
<pre><b>GET</b> https://api.zype.com/plans/[id]</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | ID of the record to retrieve (Example: 5389352e69702d401b000000) | String

## Create a Plan
```
POST https://api.zype.com/plans
```

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
plan[entitlement_type] | The entitlement type for this Plan (*tiered,global*) - **Default:** global | String
plan[playlist_ids] | A list of Playlist IDs to associate with the Plan - **Require** *entitlement_type: tiered* | Array

---

## Update a Plan
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
plan[entitlement_type] | The entitlement type for this Plan (*tiered,global*) - **Default:** global | String
plan[playlist_ids] | A list of Playlist IDs to associate with the Plan - **Require** *entitlement_type: tiered* | Array

---

## Add Playlists to a Plan
```
PUT https://api.zype.com/plans/[id]/add_playlists
```

Note: This operation will only add the specified Playlists to the Plan, it won't remove any of the
 existing Playlists associated to it

### Parameters

Parameter | Function | Type
--------- | -------- | ----
playlist_ids | A list of Playlist IDs to associate with the Plan - **Required** | Array

---

## Remove Playlists from a Plan
```
PUT https://api.zype.com/plans/[id]/remove_playlists
```

Note: This operation will only remove the specified Playlists to the Plan, if they exist.

### Parameters

Parameter | Function | Type
--------- | -------- | ----
playlist_ids | A list of Playlist IDs to remove from the Plan - **Required** | Array

---

## Delete a Plan
```
DELETE https://api.zype.com/plans/[id]
```

Note: Tiered Plans cannot be deleted.

### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | ID of the record to delete (Example: 5389352e69702d401b000000) | String

---

### Plan Object
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