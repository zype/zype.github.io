---
layout: platform
title: Zype Developer Portal | Platform Docs
permalink: /platform_docs/player_rules/
---
##All About Player Rules and Dynamic Player Technology (DPT)
The Zype Platform is feature rich, so we want to provide you with a place to learn more about it.
Below are a bunch of short tutorials (with pictures!) to help you with player rules.

<div style="width: 100%">
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
    <a href="#1">
    Learn About Dynamic Player Technology (DPT)</a>
  </div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
    <a href="#2">
    Monitoring Your Views</a>
  </div>
</div>

<hr id="1">

## Learn About Dynamic Player Technology (DPT)
Zype’s DPT allows you to create player rules based on geography and device.
For example, you could declare that end users will receive the Hulu Player if he
or she is accessing your video via desktop in the United States or the Zype Player
if he or she is accessing your video via desktop in Australia.

### What you need to start

You will need to have a video collection on the Zype Platform from the video sources
that you want to create player rules for.

1\. Make sure you have imported your videos into your [video catalogue](https://admin.zype.com/video_imports)
on the Zype Platform.

![video imports](http://i.imgur.com/XmeaBMa.png)

### What you need to do in the Zype Platform

1\. Visit the [Player Rule Page](https://admin.zype.com/player_rules) and click on New Player Rule

![player rules](http://i.imgur.com/qDK0aoL.png)

2\. Complete the Player Rules Form. You will need to know the countries and devices you want for your rule.
Based on countries and devices, you will be given player options that can be served to the end user.

![player rule form](http://i.imgur.com/nxcYd0K.png)

### Using the Player API

1\. Once you have set up your video catalogue in the Zype Platform and you have created your player rules, you are ready to use the Zype Player API!

2\. You can find your player key and api key using the [Zype Platform](https://admin.zype.com/site/api)

![site keys](http://i.imgur.com/V7UoP3i.png?1)

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


<hr id="2">

## Monitoring Your Views
In a previous post, we covered how to use Zype’s Dynamic Player Technology (DPT).
In this post, we'll be covering how to use the DPT logs to see what requests are being made for your video content.
For example, let's say you've uploaded a batch of new videos and after the first 30 days, you'd like to get an idea
of who's viewing your content and what times of the day are most popular for viewing.

### Where can I find my logs?

After you've uploaded some video content to the Zype platform, log in through the [admin portal](http://admin.zype.com/)
and navigate to the logs section under the settings dropdown menu. In this post, we'll cover the request logs,
so feel free to click on that link once you see the logs menu.  

![dpt logs navigation](http://i.imgur.com/werWhEG.png)

### What type of information can I see in my request logs?

The request logs screen shows you lots of information about the requests made to view your videos.
Here are the most pertinent pieces of information:

Data | Description
---- | -----------
Video	| The video that was requested
IP Address | The IP address of the requester
Country | The country the request was made from
Device	| The device the request was made from
Player	| The player that served the video
Provider | The provider of the content
Revenue Model	| The revenue model of the viewer
Status	| The status of the request
Created | The date and time the request was created

![dpt logs](http://i.imgur.com/Y8DzoV9.png)

### How can I search the request logs data?

The request logs screen gives you a snapshot of the most recent requests by default.

Sorting the request logs is easy: use the four drop down menus to select your search parameters
and then click on the search button.


![searching logs](http://i.imgur.com/XgruOt5.png)


*Check our [previous post](http://dev.zype.com/posts/2014/10/10/adding-zype-to-rails/)
on how to set up your Rails App with the Zype Gem!*
