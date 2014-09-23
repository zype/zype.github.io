---
layout: default
title: GeoIP
permalink: /geoip/
---

## GeoIP Collection
<hr>
### Retrive an IP Address
<hr>

<pre><code>
GET - https://api.zype.com/geoip?ip_address=ip_address
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
ip_address | Defaults to IP of API caller if not provided Example: 255.255.255.255. | Number

#### Response
200
Content-Type: application/json
<pre><code>
{
    response : {
        request: "255.255.255.255",
        ip: "255.255.255.255",
        country_code2: "US",
        country_code3: "USA",
        country_name: "United States",
        continent_code: "NA",
        region_name: "NJ",
        city_name: "Cranford",
        postal_code: "07016",
        latitude: 0.00000,
        longitude: 0.00000,
        dma_code: 0,
        area_code: 0,
        timezone: "America/New_York",
        real_region_name: "New Jersey"
      }
}
</code></pre>
