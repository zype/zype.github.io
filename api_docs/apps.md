---
layout: api
title: Zype Developer Portal | Apps
permalink: /api_docs/apps/
---

# Apps

---

## Overview
The Zype platform contains push-button app builders which allow OTT and mobile apps to be customized and built with just a few clicks. Zype app builders contain user-customizable settings specific to the app's respective platform and SDK features. The app settings specified in the Zype platform are saved and returned by the App endpoint.

The App endpoint is used to retrieve the custom settings and content associated with an app in the Zype platform.

## Retrieve App

```
GET https://api.zype.com/app
```

### Overview
Get settings, content, and details for an application created in the Zype platform.

### Use Case
If customizing an existing Zype app SDK, customizing a third-party SDK for compatibility with the Zype platform, or creating a custom app from scratch, the app's dynamic settings and content stored in the Zype platform may be retrieved using the App endpoint. In this way, an app's settings may be updated dynamically without, in most cases, requiring a resubmission or deploying updated files.

### Parameters

Parameter | Function | Type
--------- | -------- | ----
app_key   | The app key | String

## App Object
App profiles vary by the type of application. 

```
{
  "_id": "12345",
  "active": true,
  "app_type_id": "12345",
  "site_id": "abc1234",
  "store_id": "abc1234",
  "title": "Roku Title",
  "version": 1.0,
  "store_icon_url": null
}
```
