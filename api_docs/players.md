---
layout: api
title: Zype Developer Portal | Native Players
permalink: /api_docs/players/
redirect_to: https://docs.zype.com/reference#players
---

# Players

---
Zype's Dynamic Player Technology will automatically detect which device you are requesting a player from and deliver players based on your configured player rules.

## Web Players

For web-based players like desktop, iOS, and Android browsers the Player API will return a JavaScript or Iframe player response that can be used to embed the player on a web page. For web-based players no additional integration is required.

## Native Players

For native devices like iOS, Android, and OTT set-top boxes, the Player API will return a JSON player response that can be used to play your videos. The JSON player response will include everything you need to play your video, including media files, advertising schedules and subtitles.

Developers need to specify User-Agent for all requests that are coming from Native Players.

Device | User-Agent
--------- | --------
Android (Native) | zype android
Apple TV | zype tvos
Amazon Fire TV | AmazonWebAppPlatform
Roku | Roku
iOS Native | cfnetwork

You should utilize best practices for the specific native device on how to insert your video files and ad tags. For reference,
please check out [Zype's Github](https://github.com/zype/) for our open sourced SDKs.

## Retrieve Player

```
GET https://player.zype.com/embed/[video_id].[format]
```

### Parameters

Parameter | Function | Type
--------- | -------- | ----
video_id | ID of the video to request a player (Example: `540731274c616e047a000000`) | String
autoplay | Enable autoplay for web players (Default: `false`) | Boolean
audio | Request audio-only player (Default: `false`) | Boolean
download | Request download only player (Default: `false`) | Boolean
dvr | Enable DVR for Zype Live events (Default: `true`) | Boolean
format | The format for the player response. You can request Iframes, JavaScript or JSON players depending on device capabilities (Example: `html`, `js`, `json`) | String

## Player Object (JSON)
```
{
  outputs: [
    {
      master_manifest_url: "https://player.zype.com/manifest/master.m3u8",
      url: "https://player.zype.com/manifest/abc123.m3u8",
      name: "hls"
    }
  ],
  advertising: {
    client: "vast",
    schedule: [
      {
        offset: 0
        tag: "vast_tag"
      }
    ]
  },
  subtitles: [
    {
      file: "http://u.zype.com/video/{video_id}/subtitles/English.srt?1432132167",
      label: "English"
    }
  ],
  analytics: {
    beacon: "https://ma1169-r.analytics.edgekey.net/config/beacon-10061.xml?enableGenericAPI=1",
    dimensions: {
      video_id: "5751d861b0cc5b0d24000fcf",
      site_id: "571e32ef973e2807f601267a",
      player_id: null,
      device: null
    }
  }
}
```
- master_manifest_url will be provided for Zype Live videos

