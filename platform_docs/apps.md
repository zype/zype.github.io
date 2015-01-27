---
layout: platform
title: Zype Developer Portal | Platform Docs
permalink: /platform_docs/apps/
---
##All About Apps
The Zype Platform will help you configure apps that you will need to build and publish
to the respective application stores.

If you want a full walkthrough of creating an app, we suggest you look at the [creating an app guide.](http://dev.zype.com/platform_docs/creating_an_app/)

<div style="width: 100%">
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
    <a href="#1">
    Starting a Roku App on the Zype Platform</a>
  </div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
    <a href="#2">
    Adding Assets to Your Roku App</a>
  </div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
    <a href="#3">
    Categories, Playlists and Your Roku App</a>
  </div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
    <a href="#4">
    Building Your Roku App</a>
  </div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
    <a href="#5">
    Publishing Your Roku App</a>
  </div>
</div>


<hr id="1">

## Starting a Roku App on the Zype Platform
One of the biggest strengths of the Zype Platfom is its ability to distribute your
video content on multiple platforms like Roku. In this tutorial, we will describe how to use
the Zype Platform to create a Roku app that looks like the screen shot below.

![Roku Home](http://i.imgur.com/d15uKlK.png)

**Step 1**

Upload your videos into the Zype Platform. Roku will only serve videos from the Zype
video source. Don't worry if you have videos from other sources like Hulu and YouTube.
The Zype API can query to only show Zype Videos in your Roku App.

![Video Catalogue](http://i.imgur.com/Y6ozC6J.png)

**Step 2**

Navigate to the Video Apps screen using the left hand navigation and click on the Roku
icon to start the process of creating a new Roku App.

![Select App](http://i.imgur.com/77nsysj.png)

**Step 3**

You will be prompted to answer questions about how you want to set up your Roku App.
Don't worry if you want to change these configurations down the road.
The Zype Platform and API are designed so that these changes can be updated without having to republish your app!

For example, you can set the featured playlist, the category to iterate through, copy text, and
the colors of your Roku App any time you want from the Zype Platform. These changes will be reflected the
next time your Roku App is loaded. Only the Splash Screen and the Roku Store Icons cannot
be updated via the Zype Platform.

![New Roku App](http://i.imgur.com/gkeHiEI.png)

**Step 4**

Once you create your Roku App, you will need to publish the App on the Zype Platform
by clicking on the Publish App button so that your App's API goes live.
Then, you can use our API, Roku SDK, or reach out to Zype to help you build and publish the App on the Roku Channel Store!

**More tutorials in this series:**
Part II: [Developing the Roku Channel using the Zype SDK](http://dev.zype.com/posts/2014/11/28/develop-roku-app-with-zype-sdk/)

Part III: [Publishing the Private Roku Channel](http://dev.zype.com/posts/2014/11/28/publish-roku-app/)

<hr id="2">

## Adding Assets to Your Roku App
Adding image assets to your Roku Channel allow your to make the channel your own!
Using the Zype Platform and Zype API, you will be able to change the majority of
images on the fly without having to republish your app. However, there are a few images
that need to be bundled during installation because they make up your
application icon set. These images live on the Roku Channel store.
This tutorial will describe the images that need to be bundled, the images that can
be updated via the Zype Platform, and the specs for both.

**Assets that can only be configured during publication:**

Example assets are included in our [Roku SDK](https://github.com/zype/zype-roku/tree/master/images) and
need to be packaged with the Roku Channel are because they make up your application
icon set. They do not get loaded via a call to the Zype API:

1. [Image Home (Center Focus Icon)](https://github.com/zype/zype-roku/blob/master/images/mm_icon_focus_hd.png) - your large icon. HD is 366 x 210 pixels, SD is 248 x 140 pixels. PNG format.

2. [Image Brand (Side Icon)](https://github.com/zype/zype-roku/blob/master/images/mm_icon_side_hd.png) - your small icon. HD is 108 x 69 pixels, SD is 80 x 46 pixels. PNG format.

3. [Image Splash](https://github.com/zype/zype-roku/blob/master/images/splash_screen_hd.png) - the splash screen (what appears while your Roku Channel loads).
640 x 480 pixels. JPG format.

When publishing, you will also need a HD Poster that is a 290 x 218 JPG format and
an SD Poster that is a 214 x 144 JPG format. We call that the Image Store in our Zype Roku App.

**Assets that can be changed using the Zype Platform and Zype API:**

These assets get loaded via a call to the Zype API everytime the Roku Channel gets loaded.

![zype roku app](http://i.imgur.com/1Cqh522.png)

![zype roku app](http://i.imgur.com/lpgb3MY.png)

1. Logo - logo used in the overhang. Suggested size is 125 x 104 pixels HD, 83 x 69 SD, PNG format.

2. Slice - image tiled to create the overhang. Suggested size is 1 x 124 pixels HD and 1 x 83 SD, PNG format.

3. Grid Description Image - image used to contain text on the grid screen. Suggested size is 968 x 258 pixels HD, 502 x 177 pixels SD, PNG format.

4. Grid Border Image - image used for the highlight border on the grid screen. Suggested size is 268 x 190 pixels HD, 158 x 88 pixels SD, PNG format.

5. Info Poster - image used to link to the info page. Suggested size is 266 x 150 pixels HD & SD, PNG format.

6. Search Poster - image used to link to the search page. Suggested size is 266 x 150 pixels HD & SD, PNG format.

<hr id="3">

## Categories, Playlists and Your Roku App
We aim to make the development process of a Roku Channel as easy as possible using
our [Zype Roku SDK](https://github.com/zype/zype-roku). To do this, our sample Roku Channel
focuses on three major components of the Zype Platform: playlists, categories, and zobjects.
Since the playlists, categories, and zobjects are being pulled into your Roku channel
using the Zype API, they are all editable using the Zype Platform and do not require
republishing to the Roku Channel Store to make a change.

We will be using screenshots from our sample Roku Channel to highlight what you can do.

![playlists and categories](http://i.imgur.com/VVuBjU4.png)

**Featured Playlist**

The first slider of the home screen is the featured playlist. This can be any playlist
that you have created using the Zype Platform. Note, only Zype Videos will play.

**Categories**

Below the first slider are category sliders. Note that the category sliders and the featured playlist slider are identical.
The only difference is how we are calling the Zype API to return us the videos in each slider.
On the Zype Platform, you select a category that you want to iterate through for the rest
of the home screen. In the picture above, we are iterating through the category 'Genre.'
Thus, the first category slider is the 'Genre' with a value of 'Adventure' and the second
category slider will be the next 'Genre', which is 'Comedy'.

**Zobjects**

![Zobjects in video detail](http://i.imgur.com/gS2W1Em.png)

You also have the option to provide additional metadata about your videos in the video
detail screen. You select one zobject to be above the description and one zobject to be
below the description. In the example above, we selected the Zobject 'Actor' to be above the description
and it lists the actors that we have associated with the video. Similarly, we selected
the Zobject 'Director' to be below the description.

<hr id="4">

## Building Your Roku App
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

<hr id="5">

## Publishing Your Roku App
In [part two](http://dev.zype.com/posts/2014/11/28/develop-roku-app-with-zype-sdk/) of publishing a Roku Channel, we described how to develop a Roku app using the Zype SDK and running it locally.
In this tutorial, we will walk through how to publish a Private Roku Channel that you can
share immediately with anyone that owns a Roku. If you are interested in publishing a Public Roku Channel, the steps are very similar, just you have to wait for Roku to approve your channel before it can be accessed in the Roku Channel Store. It is recommended that you first publish a private channel, test the channel out to beta users, and then publish the channel publicly.

Before starting this tutorial, we will assume that you have already tested a Roku App
locally and are a registered Roku developer.

**Step 1**

Log into your Roku developer account and click Manage My Channels

![step 1](http://i.imgur.com/K66GKpz.png)

**Step 2**

Click add Private Channel. If you want to publish a Public Channel, click add Public Channel.
The steps are the same for private and public channels, except that you will need to
give contact information in case Roku has questions when they are reviewing your app.

![step 2](http://i.imgur.com/GeJiK58.png)

**Step 3**

Fill out Channel Properties for your channel.

![step 3](http://i.imgur.com/VZDUXsL.png)

**Step 4**

Fill our Channel Descriptions for your channel. You will need to have an HD Poster
that is a 290 x 218 JPEG file and an SD Poster that is a 214 x 144 JPEG file.

![step 4](http://i.imgur.com/pFA3aHQ.png)

**Step 5**

You can optionally upload screenshots of your Roku Channel. Read the [Roku documentation](http://sdkdocs.roku.com/display/sdkdoc/Channel+Packaging+And+Publishing#ChannelPackagingAndPublishing-38GeneratingScreenshotsSincev31onRoku1andv43onRoku2) on how to generate a screenshot.

![step 5](http://i.imgur.com/lMtmsak.png)

**Step 6**

Last, you will need to upload your application package. Follow the instructions from the [Roku documentation](http://sdkdocs.roku.com/display/sdkdoc/Channel+Packaging+And+Publishing#ChannelPackagingAndPublishing-30PackagingYourApplication) on how to generate a key and then package your channel.

Once you have downloaded your Roku Channel package, upload the application package and click the "Publish" arrow. You will get an access code url that can be used to download the private
Roku channel on your individual Roku account.


![step 6](http://i.imgur.com/xufsqQC.png)

**More tutorials in this series:**

Part I: [Creating a Roku Channel using the Zype Platform](http://dev.zype.com/posts/2014/11/25/create-roku-app-on-zype/)

Part II: [Developing the Roku Channel using the Zype SDK](http://dev.zype.com/posts/2014/11/28/develop-roku-app-with-zype-sdk/)
