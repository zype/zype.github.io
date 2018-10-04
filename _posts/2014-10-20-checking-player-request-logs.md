---
layout: post
title:  "Checking your DPT request logs"
date:   2014-10-20 09:07:55
categories: dpt
redirect_to: https://support.zype.com/hc/en-us/articles/115010344127
---
In a previous post, we covered how to use Zype’s Dynamic Player Technology (DPT).
In this post, we'll be covering how to use the DPT logs to see what requests are being made for your video content.
For example, let's say you've uploaded a batch of new videos and after the first 30 days, you'd like to get an idea
of who's viewing your content and what times of the day are most popular for viewing.

### Where can I find my logs?

After you've uploaded some video content to the Zype platform, log in through the [admin portal](http://admin.zype.com/)
and navigate to the logs section under the settings dropdown menu. In this post, we'll cover the request logs,
so feel free to click on that link once you see the logs menu.  

![dpt logs navigation]({{site.url}}/assets/Monitoring Your Views/log_navigation_1.png)

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


![dpt logs]({{site.url}}/assets/Monitoring Your Views/request_logs.png)

### How can I search the request logs data?

The request logs screen gives you a snapshot of the most recent requests by default.

Sorting the request logs is easy: use the four drop down menus to select your search parameters
and then click on the search button.


![searching logs]({{site.url}}/assets/Monitoring Your Views/request_log_search_3.png)


*Check our [previous post](http://dev.zype.com/posts/2014/10/10/adding-zype-to-rails/)
on how to set up your Rails App with the Zype Gem!*
