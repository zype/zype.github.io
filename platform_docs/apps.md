---
layout: platform
title: Zype Developer Portal | Platform Docs
permalink: /platform_docs/apps/
redirect_to: https://support.zype.com/hc/en-us/categories/201978548-Applications
---
## Apps
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
    Advanced Settings for Your Roku Channel</a>
  </div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
    <a href="#4">
    Adding Assets to Your Roku Channel</a>
  </div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
    <a href="#5">
    Categories, Playlists and Your Roku Channel</a>
  </div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
    <a href="#6">
    Publishing an iPhone App from the Zype Platform</a>
  </div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
    <a href="#7">
    Deleting an App</a>
  </div>
</div>


<hr id="1">

## Publishing a Roku Channel Through Zype

We have simplified the process of publishing a Roku Channel from the Zype Platform.
The process now has three parts. First, you need to set up your channel.
Then, Zype will build your Channel for you or you can
[self-publish your Channel](#2).

**Step 1: Set Up Your Video Library and Channel**

First, you will need to upload and transcode videos onto the Zype Platform.
Currently, Roku Channels only support videos with a Zype video source.

![upload and transcode]({{site.url}}/assets/Uploading Videos to the Zype Platform from the Web/upload_video_1.png)

Second, you will need to set up your Roku Channel. Navigate to the Video Apps page

![video apps page]({{site.url}}/assets/Publishing Your Roku App/dashboard_to_video_app.png)

Click on Roku to set up a new Roku Channel for publishing

![Roku publishing]({{site.url}}/assets/Publishing Your Roku App/set_up_roku_app.png)

Set up your Roku Channel by supplying a title, subtitle, a channel image, and
select a channel template. Zype will create multiple images from your one supplied
channel image including your channel logo, poster art, and loading screen.
It is suggested to have a 640 px by 480 px PNG image because the image will be used
in many different sizes.

![roku set up]({{site.url}}/assets/Publishing Your Roku App/set_up_roku_screen.png)

**Step 2: Zype Builds Your Roku Channel**

Once you set up your Channel, Zype will bundle the necessary images and prepare the
code for your Roku Channel. All you have to do is wait a couple of minutes!
The page will automatically refresh once your Channel is ready.

![roku bundling]({{site.url}}/assets/Publishing Your Roku App/roku_bundling.png)

**Step 3: Publish Channel**

You can choose to either self-publish or have Zype publish your Roku Channel for you.
If you choose to self publish [click here](#2)
to read our guide to self publish your Roku Channel.
If you choose to have Zype publish your channel, you will be sent to a checkout
page to redeem your publishing package or pay for a publishing package.
Once you checkout, a member of the Zype team will package, QA, and submit your
Roku Channel to the Roku Channel Store.

![roku publishing options]({{site.url}}/assets/Publishing Your Roku App/roku_publishing.png)

Typically, once your Roku Channel is submitted to the Roku Channel Store, it takes
3-4 weeks to get to the front of the QA queue and then another 1-2 weeks for approval.
You should expect to wait atleast 4-6 weeks for your Roku Channel to be available
on the Roku Channel Store. If you would like to immediately share your Roku Channel,
you can create a private Roku Channel that can be shared immediately via url.

**Step 4: Edit Channel Settings**

The majority of settings for your Roku Channel are configured at run-time.
Thus, you can edit Channel settings such as your featured playlist, your logos and
themes without having to re-publish. [Click here](#3)
to read how to edit your Roku Channel.

<hr id="2">

## Self Publishing a Roku Channel Through Zype
Before being ready to self-publish, you will need to set up your Roku Channel on the Zype
Platform. [Click here](#1) to read up on
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

![app.mk replacement]({{site.url}}/assets/Publishing Your Roku App/replace_appmk_vars.png))

Then, run make install inside the Roku Channel directory in your terminal to side load your Roku Channel to your Roku device.

![make install]({{site.url}}/assets/Publishing Your Roku App/make_install.png))

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
Publishing Queue for Roku QA. Based on high demand, it can take anywhere from 2 to 3 months to
get approved by Roku into the Roku Channel Store.

Click [here](https://owner.roku.com/Developer/Apps) to submit your Roku Channel!
You will have to be logged into your Roku Developer Account.

*Please feel free to reach out to Zype using the question box [in the lower left hand corner](https://admin.zype.com/)
if you have any questions or would like Zype to publish your Roku Channel for you!*


<hr id="3">

## Advanced Settings for Your Roku Channel

Selecting a Channel Template and uploading a Channel Image takes most of the hard
work out of branding your Roku Channel. However, if you want to further specialize
your Roku Channel, you can click on Edit Advanced Settings for your Roku Channel.

![advanced settings btn]({{site.url}}/assets/Publishing Your Roku App/roku_advanced_settings_btn.png)

The Advanced Settings have a lot of options! The highest impact advanced settings
that you can change are in the Main Configurations Tab and the Image Configurations Tab.

In particular, in the Main Configurations, you can change which playlist is to
be featured at the top of your Roku Channel and you can change the category to
iterate through for the rest of your Roku Channel.

![main configs]({{site.url}}/assets/Publishing Your Roku App/main_configs.png)

In the Image Configurations, you can change the run time images such as your logo, slice images,
and grid images. These images are grabbed through the Zype API each time your Roku
Channel gets loaded, so you can upload a new image and refresh your Roku Channel to see
it being changed in real time.

![image configs]({{site.url}}/assets/Publishing Your Roku App/image_configs.png)

You can also change your Channel Build Details. Note, however, that if you change
images in your Channel Build Details like your store or focus image, you will
need to resubmit your Channel to the Roku Channel Store.
If you have not yet submitted your Roku Channel, you will need to grab a new bundle of your Roku Channel.

![image configs]({{site.url}}/assets/Publishing Your Roku App/build_configs.png)

<hr id='4'>

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

![zype roku app]({{site.url}}/assets/Creating an App/roku_info.png)

![zype roku app]({{site.url}}/assets/Creating an App/more_roku_info.png)

1. Logo - logo used in the overhang. Suggested size is 125 x 104 pixels HD, 83 x 69 SD, PNG format.

2. Slice - image tiled to create the overhang. Suggested size is 1 x 124 pixels HD and 1 x 83 SD, PNG format.

3. Grid Description Image - image used to contain text on the grid screen. Suggested size is 968 x 258 pixels HD, 502 x 177 pixels SD, PNG format.

4. Grid Border Image - image used for the highlight border on the grid screen. Suggested size is 268 x 190 pixels HD, 158 x 88 pixels SD, PNG format.

5. Info Poster - image used to link to the info page. Suggested size is 266 x 150 pixels HD & SD, PNG format.

6. Search Poster - image used to link to the search page. Suggested size is 266 x 150 pixels HD & SD, PNG format.

<hr id="5">

## Categories, Playlists and Your Roku Channel
We aim to make the development process of a Roku Channel as easy as possible using
our [Zype Roku SDK](https://github.com/zype/zype-roku). To do this, our sample Roku Channel
focuses on three major components of the Zype Platform: playlists, categories, and zobjects.
Since the playlists, categories, and zobjects are being pulled into your Roku channel
using the Zype API, they are all editable using the Zype Platform and do not require
republishing to the Roku Channel Store to make a change.

We will be using screenshots from our sample Roku Channel to highlight what you can do.

![playlists and categories]({{site.url}}/assets/Categories, Playlists and Your Roku App/roku_playlist.png)

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

![Zobjects in video detail]({{site.url}}/assets/Categories, Playlists and Your Roku App/roku_zobject.png)

You also have the option to provide additional metadata about your videos in the video
detail screen. You select one zobject to be above the description and one zobject to be
below the description. In the example above, we selected the Zobject 'Actor' to be above the description
and it lists the actors that we have associated with the video. Similarly, we selected
the Zobject 'Director' to be below the description.

<hr id='6'>

## Publishing an iPhone App from the Zype Platform

Before we start, lets look at what the end result of what your iPhone App will look like!

![iphone preview]({{site.url}}/assets/iphone/mockup.png)

To configure your iPhone App using the Zype Platform, navigate to the Video Apps page and click
on the iPhone logo.

![select iphone]({{site.url}}/assets/iphone/apps_screen.png)

Next, fill in the App Details. This includes the title, the version number, and the store icon.
The store icon will be the icon that users click to on your iPhone screen to enter your app.

![app details]({{site.url}}/assets/iphone/app_details_screen.png)

Then, fill out the Channel Information. The banner image is what appears at the top of your home
screen. The larger banner is for higher quality displays. Check out the mock up of an iPhone App
below to see where the banner gets displayed in the home screen.

![channel screen]({{site.url}}/assets/iphone/channel_screen.png)

![banner display]({{site.url}}/assets/iphone/mockup-help.png)

Next, add tiles. Tiles are what a user can click on in the app’s home screen to go to the appropriate page. An iPhone app can have up to 9 tiles.
Tiles can include links to Twitter, Facebook, Google+, your blog, your personal website,
favorites, videos, and messages. You can drag the tiles in the editor to change their order on
the iPhone Screen. Check out the mock up to see where the tiles get displayed.

![tile screen]({{site.url}}/assets/iphone/tiles_screen.png)

![tiles display]({{site.url}}/assets/iphone/mockup-help.png)

If you would like to add a message to your users at this time, you can click on the Message tab
and add a message.

![message screen]({{site.url}}/assets/iphone/message_screen.png)

Once you are finished, click save changes. You will be redirected to the iPhone App details
screen where you will see a mock up of your channel home screen. You can either
use Zype's [API documentation]({{site.url}}/api_docs/apps) to self-publish or have Zype publish
for you!

![iphone preview]({{site.url}}/assets/iphone/iphone_show.png)

<hr id='7'>

## Deleting an App

To delete an app from the Zype Platform, navigate to your [video apps](https://admin.zype.com/apps)
and click on the app that you want to delete.

![delete app 1]({{site.url}}/assets/apps/delete_1.png)

Then, click on the delete button in the upper right hand corner.

![delete app 2]({{site.url}}/assets/apps/delete_2.png)
