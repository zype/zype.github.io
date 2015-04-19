---
layout: api
title: Zype Developer Portal | OAuth
permalink: /api_docs/oauth/
---
## Consumer OAuth

Zype provides an authentication mechanism for consumer authentication. First, you need
to have a consumer created ([see our consumer docs on how to create a
consumer](http://dev.zype.com/api_docs/consumers/)). Once a consumer has been created,
you can authenticate to get an access token. This authentication
token is then used to authenticate API requests on the behalf of your end user.

### How to get an access token

#### Via password grant flow

The password grant flow allows you to pass in a user's email address and password
and get an authentication token in return.

<hr />

<pre><code> POST - https://api.zype.com/oauth/token/?client_id=client_id&client_secret=client_secret&email=email&password=password&redirect_uri=redirect_uri
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
client_id |       | String
client_secret |   | String
email | Email of the end user | String
password | Password of the end user | String
redirect_uri |  | String

#### Response
200
Content-Type: application/json

<pre><code>{
  "access_token":"dbaf9757982a9e738f05d249b7b5b4a266b3a139049317c4909f2f263572c781",
  "token_type":"bearer",
  "expires_in":7200,
  "refresh_token":"76ba4c5c75c96f6087f58a4de10be6c00b29ea1ddc3b2022ee2016d1363e3a7c",
  "scope":"public"
}
</code></pre>

#### Via authorization code flow

We will be supporting this flow in the future. If you have a need for this type of
oauth flow. Please <a href='mailto:developers@zype.com'>reach out</a>.

### How to check the status of an access token

To check the status of an access token, you can get the details about the token
used for authentication.

<hr />

<pre><code>
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----


#### Response

#### Check if expired

#### Check expiration time

### How to refresh access token

Your access token will expire after BLANK. To refresh your access token, you will need
to post your refresh token and get a new authentication token in return.

<hr />

<pre><code> POST - https://api.zype.com/oauth/token/?client_id=client_id&client_secret=client_secret&refresh_token=refresh_token
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
client_id |       | String
client_secret |   | String
refresh_token | Token that allows you to refresh your access token | String

#### Response
200
Content-Type: application/json

<pre><code>{  
    "access_token":"ad0b5847cb7d254f1e2ff1910275fe9dcb95345c9d54502d156fe35a37b93e80",
    "token_type":"bearer",
    "expires_in":30,
    "refresh_token":"cc38f78a5b8abe8ee81cdf25b1ca74c3fa10c3da2309de5ac37fde00cbcf2815",
    "scope":"public"
  }
</code></pre>

### Authenticate an API request on the behalf of a consumer
