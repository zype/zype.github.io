---
layout: api
title: Zype Developer Portal | Device Linking
permalink: /api_docs/device_linking/
---

# Device Linking

---

## Retrieve Device Pin

```
GET https://api.zype.com/pin/status
```

### Parameters

Parameter | Function | Type
--------- | -------- | ----
linked_device_id | Unique ID of the user's device | String


## Create Device Pin

```
POST https://api.zype.com/pin/acquire
```

### Parameters

Parameter | Function | Type
--------- | -------- | ----
linked_device_id | Unique ID of the user's device | String

## Link Device Pin

```
PUT https://api.zype.com/pin/link
```

### Parameters

Parameter | Function | Type
--------- | -------- | ----
consumer_id | ID of the consumer to link | String
pin | The value for the acquired device pin (Example: `zabc123`) | String


## Unlink Device Pin

```
PUT https://api.zype.com/pin/unlink
```

### Parameters

Parameter | Function | Type
--------- | -------- | ----
consumer_id | ID of the consumer to link | String
pin | The value for the acquired device pin (Example: `zabc123`) | String


## Device Pin Object

```
{
  "_id": "57113fc6f283474159000004",
  "consumer_id": null,
  "created_at": "2016-04-15T15:23:50.198-04:00",
  "deleted_at": null,
  "device_id": null,
  "linked_device_id": "sdkjafklsjdklfjasdf",
  "pin": "zizm529",
  "pin_expiration": "2016-04-15T15:53:50.195-04:00",
  "site_id": "5468fd6569702d17ee500000",
  "updated_at": "2016-04-15T15:23:50.198-04:00",
  "linked": false,
  "subscription_count": null
}
```
