---
layout: api
title: Zype Developer Portal | Subtitle Playlists
permalink: /api_docs/subtitle_playlists/
redirect_to: https://docs.zype.com/reference#subtitle-playlists
---

# Subtitle Playlists
---

## Overview
The Subtitle Playlists API allows users to integrate subtitles with HLS manifests from a Zype video source. It's a simple way to add subtitles which will be supported in all platforms that implement the Apple HLS specification.

Each Video can have many subtitles but they are limited to have only one subtitle of each language.

* [Create a Subtitle Playlist](#create-a-subtitle-playlist)
* [Delete a Subtitle Playlist](#delete-a-subtitle-playlist)

## Create a Subtitle Playlist
```
POST https://api.zype.com/videos/[video_id]/subtitle_playlists
```

### Overview
Creates segments of subtitles in the WEBVTT format based on the source subtitle provided.

**Note:** Source subtitles **MUST** be in the SRT or VTT formats.

### Parameters

Parameter | Function | Type
--------- | -------- | ----
subtitle_playlist[source_url] | The URL for the source subtitle | String
subtitle_playlist[language] | The language of the source subtitle provided (Examples: Chinese,English,Spanish). | String

---

## Delete a Subtitle Playlist
```
DELETE https://api.zype.com/videos/[video_id]/subtitle_playlists/[language_code]
```

### Parameters

Parameter | Function | Type
--------- | -------- | ----
video_id        | ID of the Video that contains the Subtitle Playlist (Example: 5389352e69702d401b000000) | String
language_code   | Abbrevation of the language of the subtitle you want to specify (Examples: en,es,pt,ru)

---
