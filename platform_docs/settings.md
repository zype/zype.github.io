---
layout: platform
title: Zype Developer Portal | Platform Docs
permalink: /platform_docs/settings/
---
## Settings Dashboard
You can use the settings dashboard to set your global configurations.

<div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
<a href="#monetization">
Monetization</a>
</div>
<div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
<a href="#player_settings">
Player Settings</a>
</div>
<div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
<a href="#player_branding">
Player Branding</a>
</div>
<div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
<a href="#player_messaging">
Player Messaging</a>
</div>
<div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
<a href="#smtp">
SMTP Settings</a>
</div>

<hr id='monetization'>

## Monetization

To integrate the Zype Platform with your Stripe or Braintree accounts, you need
to enter your account settings from the respective platform. [Click here](https://dashboard.stripe.com/register)
to create a Stripe Account. [Click here](https://www.braintreepayments.com/signup) to
create a Braintree Account. You will need to set up monetization on the Zype Platform
to utilize Zype subscription services.

![monetization]({{site.url}}/assets/settings/monetization.png)

<hr id='player_settings'>

## Player Settings

You can configure settings for your player such as age gating, social sharing,
google analytics tracking, and player expiration.

![player setting]({{site.url}}/assets/settings/player_settings.png)

### Age Gating

If there is an age gate, viewers will have to enter their birthday before viewing.
You can choose to have this for all videos or just for videos that you deem to be
mature content. You can set mature content for each video in the video detail screen.

Below is what age gating looks like:

![mature content]({{site.url}}/assets/settings/age_gate.png)

### Social Sharing

You can toggle social sharing on for your videos. If social sharing is on, viewers
will be able to easily share your video via Facebook, Twitter, or via email.

Below is what social sharing looks like:

![social sharing]({{site.url}}/assets/settings/share_video.png)

### Google Analytics

You can add your Google Analytics tracker. We'll use the tracking object on your web site to deliver impression and completion data. To set up and find your Google Analytics
Tracking Object, [check out Google's documentation](https://support.google.com/analytics/answer/1008080?hl=en).

### Expiration

For security reasons, Zype recommends that the url for the player expires after 300 seconds (5
minutes). You can choose to change this time. If you prefer to not have your player
url expires, you can set expiration to 0.

<hr id='player_branding'>

## Player Branding

You can configure a logo or 'bug' that will appear on videos you've uploaded to the Zype platform.

Navigate to your [settings page](https://admin.zype.com/site/edit) and click on the "Player Branding" tab.

![settings]({{site.url}}/assets/player_logo/settings.png)

![player branding]({{site.url}}/assets/player_logo/player_branding.png)

Click on the upload button to add an image right from your local machine. There are a few recommendations that Zype has regarding the image you upload as the player logo or bug.

1) The image will be scaled to a maximum of 48px by 48px so keep your logo small and not too 'busy'.

2) The image should not be opaque, so that it doesn't block the video content behind it. Zype recommends an opacity of 50%.

![upload]({{site.url}}/assets/player_logo/help.png)

Once you've uploaded an image, use the form to configure how it will be positioned by choosing a position and margins. You can also add a URL to redirect viewers when they click your logo and choose whether or not to hide your logo when other player elements fade out.

![preview]({{site.url}}/assets/player_logo/player_logo.png)

Click the save changes button when complete to test out your new player logo.


![save changes]({{site.url}}/assets/player_logo/save_changes.png)

If you've already uploaded a video to Zype, you can preview it from the video library to see your player logo in action.

![confirm]({{site.url}}/assets/player_logo/confirm.png)

<hr id='player_messaging'>

## Player Messaging
Zype allows you to customize the messages a viewer sees if a video cannot be served
The following are reasons that a video cannot be served:

- Video is still being transcoded
- Video is inactive
- Video has been deleted and the embed still exists
- You restrict the devices where the video can be accessed
- You restrict the countries where the video can be accessed

Zype has supplied smart defaults for each of the above scenarios. You can
use the Settings Dashboard to customize these settings.

![player messaging]({{site.url}}/assets/settings/player_messaging.png)

This is an example of a player message:

![player message example]({{site.url}}/assets/settings/messaging_ex.png)


<hr id='smtp'>

## SMTP Settings
If you are using our Paywall Embed for Subscription, Purchase, or Rental, it is highly recommended that you use your own SMTP service for email delivery.

Using your own SMTP service will allow for more reliable email sending for emails such as purchase/subscription confirmations, password reset emails, and other emails that our Paywall Embed will send on your behalf.

You can use any mail sending service as long as it supports SMTP. If you'd like a recommendation, we suggest [Mailgun](https://www.mailgun.com/).

Please note that the domain name you setup on your mail service should match the domain name of the site you are hosting your Paywall Embeds on.

Once you have signed up for a mail service, you'll need the following SMTP information:

- SMTP Address
- SMTP Port
- SMTP User Name
- SMTP Password

To set these items on Zype go to [Settings](https://admin.zype.com/site/edit) and click the SMTP tab. Enter the settings, then click Save Changes.

![SMTP Settings Example]({{site.url}}/assets/settings/smtp.png)
