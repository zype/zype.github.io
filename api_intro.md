---
layout: api_intro
title: Zype Developer Portal | API
permalink: /api_docs/intro/
---

## Introduction

Zype API documentation provides information to web developers who wish to use Zype's Application Programming Interfaces (APIs).
The Zype API includes modules for managing videos and associated metadata.
In addition, this reference describes a number of related objects. The Zype API is a RESTful API service.

Our API is designed around standard REST CRUD (Create-Read-Update-Delete) semantics:

**POST** - Create a resource within a given collection

**GET** - Get a resource or collection of resources

**PUT** - Update a resource

**DELETE** - Delete a resource

Our default is to support JSON formatting, however if you prefer XML use the Content-Type header with value text/xml.
<hr>

## Authentication

There are multiple ways to authenticate to the Zype API. Your Zype channels is automatically set up with API keys that you can integrate with, but you can also use app keys and consumer access tokens to authenticate as well.

### API Keys

Your Zype channel is automatically set up with the following API keys:

- **Admin Key:** Admin keys have full access to your account and should not be distributed in video applications.
- **Read Only Key:** Read only keys have limited access to your account and are not allowed to create or modify existing resources. Read only keys should be used when distributing a video application.
- **Player Key:** Player keys have limited access to your account and are only allowed to issue player requests. Player keys should be used in embed codes for web applications.

#### Example:

<pre><b>GET</b> https://api.zype.com/videos?api_key=[api_key]</pre>

### App Keys

App keys are automatically created when you set up new apps. App keys provide per app authentication so that each bundled app has separate credentials. App keys are automatically bundled using Zype app builders. App keys can be retrieved from your app's detail page.

#### Example:

<pre><b>GET</b> https://api.zype.com/videos?app_key=[app_key]</pre>

### Access Tokens

Access tokens provide per user authentication for API requests. Access tokens are time based tokens that are created using OAuth. [Click here](/api_docs/oauth) for more information about using OAuth.

#### Example:

<pre><b>GET</b> https://api.zype.com/videos?access_token=[access_token]</pre>

<hr>

## Errors

Zype uses conventional HTTP response codes to indicate success or failure of an API request. In general, codes in the 2xx range indicate success, codes in the 4xx range indicate an error that resulted from the provided information (e.g. a required r was missing, a charge failed, etc.), and codes in the 5xx range indicate an error with Zype's servers.

### 200 (OK)
The request was processed successfully.

### 401 (Unauthorized)
The request could not be processed because no API key was provided, or the API key provided is invalid.

### 404 (Not Found)
The request could not be processed because the resource you are operating on could not be found.

### 422 (Unprocessable Entity)
The request could not be processed due to a validation rule.

### 500 (Server Error)
The request could not be processed due to a error on Zype's servers.

### Attributes:
**message** - A human-readable message giving more details about the error.

<hr>

## Pagination

Pagination is required for all 'list' requests. The default setting for any list request is to return 10 records.

### Parameters

page (optional) The page number of records to return (zero indexed).

per_page (optional) The number of records to return (Default: 10, Maximum: 100).

### Attributes

Paging data is returned in the 'pagination' element on list requests. The following data is made available.

**current** - The current page requested

**previous** - The page before the page requested.

**next** - The page after the page requested.

**per_page** - The maximum number of records returned.

**pages** - The total number of pages available.

Example:

<pre>{
    response: { ... },
    pagination: {
        current: 1,
        previous: null,
        next: 2,
        per_page: 10,
        pages: 5
    }
}
</pre>
<hr>

## Video Formats

Videos published through the Zype platform support the following resolution and aspect ratios.

### HLS (HTTP Live Streaming):

Resolution | Aspect | Width | Height
---------- | ------ | ----- | ------
240p	     | 16x9	  | 426px	| 240px
360p	     | 16x9   | 640px	| 360px
480p	     | 16x9   | 854px	| 480px
720p	     | 16x9   | 1280px|	720px
1080p	     | 16x9   | 1920px|	1080px

### WebM/MP4 Streaming:

To ensure compatibility with devices that do not support HLS, Zype provides WebM and MP4 streams.

Format | Resolution | Aspect | Width | Height
------ | ---------- | ------ | ----- | ------
WebM   | 360p	      | 16x9	 | 640px | 360px
MP4	   | 360p	      | 16x9	 | 640px | 360px

Video formats are optional and are configurable in the Zype Publisher dashboard.
<hr>

## Client Libraries

Zype currently provides the following client libraries:

### [Ruby](https://github.com/edla/zype-cli)

If your platform of choice is not found above, you can create your own or use API code samples.
