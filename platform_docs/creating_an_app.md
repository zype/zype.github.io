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

REDO


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
