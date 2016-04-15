---
layout: api
title: Zype Developer Portal | GeoIP
permalink: /api_docs/geoip/
---

## GeoIP
<hr>
### Retrieve an IP Address

<pre><b>GET</b> https://api.zype.com/geoip</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
ip_address | Defaults to IP of API caller if not provided Example: 255.255.255.255. | String

### GeoIP Object

<pre>
{
  "request": "108.29.95.21",
  "ip": "108.29.95.21",
  "country_code": 225,
  "country_code2": "US",
  "country_code3": "USA",
  "country_name": "United States",
  "continent_code": "NA"
}
</pre>
