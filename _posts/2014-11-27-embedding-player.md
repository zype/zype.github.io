---
layout: post
title:  "Embedding a Video Player Using the Zype Platform"
date:   2014-11-27 10:37:55
categories: developers
---

The Zype Platform allows you to manage all of your video content in one place and
then deliver your video content across any platform or device. In this tutorial, I
will map out how to embed a video uploaded to the Zype Platform on any webpage.

**Step 1**

Navigate to your video's page and click on the Embed Code tab.

![Go to Embed Code](http://i.imgur.com/4LcF8Lf.png)


**Step 2**

Copy the embed code.

![Copy Embed Code](http://i.imgur.com/jvHwsnU.png)

**Step 3**

You will need to place the div with the id 'zype_player' where you want your player
to be located on your page.

Currently, you can pass in autoplay, player_key, and subscription_id params.
The player_key is required and can be found in Settings > API. Autoplay and subscription_id
are optional.

{% highlight html %}

<div id='zype_player'></div>
<script id='zype_player_js' src='https://api.zype.com/embed/{video_id}.js?autoplay={boolean}&player_key={player_key}&subscription_id={subscription_id}' type='text/javascript'></script>

{% endhighlight %}
