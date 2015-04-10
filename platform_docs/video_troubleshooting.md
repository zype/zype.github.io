---
layout: platform
title: Zype Developer Portal | Platform Docs
permalink: /platform_docs/video_troubleshooting/
---
## Video Troubleshooting

Below are some frequently asked playing videos from the Zype Platform.
Please reach out to Zype by hitting the [?] box in the lower left hand corner in the [Zype Platform](https://admin.zype.com/) if you have other questions or want additional guidance!

<div style="width: 100%;">
<div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
  <a href="#0">
    My video is in my video library, but the embed code does not work on my web browser. What do I need to do?
  </a>
</div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
    <a href="#1">
      My video works on a desktop web browser, but does not work on my Roku Channel. What is wrong?
    </a>
  </div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
    <a href="#1">
      How do I make sure my player rules are set up correctly?
    </a>
  </div>
</div>


<hr id='0'>

### My video is in my video library, but the embed code does not work on my web browser. What do I need to do?

First, make sure that your video is active. Videos that are inactive are in your video library,
but are unable to be played externally.

![video inactive]({{ site.url }}/assets/videos/inactive.png)

To activate your video, navigate to the video and toggle active on.

Next, check to make sure that your video plays in the Zype Dashboard. Navigate to your video and click on the
"Video Sources" tab. For each video source click on the camera button to watch your video.

![preview videos]({{ site.url }}/assets/videos/preview.png)

If the video does not play from the Zype data source, then you will need to have Zype
[transcode](http://en.wikipedia.org/wiki/Transcoding) your video. Click on the "Transcode Now" button.

![preview videos]({{ site.url }}/assets/videos/transcode.png)

If your video still is not playing using the embed code in your browser, check to make sure
that you have the proper [player rules set up](#2).

<hr id='1'>

### My video works on a desktop web browser, but does not work on my Roku Channel. What's wrong?

Currently, only videos that are uploaded directly to the Zype Platform or videos that are
imported from Vimeo PRO are playable on Roku devices. We currently cannot distribute
videos imported from YouTube, Vimeo, Hulu, and Crunchyroll onto Roku devices.

If you own your video content and it is currently on YouTube, Vimeo, Hulu, and/or Crunchyroll,
Zype can help you streamline the process of getting your videos playable on Roku.
Please reach out to Zype by hitting the [?] box in the lower left hand corner in the [Zype Platform](https://admin.zype.com/).

<hr id='2'>

### How do I make sure my player rules are set up correctly?

Player rules determine which player gets served to your end user based on device and geolocation.
If a player rule is not set up for the device or geography that your end user is coming from,
she will not be able to view the video. Moreover, if a player rule is not set up for
the video source where your video is coming from, your video will not be able to be viewed.

To see if you have the appropriate player rules set up, go to the [player rules page](https://admin.zype.com/player_rules)
and check the player rules that you have set up and active. Inactive player rules are grayed out.

![player rule index]({{ site.url }}/assets/player_rules/index.png)

If the player rule you want is inactive, click on the player rule. Then, click on the activate button.

![player rule activate]({{ site.url }}/assets/player_rules/activate.png)

If you do not see the appropriate player rule based on player, device, and geolocation, click on the "New Player Rule" button.

![player rule button]({{ site.url }}/assets/player_rules/new_button.png)

Then, you will need to select the geolocation, device, and player that you want for the rule.

![player rule step]({{ site.url }}/assets/player_rules/geolocation.png)

![player rule step]({{ site.url }}/assets/player_rules/device.png)

![player rule step]({{ site.url }}/assets/player_rules/player.png)

![player rule step]({{ site.url }}/assets/player_rules/confirm.png)

Player rules can be tricky. Please reach out to Zype by hitting the [?] box in the lower left hand corner in the [Zype Platform](https://admin.zype.com/) if you have any questions!
