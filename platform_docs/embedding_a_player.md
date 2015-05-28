---
layout: platform
title: Zype Developer Portal | Platform Docs
permalink: /platform_docs/embedding_a_player/
---
##Embedding a player on your site
One of the quickest ways to get up and running with Zype videos is to simply drop a player embed code onto your site. Once you've got some videos ready to view, take a look at the guides below.

<div style="width: 100%;">
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
    <a href="#1">
    Embedding a player on your site</a>
  </div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
  <a href="#2">
  Configuring Player Expiration for your site</a>
  </div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
  <a href="#3">
  Enabling Social Sharing Controls for Zype players</a>
  </div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
  <a href="#4">
  Adding a Player Logo</a>
  </div>
</div>

<hr id="1">

## Embedding a player on your site
We're happy to announce that the [Zype Platform](http://admin.zype.com) now grants you the power to "grab and go" with embed codes! Each video that you add to the platform has a snippet of code located under the Embed Code tab. You can navigate to the tab by finding a video that you want to embed and clicking on the edit button. The tab appears along the top of the menu.

![embed code]({{site.url}}assets/Embedding a Player on Your Site2/embed_code.png)

The embed codes are designed to be dropped into a web page, wherever you need them. The div id must remain the same, but other than that, you're free to do as you please. As the page states, we recommend that you include the JavaScript portion of the embed code before the closing body tag on the page.

We hope you use this feature to get up and running with Zype videos on your site in the blink of an eye!

<hr id="2">

## Configuring Player Expiration for your site

One of the ways that Zype defends your video content is by expiring our video URLs after a set amount of time. We let you configure the time before expiration using the [Zype Platform.](http://admin.zype.com).

If you want to edit your Player Expiration value, head over to your Site Settings by clicking on the gear at the top of the screen and clicking on settings.

![site settings]({{site.url}}assets/Embedding a Player on Your Site2/setting.png)

At the bottom of the Site Settings page is a value for Player Expiration, the default is 300 seconds or 5 minutes. You can change this value by typing directly into the box or using the step arrows on the side. The minimum value is 0, which means that your video url's will never expire. The maximum value is 2592000 seconds or one month. Edit the value as needed and click save changes.  

![player expiration]({{site.url}}assets/Embedding a Player on Your Site2/300.png)

That's it! You can confirm by clicking on Site Settings again scrolling to the bottom to see your changes.

<hr id="3">

## Enabling Social Sharing Controls for Zype players

You can enable social sharing to allow viewers to easily share your videos on Facebook and Twitter!

Navigate to your [settings page](https://admin.zype.com/site/edit) and click on the "Player" tab.

![social sharing 1]({{site.url}}assets/social_sharing/social_sharing_1.png)

Then, toggle "Player Sharing Enabled" on towards the button of the page.

![social sharing 2]({{site.url}}assets/social_sharing/social_sharing_2.png)

<hr id="4">

## Adding a Player Logo

You can configure a logo or 'bug' that will appear on videos you've uploaded to the Zype platform.

Navigate to your [settings page](https://admin.zype.com/site/edit) and click on the "Player Branding" tab.

![settings]({{site.url}}assets/player_logo/settings.png)

![player branding]({{site.url}}assets/player_logo/player_branding.png)

Click on the upload button to add an image right from your local machine. There are a few recommendations that we have regarding the image you upload as the player logo or bug.

1) The image will be scaled to a maximum of 48px by 48px so keep your logo small and not too 'busy'.

2) The image should not be opaque, so that it doesn't block the video content behind it. We recommend an opacity of 50%.

![upload]({{site.url}}assets/player_logo/help.png)

Once you've uploaded an image, use the form to configure how it will be positioned by choosing a position and margins. You can also add a URL to redirect viewers when they click your logo and choose whether or not to hide your logo when other player elements fade out.

![preview]({{site.url}}assets/player_logo/player_logo.png)

Click the save changes button when complete to test out your new player logo.


![save changes]({{site.url}}assets/player_logo/save_changes.png)

If you've already uploaded a video to Zype, you can preview it from the video library to see your player logo in action.


![confirm]({{site.url}}assets/player_logo/confirm.png)
