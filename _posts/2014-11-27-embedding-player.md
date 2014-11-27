---
layout: post
title:  "Embedding a Video Using the Zype Platform"
date:   2014-11-27 10:37:55
categories: developers
---

The Zype Platform allows you to manage all of your video content in one place and
then deliver your video content across any platform or device. In this tutorial, I
will map out how to embed a video uploaded to the Zype Platform on any webpage.

**Step 1**

Navigate to your video's page and click on the Embed Code tab.

![Go to Embed Code](http://i.imgur.com/kvfYeCS.png)


**Step 2**

Copy the embed code.

![Copy Embed Code](http://i.imgur.com/yJLyMCp.png)

**Step 3**

Place the div with the id player_id where you want your player to appear on your webpage.
We recommend that video embed codes are included before the closing body tag on your site.

{% highlight html %}

<div id='player_id'></div>

<script type="text/javascript" src="https://api.zype.com/player.js"></script>
<script type="text/javascript">
zype.player_key ="3EytE8rlvjELg7sVXINIcA";
zype.play("#player_id", "5477416869702d6d03150000", { autoplay: true });
</script>

{% endhighlight %}
