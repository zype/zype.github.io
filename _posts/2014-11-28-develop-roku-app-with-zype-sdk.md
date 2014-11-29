---
layout: post
title:  "Publishing a Roku Channel: Part II - Developing Your Roku App Using the Zype SDK"
date:   2014-11-28 10:37:55
categories: developers
---

In a [previous tutorial](http://dev.zype.com/posts/2014/11/25/create-roku-app-on-zype/),
we described how to create a Roku App using the Zype Platform. In this tutorial,
we will walk through how to develop a Roku app using the Zype SDK and testing it locally.

To complete this tutorial, we expect that you know how to clone a repo on GitHub. You do
not need to have prior experience with the [BrightScript language](http://sdkdocs.roku.com/display/sdkdoc/BrightScript+Language+Reference)
that Roku uses to create Roku Channels, but you should be comfortable with programming because
you will need to update some variables within the cloned app and [telnet](http://en.wikipedia.org/wiki/Telnet).

Moreover, you need to have a Roku available to test out your app and a developer account with Roku to publish the app. [Register here](https://www.roku.com/developer) for a Roku developer account.

**Step 1**

You should have already created a Roku App on the Zype Platform. If you need help
creating a Roku App from the Zype Platform, please read our [previous tutorial](http://dev.zype.com/posts/2014/11/25/create-roku-app-on-zype/).

**Step 2**

Now that you have a Roku App created on the Zype Platform, you will need to turn developer mode
on for your Roku. This will allow you to test out your app before you publish it on your local Roku.

To set up your Roku for developer mode, navigate to the home screen of your Roku
and, with your Roku remote control, click the following:

<pre><code>Home 3x, Up 2x, Right, Left, Right, Left, Right.</code></pre>

On your Roku, you will be prompted to enter a developer password for the Roku device.
Record the password that you enter because it will be used to load your channel in development mode.

You will also need to record your Roku Player's IP address. In your Roku, go to
Settings > Network to find it.

**Step 3**

Now that your Roku is set up for developer mode and you have recorded your Developer Password
and your Roku Player's IP address, you are set to grab the Zype Roku SDK from our GitHub account.

Clone the repo [here](http://github.com/zype/zype-roku).

**Step 4**

Once you have the code on your computer, you will need to do 3 things to customize the Roku app
for your own app.

First, you need to open the app.mk file and set the ROKU_DEV_TARGET to your Roku Player's IP
address and set the DEVPASSWORD to your Developer Password.

Second, you will need to change the hard coded keys/initialization variables that are
located in source/objects/config.brs. You will be able to find your api_key, app_key, and
player_key in the Zype Platform.

Third, you need to make sure that the APPNAME in the Makefile matches the name of the Roku App's directory that you cloned into. If you do not change anything from cloning, the Makefile and the
directory name should both be zype-roku.

**Step 5**

Now, its time to test run your Roku App on your local Roku. Navigate to the Roku app's directory in your computer's terminal and run:

<pre><code>$ make install</code></pre>

This will build the app onto your local Roku. Once the build is finished, the channel will automatically load. Test to make sure everything works appropriately.

Now that your Roku app is built, you will need to publish the app to the Roku Channel store.
[Click here](http://dev.zype.com/posts/2014/11/28/publish-roku-app/) to read how to publish your Roku App.

**More tutorials in this series:**

Part I: [Creating a Roku Channel using the Zype Platform](http://dev.zype.com/posts/2014/11/25/create-roku-app-on-zype/)

Part III: [Publishing the Private Roku Channel](http://dev.zype.com/posts/2014/11/28/publish-roku-app/)
