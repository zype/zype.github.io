---
layout: post
title:  "Analytics: Domains, Tracking Partners, and Tracking Codes"
date:   2015-11-03 10:04:55
categories: developers
redirect_to: https://support.zype.com/hc/en-us/categories/201978178-Analytics
---

# Domains #
You can now track your player impressions by domain. This comes in handy if you are embedding your videos on more than one site and want to see which is the most popular.

The <a href="https://admin.zype.com/analytics">Zype Analytics Dashboard</a> will show you your top domain requests. Clicking the table will give you more details.

# Tracking Partner and Tracking Codes #

If you are embedding your videos on 3rd party sites and would like to track player impressions beyond just tracking the referring Domain, you can add Tracking Partner and Tracking Codes to your Embed Codes.
This is useful if you have specific campaigns or goals. For example, if your player is part of a social media promotion campaign, you may want to map the Tracking Partner to your ad agency, and the tracking code to a specific campaign or project.

The general format for usage is:

```
https://player.zype.com/embed/[video_id].html?autoplay=true&api_key=[api_key]&tracking_code=[tracking_code]&tracking_partner=[tracking_partner]
```

Note that you must always add the <b>tracking_partner</b>. The tracking_code is optional.


## Tracking Partner ##

Let's say you are embedding your videos on a site iWidgets. To track impressions by that partner you'd add tracking_partner=iwidgets to your Embed Code url:

```
https://player.zype.com/embed/[video_id].html?autoplay=true&api_key=[api_key]&tracking_partner=iwidgets
```

## Tracking Code ##

If you'd like to get more details you can add a Tracking Code. Tracking Codes are grouped by Tracking Partner. For example, if the iWidgets site is placing your videos on the <b>home</b> page and on the <b>store</b> page you could track how each of these individually performs, by adding <b>tracking_code=home</b> and <b>tracking_code=store</b>. For example

```
https://player.zype.com/embed/[video_id].html?autoplay=true&api_key=[api_key]&tracking_partner=iwidgets&tracking_code=home
```

```
https://player.zype.com/embed/[video_id].html?autoplay=true&api_key=[api_key]&tracking_partner=iwidgets&tracking_code=store
```

Note that we have also added tracking_partner=iwidgets to each of these urls.

## Modifying Your Embed Code ##

To find the embed code for your video go to the Zype Dashboard > Video Library and then click the Video you'd like to edit. Go to the Embed Code tab on the top and you'll see the video's embed code.

![embed code]({{site.url}}/assets/tracking_partner/embed.png)

### iFrame or JavaScript Embed Code ###

<b>Copy</b> the embed code. Then modify the <b>src</b> by adding the <b>tracking_partner</b> and <b>tracking_code</b> parameters. Note that you must always add the <b>tracking_partner</b>. The tracking_code is optional.

```
https://player.zype.com/embed/[video_id].html?autoplay=true&api_key=[api_key]&tracking_code=[tracking_code]&tracking_partner=[tracking_partner]
```

### Paywall Embed Code ###

If you have set up subscription, purchase, rental, or pass plans you can also add tracking_partner and tracking_code. First, grab your paywall embed code:

![paywall embed code]({{site.url}}/assets/tracking_partner/paywall_embed.png)

<b>Copy</b> the paywall embed code. You'll have to add <b>zype.tracking_partner=[tracking_partner]; zype.tracking_code=[tracking_code];</b> in the second script tag. Be sure to add it before the zype.VideoEmbed() function. For example:

```
<script type="text/javascript" src="https://play.zype.com/javascripts/subscription_embed.js"></script><div id='zype_553297c169702d0885a4435b' style='width:100%; min-width:300px; max-width:560px;'></div><script>zype.siteId = 'F7DbcH2vVnvPtYRIY1Xq9z92Bypj90i2uEcudIqK8KhNl_y-xWQNIi2UfpfzZl3N'; zype.tracking_partner=[tracking_partner]; zype.tracking_code=[tracking_code]; zype.videoId = '553297c169702d0885a4435b';zype.videoEmbed('zype_553297c169702d0885a4435b');</script>
```