---
layout: api
title: Zype Developer Portal | Native Players
permalink: /api_docs/players/
---

## Native Players

For native players like iOS, Android, and OTT devices, Zype returns a JSON player response for you to use to play your video. The following are included in the player response: player manifest url, type of video file, ad tags, and subtitles.
You should utilize best practices for the specific native device on how to insert your video files and ad tags. For reference,
please checkout [Zype's Github](https://github.com/zype/) for our open sourced SDKs.

### What to expect from the JSON responses

Videos from the Zype Platform are in either "HLS" or "MP4" format. For advertising,
the offset is the time in milliseconds from the start of the video for when the
advertising is scheduled. You will need to parse the advertising tag natively.

### How to get the Native Player JSON

Because of Zype's Dynamic Player Technology, the Zype Platform will automatically
detect which device you are coming from to get your player. If you would like to
get a different device response, or a native device response in a web browser, you will need to spoof the device.

<pre><code> GET - https://player.zype.com/embed/{video_id}.json?api_key={api_key}
</code></pre>

#### Roku JSON Response
<pre><code>{
  :outputs=>
    [
      {
        :url => "https://player.zype.com/manifest/abc123.m3u8",
        :name => "hls"
      }
    ],
  :advertising =>
    {
      :client => "vast",
      :schedule => [
        {
          :offset => 0
          :tag => "vast_tag"
        }
      ]
    },
    :subtitles =>
      [
        {
          :file => "http://zype-upload.s3.amazonaws.com/video/{video_id}/subtitles/English.srt?1432132167",
          :label => "en"
        }
      ]
  }
</code></pre>

#### iOS JSON Response

<pre><code>{
  :files => [
    {
      :url => "https://player.zype.com/manifest/abc123.m3u8",
      :name => "hls"
    }
  ],
  :advertising =>
    {
      :client => "vast",
      :schedule => [
        {
          :offset => 0
          :tag => "vast_tag"
        }
      ]
    }
  :subtitles =>
    [
      {
        :file => "http://zype-upload.s3.amazonaws.com/video/{video_id}/subtitles/English.srt?1432132167",
        :label => "en"
      }
    ]
}
</code></pre>
