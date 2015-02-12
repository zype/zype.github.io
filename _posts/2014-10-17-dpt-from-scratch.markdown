---
layout: post
title:  "Using Zype's Dynamic Player Technology (DPT)"
date:   2014-10-17 15:53:00
categories: dpt
---
Zype’s DPT allows you to create player rules based on geography and device.
For example, you could declare that end users will receive the Hulu Player if he
or she is accessing your video via desktop in the United States or the Zype Player
if he or she is accessing your video via desktop in Australia.

### What you need to start

You will need to have a video collection on the Zype Platform from the video sources
that you want to create player rules for.

1\. Make sure you have imported your videos into your [video catalogue](https://admin.zype.com/video_imports)
on the Zype Platform.

![video imports]({{site.url}}assets/DPT/add_videos.png)

### What you need to do in the Zype Platform

1\. Visit the [Player Rule Page](https://admin.zype.com/player_rules) and click on New Player Rule

![player rules]({{site.url}}assets/DPT/player_rule.png)

2\. Complete the Player Rules Form. You will need to know the countries and devices you want for your rule.
Based on countries and devices, you will be given player options that can be served to the end user.

![player rule form]({{site.url}}assets/DPT/player_rule_form.png)

### Using the Player API

1\. Once you have set up your video catalogue in the Zype Platform and you have created your player rules, you are ready to use the Zype Player API!

2\. You can find your player key and api key using the [Zype Platform](https://admin.zype.com/site/api)

![site keys]({{site.url}}assets/API/site_key.png)

3a\. To make the API call to get the appropriate player
{% highlight ruby %}
GET http://api.zype.com/videos/{video_id}/player/?api_key={api_key}&player_key={player_key}
{% endhighlight %}

3b\. To use the [Zype Ruby Gem](https://github.com/edla/zype-cli) to get the appropriate player
{% highlight ruby %}
@zype_cli = Zype::Client.new
@video = @zype_cli.videos.find(params[:video_id])
@player = @video.player(player_key: params[:player_key])
{% endhighlight %}

*Check our [previous post](http://dev.zype.com/posts/2014/10/10/adding-zype-to-rails/)
on how to set up your Rails App with the Zype Gem!*
