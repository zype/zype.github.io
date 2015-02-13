---
layout: platform
title: Zype Developer Portal | Platform Docs
permalink: /platform_docs/creating_an_app/
---
##Creating an App Using the Zype Platform
If you're ready to start creating a video app for devices like Roku, Chromecast, Xbox, etc, take a look at the guides below and follow them in order to reach your goal!

<div style="width: 100%;">
  <div style="margin: 20px;">
    <h3>Roku</h3>
    <hr>
  </div>
  <div style="margin: 20px;"> 1)
    <span class="fa fa-file-text" style="margin-right: 4px; margin-left: 10px;"></span>
    <a href="#1">
    Publishing a Roku Channel with Zype</a>
  </div>
  <div style="margin: 20px;"> 2)
    <span class="fa fa-file-text" style="margin-right: 4px; margin-left: 10px;"></span>
    <a href="#2">
    Self Publishing a Roku Channel with Zype</a>
  </div>
  <div style="margin: 20px;">
    <h3>iPhone</h3>
    <hr>
    <div> 1)
      <span class="fa fa-file-text" style="margin-right: 4px; margin-left: 10px;"></span>
      <a href="#3">
      Publishing an iPhone App with Zype</a>
    </div>
  </div>
</div>

<hr id="1">

## Publishing a Roku Channel with Zype

We have simplified the process of publishing a Roku Channel from the Zype Platform.
The process now has three parts. First, you need to set up your channel.
Then, Zype will build your Channel for you or you can
[self-publish your Channel](#2).

**Step 1: Set Up Your Video Library and Channel**

First, you will need to upload and transcode videos onto the Zype Platform.
Currently, Roku Channels only support videos with a Zype video source.

![upload and transcode]({{site.url}}assets/Uploading Videos to the Zype Platform from the Web/upload_video_1.png)

Second, you will need to set up your Roku Channel. Navigate to the Video Apps page

![video apps page]({{site.url}}assets/Publishing Your Roku App/dashboard_to_video_app.png)

Click on Roku to set up a new Roku Channel for publishing

![Roku publishing]({{site.url}}assets/Publishing Your Roku App/set_up_roku_app.png)

Set up your Roku Channel by supplying a title, subtitle, a channel image, and
select a channel template. Zype will create multiple images from your one supplied
channel image including your channel logo, poster art, and loading screen.
It is suggested to have a 640 px by 480 px PNG image because the image will be used
in many different sizes.

![roku set up]({{site.url}}assets/Publishing Your Roku App/set_up_roku_screen.png)

**Step 2: Zype Builds Your Roku Channel**

Once you set up your Channel, Zype will bundle the necessary images and prepare the
code for your Roku Channel. All you have to do is wait a couple of minutes!
The page will automatically refresh once your Channel is ready.

![roku bundling]({{site.url}}assets/Publishing Your Roku App/roku_bundling.png)

**Step 3: Publish Channel**

You can choose to either self-publish or have Zype publish your Roku Channel for you.
If you choose to self publish [click here]({{site.url}}posts/2015/02/13/self-publish-roku/)
to read our guide to self publish your Roku Channel.
If you choose to have Zype publish your channel, you will be sent to a checkout
page to redeem your publishing package or pay for a publishing package.
Once you checkout, a member of the Zype team will package, QA, and submit your
Roku Channel to the Roku Channel Store.

![roku publishing options]({{site.url}}assets/Publishing Your Roku App/roku_publishing.png)

Typically, once your Roku Channel is submitted to the Roku Channel Store, it takes
3-4 weeks to get to the front of the QA queue and then another 1-2 weeks for approval.
You should expect to wait atleast 4-6 weeks for your Roku Channel to be available
on the Roku Channel Store.

**Step 4: Edit Channel Settings**

The majority of settings for your Roku Channel are configured at run-time.
Thus, you can edit Channel settings such as your featured playlist, your logos and
themes without having to re-publish. [Click here]({{site.url}}posts/2015/02/13/roku-advanced-settings/)
to read how to edit your Roku Channel.

<hr id="2">

## Self Publishing a Roku Channel with Zype

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

## Publishing an iPhone App with Zype

REDO
