---
layout: platform
title: Zype Developer Portal | Platform Docs
permalink: /platform_docs/apps/
---
##All About Apps
The Zype Platform will help you configure apps that you will need to build and publish
to the respective application stores.

If you want a full walkthrough of creating an app, we suggest you look at the [creating an app guide.]({{site.url}}platform_docs/creating_an_app/)

<div style="width: 100%">
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
    <a href="#1">
    Publishing a Roku Channel Through Zype</a>
  </div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
    <a href="#2">
    Self Publishing a Roku Channel Through Zype</a>
  </div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
    <a href="#3">
    Adding Assets to Your Roku Channel</a>
  </div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
    <a href="#4">
    Categories, Playlists and Your Roku Channel</a>
  </div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
    <a href="#5">
    Creating an iPhone App from the Zype Platform</a>
  </div>
</div>


<hr id="1">

## Publishing a Roku Channel Through Zype
REDO

<hr id="2">

## Self Publishing a Roku Channel Through Zype
Before being ready to self-publish, you will need to set up your Roku Channel on the Zype
Platform. [Click here]({{site.url}}posts/2015/02/13/zype-publish-roku) to read up on
how to set up your Roku Channel for publishing.
To self-publish your Roku Channel, you will need to have a Roku device and be
comfortable using the terminal. This tutorial is focused for those users who are
on Mac or linux. If you are on Windows, you can follow along with the tutorial,
but you will need to use the [Eclipse BrightScript plug-in to package your Roku Channel](http://sdkdocs.roku.com/display/sdkdoc/Eclipse+Plugin+Guide) (step 2).

**Step 1: Enable Roku Development Mode on Your Box**

You will need to enable Roku Development Mode on your Roku device. Read through the [Roku
Documentation](http://sdkdocs.roku.com/display/sdkdoc/Developer+Guide#DeveloperGuide-70LoadingandRunningyourApplicationWalkthrough)
on how to load and run your Roku Channel.

Please store your ROKU_DEV_TARGET (the IP address
of your Roku) and DEVPASSWORD (you will get to choose this when you set up your Roku Developer Device). You will need both of these to side load
your Roku Channel into your Roku device.


**Step 2: Unzip your bundled channel and test out locally (Mac/Linux)**

Zype will email you a bundled channel zip that contains the BrightScript code for your Roku Channel. You will need to unzip your channel and, in your terminal, navigate to the Roku code.

Next, open up app.mk in your text editor of choice and change the ROKU_DEV_TARGET
and DEVPASSWORD to match your Roku device.

![app.mk replacement]({{site.url}}assets/Publishing Your Roku App/replace_appmk_vars.png))

Then, run make install inside the Roku Channel directory in your terminal to side load your Roku Channel to your Roku device.

![make install]({{site.url}}assets/Publishing Your Roku App/make_install.png))

If the command is successful, your Roku Channel will load automatically to your Roku Device.

**Step 3: Package Your Roku Channel for Publishing**

You will need to key your Roku Channel using your Roku device.
Please read the official [Roku
documentation](http://sdkdocs.roku.com/display/sdkdoc/Channel+Packaging+And+Publishing#ChannelPackagingAndPublishing-30PackagingYourApplication)
on how to generate your key and key your device.

**Step 4: Submit Your Roku Channel to the Roku Channel Store**

Now that you have a packaged Roku Channel, you will need to submit your Roku Channel to the Roku Channel Store. You can choose to either publish
a private channel or a public channel. A private channel will be published right away, but is not searchable via the Roku Channel Store. You will
be given a Channel URL that you can share to others to add your private channel. To publish a public channel, you will added to the Roku
Publishing Queue for Roku QA. This queue takes approximately 3-4 to get to the front of. You should expect it to take 4-6 weeks to get your
public Roku Channel available on the Roku Channel Store.

Click [here](https://owner.roku.com/Developer/Apps) to submit your Roku Channel!
You will have to be logged into your Roku Developer Account.

*Please feel free to reach out to Zype using the question box [in the lower left hand corner](https://admin.zype.com/)
if you have any questions or would like Zype to publish your Roku Channel for you!*


<hr id="3">

## Adding Assets to Your Roku Channel
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

![zype roku app]({{site.url}}assets/Creating an App/roku_info.png)

![zype roku app]({{site.url}}assets/Creating an App/more_roku_info.png)

1. Logo - logo used in the overhang. Suggested size is 125 x 104 pixels HD, 83 x 69 SD, PNG format.

2. Slice - image tiled to create the overhang. Suggested size is 1 x 124 pixels HD and 1 x 83 SD, PNG format.

3. Grid Description Image - image used to contain text on the grid screen. Suggested size is 968 x 258 pixels HD, 502 x 177 pixels SD, PNG format.

4. Grid Border Image - image used for the highlight border on the grid screen. Suggested size is 268 x 190 pixels HD, 158 x 88 pixels SD, PNG format.

5. Info Poster - image used to link to the info page. Suggested size is 266 x 150 pixels HD & SD, PNG format.

6. Search Poster - image used to link to the search page. Suggested size is 266 x 150 pixels HD & SD, PNG format.

<hr id="4">

## Categories, Playlists and Your Roku Channel
We aim to make the development process of a Roku Channel as easy as possible using
our [Zype Roku SDK](https://github.com/zype/zype-roku). To do this, our sample Roku Channel
focuses on three major components of the Zype Platform: playlists, categories, and zobjects.
Since the playlists, categories, and zobjects are being pulled into your Roku channel
using the Zype API, they are all editable using the Zype Platform and do not require
republishing to the Roku Channel Store to make a change.

We will be using screenshots from our sample Roku Channel to highlight what you can do.

![playlists and categories]({{site.url}}assets/Categories, Playlists and Your Roku App/roku_playlist.png)

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

![Zobjects in video detail]({{site.url}}assets/Categories, Playlists and Your Roku App/roku_zobject.png)

You also have the option to provide additional metadata about your videos in the video
detail screen. You select one zobject to be above the description and one zobject to be
below the description. In the example above, we selected the Zobject 'Actor' to be above the description
and it lists the actors that we have associated with the video. Similarly, we selected
the Zobject 'Director' to be below the description.

<hr id='5'>

## Creating an iPhone App from the Zype Platform

TODO
