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

<hr>

### Check to see if the device has been linked to a consumer

You will first want to see if the current device id has been linked to a Zype consumer.
<hr>
<pre><code>GET - https://api.zype.com/pin/status/?linked_device_id=linked_device_id
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
linked_device_id      | Unique id of the end user's device | String

#### Response - Device has never been pinned.
<pre><code>404</code></pre>

You will need to acquire a pin for this device.

#### Response - Device has been pinned.

200 Content-Type: application/json
<pre><code>{
  "response"=>
    {
      "_id"=>"1234abc",
      "consumer_id"=>nil,
      "created_at"=>"2015-02-05T15:12:07.814-05:00",
      "deleted_at"=>nil,
      "device_id"=>"5429b1c769702d2f7c120000",
      "linked_device_id"=>"1234ABCXY",
      "pin"=>"znvm947",
      "pin_expiration"=>"2015-02-05T15:42:07.823-05:00",
      "site_id"=>"abc123",
      "updated_at"=>"2015-02-05T15:12:07.814-05:00",
      "linked"=>false}
    }
  }
</code></pre>

Consumer id will be nil and linked will be false if device has not been linked to a Zype consumer.
Note, pin expires every 30 minutes. You will need to reacquire the pin after 30 minutes.
Consumer id will be the id of the consumer and linked will be true if device has been successfully
linked to a Zype consumer.

<hr>

### Acquire pin for a device

Takes the linked device id and creates a 7 digit pin for the device. Note, pin expires
every 30 minutes. You will need to reacquire the pin after 30 minutes.

<hr>

<pre><code>POST - https://api.zype.com/pin/acquire/?linked_device_id=linked_device_id&type=type
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
linked_device_id      | Unique id of the end user's device | String
type | Type of device. Example: roku | String

#### Response

200 Content-Type: application/json
<pre><code>{
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
</code></pre>

<hr>

### Link the consumer to the pinned device

Takes the pin and the consumer id and links the Zype consumer to the device.

<hr>

<pre><code> PUT - https://api.zype.com/pin/link/?consumer_id=consumer_id&pin=pin
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
consumer_id      | Zype id of your consumer | String
pin | The acquired pin. Example: zabc123 | String

#### Response

200 Content-Type: application/json

<pre><code>{
  "response"=>
    {
      "_id"=>"abc123",
      "_keywords"=>["api", "com", "docs", "example"],
      "created_at"=>"2015-01-08T14:51:34.907-05:00",
      "deleted_at"=>nil,
      "email"=>"api-docs@example.com",
      "site_id"=>"abc123",
      "stripe_id"=>"cus_abc123",
      "subscription_count"=>1,
      "updated_at"=>"2015-01-08T14:51:34.907-05:00",
      "linked_devices"=>
        [ "test1""]
      }
    }
</code></pre>

<hr>
