---
layout: api
title: Zype Developer Portal | Video Manifests
permalink: /api_docs/manifests/
redirect_to: https://docs.zype.com/reference#manifests
---

## Video Manifests Collection
<hr>

### Retrieve a Live Video Manifest URL

Returns an object containing the **id** and the masked **url** for the manifest.

<pre><b>GET</b> https://api.zype.com/manifest/live/[id]</pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
id        | ID of the record (Example: 5389352e69702d401b000000) | String

### Video Manifest Object
<pre>{
  "response": {
    "_id": "59db911f6e82c2000100000e",
    "url": "https://1hc0aipw92.execute-api.us-east-1.amazonaws.com/latest/eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJhZF91cmwiOiJodHRwczovL3p5cGVsaXZlLWxoLmFrYW1haWhkLXN0YWdpbmcubmV0L2kvZGVmYXVsdF8xQEFzdGFjb21tL21hc3Rlci5tM3U4P3N0YXJ0PTE1MDc1NjE3MjkmaGRudHM9ZXhwJTNEMTUwODUzNTMxNSU3RWFjbCUzRCUyRiolNDBBc3RhY29tbSUyRiolN0VobWFjJTNENjhjMDU2MjRjNzQ0YzY4MWUyNDQ2YjcyZGFjYzllN2U1MWNhYTA5ZWRjZjgyNTk5ZTUwYzI0MmQ2ZjQzMWQ2MSIsInZpZGVvX2lkIjoiNTlkYjkxMWY2ZTgyYzIwMDAxMDAwMDBlIiwic2l0ZV9pZCI6IjU5ODMzMmVlODExMzc4MDAwMTAwMDBlNyIsImRhdGUiOiIyMDE3LTEwLTE5VDIxOjM1OjE1KzAwOjAwIiwiZW52Ijoic3RhZ2UifQ.v2H5T5BHO5jYFE2AQ1TW7EP33624up7oM3KuNOg6BBY"
  }
}</pre>
