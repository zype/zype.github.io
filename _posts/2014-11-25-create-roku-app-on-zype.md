---
layout: post
title:  "Publishing a Roku Channel: Part I - Creating a Roku App Using the Zype Platform"
date:   2014-11-25 10:37:55
categories: developers
---

**Note, this article is depreciated as of 2/13/15. To find an up to date version
of publishing a Roku Channel, [click here]({{site.url}}posts/2015/02/13/zype-publish-roku/).**

One of the biggest strengths of the Zype Platfom is its ability to distribute your
video content on multiple platforms like Roku. In this tutorial, we will describe how to use
the Zype Platform to create a Roku app that looks like the screen shot below.

![Roku Home]({{site.url}}assets/Creating an App/roku.png)

**Step 1**

Upload your videos into the Zype Platform. Roku will only serve videos from the Zype
video source. Don't worry if you have videos from other sources like Hulu and YouTube.
The Zype API can query to only show Zype Videos in your Roku App.

![Video Catalogue]({{site.url}}assets/Creating an App/videos.png)

**Step 2**

Navigate to the Video Apps screen using the left hand navigation and click on the Roku
icon to start the process of creating a new Roku App.

![Select App]({{site.url}}assets/Creating an App/vid_app.png)

**Step 3**

You will be prompted to answer questions about how you want to set up your Roku App.
Don't worry if you want to change these configurations down the road.
The Zype Platform and API are designed so that these changes can be updated without having to republish your app!

For example, you can set the featured playlist, the category to iterate through, copy text, and
the colors of your Roku App any time you want from the Zype Platform. These changes will be reflected the
next time your Roku App is loaded. Only the Splash Screen and the Roku Store Icons cannot
be updated via the Zype Platform.

![New Roku App]({{site.url}}assets/Creating an App/new_video_app.png)

**Step 4**

Once you create your Roku App, you will need to publish the App on the Zype Platform
by clicking on the Publish App button so that your App's API goes live.
Then, you can use our API, Roku SDK, or reach out to Zype to help you build and publish the App on the Roku Channel Store!

**More tutorials in this series:**
Part II: [Developing the Roku Channel using the Zype SDK](http://dev.zype.com/posts/2014/11/28/develop-roku-app-with-zype-sdk/)

Part III: [Publishing the Private Roku Channel](http://dev.zype.com/posts/2014/11/28/publish-roku-app/)
