---
layout: platform
title: Zype Developer Portal | Platform Docs
permalink: /platform_docs/player_rules/
---
## Player rules and Dynamic Player Technology (DPT)
Dynamic Player Technology allows you to create player rules based on geography and device.

<div style="width: 100%">
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
    <a href="#1">
    Learn about Dynamic Player Technology (DPT)</a>
  </div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
    <a href="#2">
    Setting up Player Rules</a>
  </div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
    <a href="#3">
    Monitoring your views</a>
  </div>
</div>

<hr id="1">

## Learn about Dynamic Player Technology (DPT)
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

1\. Visit the [Player rule page](https://admin.zype.com/player_rules) and click on "New Player Rule."

![player rules]({{site.url}}assets/DPT/player_rule.png)

2\. Complete the player rules form. You will need to know the countries and devices you want for your rule.
Based on countries and devices, you will be given player options that can be served to the end user.

![player rule form]({{site.url}}assets/DPT/player_rule_form.png)

### Using the API

You can query the Zype API to only show videos that dynamically conform to your DPT rules
given an end user's device and geolocation. Set dpt to equal true in your GET request.

<pre><code> GET - https://api.zype.com/videos?dpt=true
</code></pre>


### Using the player API

1\. Once you have set up your video catalog in the Zype Platform and you have created your player rules, you are ready to use the Zype Player API!

2\. You can find your player key and API key using the [Zype Platform](https://admin.zype.com/site/api)

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


<hr id='2'>

## Setting up player rules

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

<hr id="3">

## Monitoring your views
In a previous post, we covered how to use Zype’s Dynamic Player Technology (DPT).
In this post, we'll be covering how to use the DPT logs to see what requests are being made for your video content.
For example, let's say you've uploaded a batch of new videos and after the first 30 days, you'd like to get an idea
of who's viewing your content and what times of the day are most popular for viewing.

### Where can I find my logs?

After you've uploaded some video content to the Zype Platform, log in through the [admin portal](http://admin.zype.com/)
and navigate to the logs section under the settings dropdown menu. In this post, we'll cover the request logs,
so feel free to click on that link once you see the logs menu.  

![dpt logs navigation]({{site.url}}assets/Monitoring Your Views/log_navigation_1.png)

### What type of information can I see in my request logs?

The request log's screen shows you a lot of information about the requests made to view your videos.
Here are the most pertinent pieces of information:

Data | Description
---- | -----------
Video	| The video that was requested
IP address | The IP address of the requester
Country | The country the request was made from
Device	| The device the request was made from
Player	| The player that served the video
Provider | The provider of the content
Revenue model	| The revenue model of the viewer
Status	| The status of the request
Created | The date and time the request was created

![dpt logs]({{site.url}}assets/Monitoring Your Views/request_logs.png)

### How can I search the request logs data?

The request logs screen gives you a snapshot of the most recent requests by default.

Sorting the request logs is easy: use the four drop down menus to select your search parameters
and then click on the search button.


![searching logs]({{site.url}}assets/Monitoring Your Views/request_log_search_3.png)


*Check our [previous post](http://dev.zype.com/posts/2014/10/10/adding-zype-to-rails/)
on how to set up your Rails App with the Zype Gem!*
