---
layout: api
title: Zype Developer Portal | GeoIP
permalink: /api_docs/geoip/
---

## GeoIP Collection
<hr>
### Retrive an IP Address
<hr>

<pre><code>GET - https://api.zype.com/geoip?ip_address=ip_address
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
ip_address | Defaults to IP of API caller if not provided Example: 255.255.255.255. | Integer

#### Response
200
Content-Type: application/json
<pre><code>{
  "response": {
    "request": "108.29.95.21",
    "ip": "108.29.95.21",
    "country_code": 225,
    "country_code2": "US",
    "country_code3": "USA",
    "country_name": "United States",
    "continent_code": "NA"
  }
}
</code></pre>
