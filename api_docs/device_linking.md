---
layout: api
title: Zype Developer Portal | Device Linking
permalink: /api_docs/device_linking/
---

## Link Consumer to a Device

<hr>

You can use Zype to link a consumer to a device. At a high level, the Zype API
can check to see if the device has been linked to a Zype consumer, can acquire a pin for
a Zype consumer to link her device, and link the device to the Zype consumer via the acquired pin.

### Check to see if the device has been linked to a consumer

You will first want to see if the current device id has been linked to a Zype consumer.

<pre><b>GET</b> https://api.zype.com/pin/status/?linked_device_id=linked_device_id
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
linked_device_id      | Unique id of the end user's device | String

#### Response - Pin does not exist for that device.
<pre>404</pre>

You will need to acquire a pin for this device.

#### Response - Pin exists for the device, but has not been linked to a consumer.

200 Content-Type: application/json
<pre>
{
  "response": {
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
}
</pre>

Consumer id will be nil and linked will be false if device has not been linked to a Zype consumer.
Note, pin expires every 30 minutes. You will need to reacquire the pin after 30 minutes.

#### Response - Device has been pinned.

200 Content-Type: application/json
<pre>
  {
    "response": {
      "_id": "56c262014d656c9e6e010000",
      "consumer_id": "5466584169702d4d300d0000",
      "created_at": "2016-02-15T18:40:49.718-05:00",
      "deleted_at": null,
      "device_id": null,
      "linked_device_id": "1RG4A00102041449868105",
      "pin": "zles327",
      "pin_expiration": "2016-02-16T14:56:22.346-05:00",
      "site_id": "5463c68e69702d24db490000",
      "updated_at": "2016-02-16T14:26:22.348-05:00",
      "linked": true,
      "subscription_count": 0
    }
  }
</pre>

Consumer id will be the id of the consumer and linked will be true if device has been successfully
linked to a Zype consumer.
The subscription_count indicates the number of active subscriptions for the currently linked consumer.
Note, pin expires every 30 minutes. You will need to reacquire the pin after 30 minutes.

### Acquire pin for a device

Takes the linked device id and creates a 7 digit pin for the device. Note, pin expires
every 30 minutes. You will need to reacquire the pin after 30 minutes.

<pre><b>POST</b> https://api.zype.com/pin/acquire/?linked_device_id=linked_device_id
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
linked_device_id      | Unique id of the end user's device | String

#### Response

200 Content-Type: application/json
<pre>{
  "response"=>
    {
      "_id"=>"abc123",
      "consumer_id"=>nil,
      "created_at"=>"2015-02-05T15:12:07.814-05:00",
      "deleted_at"=>nil,
      "device_id"=>"5429b1c769702d2f7c120000",
      "linked_device_id"=>"test2",
      "pin"=>"znvm947",
      "pin_expiration"=>"2015-02-05T15:42:07.824-05:00",
      "site_id"=>"abc123",
      "updated_at"=>"2015-02-05T15:12:07.814-05:00",
      "linked"=>false
      }
    }
</pre>

### Link the consumer to the pinned device

Takes the pin and the consumer id and links the Zype consumer to the device.

<pre> <b>PUT</b> https://api.zype.com/pin/link/?consumer_id=consumer_id&pin=pin
</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
consumer_id      | Zype id of your consumer | String
pin | The acquired pin. Example: zabc123 | String

#### Response

200 Content-Type: application/json

<pre>
{
  "response": {
    "_id": "56be0daa4d656c0fbd0a0000",
    "created_at": "2016-02-12T11:51:54.634-05:00",
    "email": "a@email.com",
    "name": "a@email.com",
    "password_token": null,
    "remember_token": null,
    "rss_token": "xUz2wBCNUHT1zeDfXDO2n0dweV94VgMs1Yau7NRhqwUgIQc0YhQUEOAp8nbbgF1R",
    "site_id": "5468fd6569702d17ee500000",
    "subscription_count": 0,
    "linked_devices": [
      "908345KJSD879"
    ]
  }
}
</pre>