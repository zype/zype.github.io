---
layout: post
title:  "Publishing a Roku Channel: Part III - Publishing the Channel"
date:   2014-11-28 12:37:55
categories: developers
---

**Note, this article is depreciated as of 2/13/15. To find an up to date version
of publishing a Roku Channel, [click here]({{site.url}}posts/2015/02/13/zype-publish-roku/).**

In [part two](http://dev.zype.com/posts/2014/11/28/develop-roku-app-with-zype-sdk/) of publishing a Roku Channel, we described how to develop a Roku app using the Zype SDK and running it locally.
In this tutorial, we will walk through how to publish a Private Roku Channel that you can
share immediately with anyone that owns a Roku. If you are interested in publishing a Public Roku Channel, the steps are very similar, just you have to wait for Roku to approve your channel before it can be accessed in the Roku Channel Store. It is recommended that you first publish a private channel, test the channel out to beta users, and then publish the channel publicly.

Before starting this tutorial, we will assume that you have already tested a Roku App
locally and are a registered Roku developer.

**Step 1**

Log into your Roku developer account and click Manage My Channels

![step 1]({{site.url}}assets/Publishing Your Roku App/1.png)

**Step 2**

Click add Private Channel. If you want to publish a Public Channel, click add Public Channel.
The steps are the same for private and public channels, except that you will need to
give contact information in case Roku has questions when they are reviewing your app.

![step 2]({{site.url}}assets/Publishing Your Roku App/2.png)

**Step 3**

Fill out Channel Properties for your channel.

![step 3]({{site.url}}assets/Publishing Your Roku App/3.png)

**Step 4**

Fill our Channel Descriptions for your channel. You will need to have an HD Poster
that is a 290 x 218 JPEG file and an SD Poster that is a 214 x 144 JPEG file.

![step 4]({{site.url}}assets/Publishing Your Roku App/4.png)

**Step 5**

You can optionally upload screenshots of your Roku Channel. Read the [Roku documentation](http://sdkdocs.roku.com/display/sdkdoc/Channel+Packaging+And+Publishing#ChannelPackagingAndPublishing-38GeneratingScreenshotsSincev31onRoku1andv43onRoku2) on how to generate a screenshot.

![step 5]({{site.url}}assets/Publishing Your Roku App/5.png)

**Step 6**

Last, you will need to upload your application package. Follow the instructions from the [Roku documentation](http://sdkdocs.roku.com/display/sdkdoc/Channel+Packaging+And+Publishing#ChannelPackagingAndPublishing-30PackagingYourApplication) on how to generate a key and then package your channel.

Once you have downloaded your Roku Channel package, upload the application package and click the "Publish" arrow. You will get an access code url that can be used to download the private
Roku channel on your individual Roku account.


![step 6]({{site.url}}assets/Publishing Your Roku App/6.png)

**More tutorials in this series:**

Part I: [Creating a Roku Channel using the Zype Platform](http://dev.zype.com/posts/2014/11/25/create-roku-app-on-zype/)

Part II: [Developing the Roku Channel using the Zype SDK](http://dev.zype.com/posts/2014/11/28/develop-roku-app-with-zype-sdk/)
