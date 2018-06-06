---
layout: api
title: Zype Developer Portal | OAuth
permalink: /api_docs/oauth/
redirect_to: https://docs.zype.com/reference#oauth-1
---
## OAuth
<hr>
### Retrieving Client ID and Secret

Your client ID and secrets are provided by creating an application. Everyone application created in the Zype Platform has a unique client ID and secret.

### Retrieving an Access Token

The password grant flow allows you to pass in a user's username (email address) and password to get an access token in return.

<pre><b>POST</b> https://login.zype.com/oauth/token</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
client_id | The client ID for your Zype application      | String
client_secret | The client secret for your Zype application   | String
username | The username (email) of the consumer. <br />*Note: Password is required if username is used to authenticate.* | String
password | Password of the consumer. <br />*Note: Required if using username to authenticate.* | String
linked_device_id | The linked device ID of the consumer. <br />*Note: Pin is required if linked device ID is used to authenticate.* | String
pin | The pin for the linked device. <br />*Note: Required if using linked device ID to authenticate.* | String
grant_type | Grant Type. Use: 'password' | String

### Retrieving Access Token Status
<pre><b>GET</b> https://login.zype.com/oauth/token/info</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
access_token | The access token created via OAuth | String

### Refreshing an Access Token
<pre><b>POST</b> https://api.zype.com/oauth/token</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
client_id | The client ID for your Zype application      | String
client_secret | The client secret for your Zype application   | String
refresh_token | The refresh token returned when an access token is created | String
grant_type | Grant type. Use: 'refresh_token' | String

### Authentication Using Access Tokens

To authenticate an API request on the behalf of a consumer, you can pass the access token
into your API request with the access_token parameter. Note: Not all APIs are available for use by consumers.

<pre><b>GET</b> https://api.zype.com/videos</pre>

Parameter | Function | Type
--------- | -------- | ----
access_token | The access token retrieved via oauth | String

### Access Token Object

<pre>{
  "access_token":"abc123",
  "token_type":"bearer",
  "expires_in":7200,
  "refresh_token":"def456",
  "scope":"public"
}
</pre>
