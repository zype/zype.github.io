---
layout: api
title: Zype Developer Portal | OAuth
permalink: /api_docs/oauth/
---
## Consumer OAuth

Zype provides an authentication mechanism for consumer authentication.
You will need to create a consumer before you can authenticate her.
Please [check out our consumer docs](http://dev.zype.com/api_docs/consumers/) to learn how to create a consumer. Once a consumer
has been created, you will authenticate her to get an access token. This access
token is then used to authenticate API requests on the behalf of your end user.

### Getting your client id and client secret

To make consumer authentication requests, you will need to use your client id and client secret keys.
To get to your client id and client secret keys ...

### Retrieving an access token

#### Via password grant flow

The password grant flow allows you to pass in a user's email address and password
and get an access token in return.

<hr />

<pre><code> POST - https://live.zype.com/oauth/token/?client_id=client_id&client_secret=client_secret&email=email&password=password&grant_type=password
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
client_id | Your Zype App's client id      | String
client_secret | Your Zype App's client secret   | String
email | Email of the end user | String
password | Password of the end user | String
grant_type | Grant Type. Use: 'password' | String

#### Response
200
Content-Type: application/json

<pre><code>{
  "access_token":"abc123",
  "token_type":"bearer",
  "expires_in":7200,
  "refresh_token":"def456",
  "scope":"public"
}
</code></pre>

#### Via authorization code grant flow

We will be supporting the authorization code grant flow in the future. If you have a need for this type of
oauth flow now, please <a href='mailto:developers@zype.com'>reach out</a>!

### Getting access token metadata

You can get additional metadata from your access token. This includes when the access token
expires, when the access token was created, and the consumer id linked to the access token.
Note, the consumer id is found in the returned "resource_owner_id" value.

<hr />

<pre>GET - https://login.zype.com/oauth/token/info?access_token=access_token<code>
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
access_token | The access token created via oauth | String

#### Response
200
Content-Type: application/json

<pre><code>{
  "resource_owner_id": "abc123",
  "scopes": [
    "consumer"
    ],
  "expires_in_seconds": 7026,
  "application": {
    "uid": "abc123"
    },
  "created_at": 1429544923
}
</code></pre>

### Refreshing an access token

Your access token will expire after 2 hours. To refresh your access token, post your refresh token and you will get a new access token in return.

<hr />

<pre><code> POST - https://api.zype.com/oauth/token/?client_id=client_id&client_secret=client_secret&refresh_token=refresh_token&grant_type=refresh_token
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
client_id | Your Zype App's client id      | String
client_secret | Your Zype App's client secret   | String
refresh_token | Token that allows you to refresh your access token | String
grant_type | Grant type. Use: 'refresh_token' | String

#### Response
200
Content-Type: application/json

<pre><code>{  
    "access_token":"abc123",
    "token_type":"bearer",
    "expires_in":30,
    "refresh_token":"def456",
    "scope":"public"
  }
</code></pre>

### Authenticating an API request on the behalf of a consumer

To authenticate an API request on the behalf of a consumer, you can pass the access token
into your API request with the access_token parameter. For example, see below how to
request a player for a SVOD video using your access token.

<pre><code> GET - https://player.zype.com/embed/abc123.js?access_token=access_token
</code></pre>

Parameter | Function | Type
--------- | -------- | ----
access_token | The access token retrieved via oauth | String
