---
layout: platform
title: Zype Developer Portal | Platform Docs
permalink: /platform_docs/purchase_and_rental/
---
# Purchase and Rental
Purchase & Rental allows you to make money from your videos by selling or renting them to your consumers. The Zype Platform supports Stripe and Braintree for credit card processing of transactions. You can also use the Zype Transaction API to extend the functionality listed here. Contact us for more info.

<div style="width: 100%;">
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
    <a href="#setup">Setting Up Purchase & Rental</a>
  </div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
    <a href="#enabling">Enabling Purchase & Rental on Videos</a>
  </div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
    <a href="#publishing">Publishing Your Videos</a>
  </div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
    <a href="#overriding">Overriding the subscription embed</a>
  </div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
    <a href="#managing">Managing Your Purchase/Rental Settings & Consumers</a>
  </div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
    <a href="#analytics">Purchase & Rental Analytics</a>
  </div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
    <a href="#purchase_rental_settings">Purchase & Rental Settings</a>
  </div>
</div>

<hr id="setup">
## Setting Up Purchase & Rental
To get started using Purchase & Rental with Zype, login to your account and click on ‘Monetization’ in the sidebar.

Click ‘Enable Purchase & Rental’ and follow the prompts to get everything set up.

![stripe settings]({{site.url}}/assets/purchase_and_rental_setup/monetization.png)

Your subscription payments can be processed by Stripe or Braintree so you’ll need a Stripe or Braintree account to complete this process.

**Stripe:** [Click here](https://dashboard.stripe.com/register) to sign up for a Stripe account or [click here](https://dashboard.stripe.com/account/apikeys) to sign in and get your Stripe API Keys.

**Braintree:** [Click here](https://www.braintreepayments.com/signup) to sign up for a Braintree account or [click here](https://www.braintreegateway.com/login) to sign in and get your Braintree API Keys.

Once you’ve completed setting up your account, you’ll either be shown an example embed code for the first video you added or a prompt to add videos if you haven’t done that already.

When you return to the Monetization page, you’ll now see a breakdown of your purchases, rentals, consumers, and plans. Click on any one of these to find out more about your Purchase & Rental business through Zype.

<hr id="enabling">
## Enabling Purchase & Rental on Videos

After you’ve set up your Stripe or Braintree info and completed the Purchase & Rental Setup Wizard from the previous step, you will be prompted to turn “purchase” or “rental” on for all of your videos. To manage these settings on each video, go to the “Video Library” in the sidebar nav and then go to the Edit Video section by clicking on the video you want to edit. Once in the Edit Video screen, click on the “Monetization” tab.

![monetization tab]({{site.url}}/assets/purchase_and_rental_setup/monetization-tab.png)

Once you click the monetization tab, you can edit the settings for your video. You can only enable one type of monetization per video at any given time. For example, if you enable subscription then you cannot enable purchase or rental and vice versa. This screen also lets you set the purchase or rental price for the individual video as well as setting the rental duration.

![monetization tab detail]({{site.url}}/assets/purchase_and_rental_setup/monetization-tab-detail.png)

<hr id="publishing">
## Publishing Your Videos

To publish your videos on your website, simply grab the embed code from the “Embed” tab of the Edit Video screen from the previous step and paste it into your web site code:

Make sure the “Paywall” toggle is set to “ON” to enable the purchase, rental, or subscription paywalls in the player.

![embed code]({{site.url}}/assets/purchase_and_rental_setup/embed-code.png)

<hr id="overriding">
## Overriding the subscription embed

You are able to override the default embed settings on a per embed basis using JavaScript. For example, when you copy your embed code, you can add additional JS inside your script tag.

<table>
  <tr>
    <th>Variable</th>
    <th>Example</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>backgroundColor</td>
    <td>zype.backgroundColor = ‘#264547’;</td>
    <td>Hexcolor of background if no video thumbnail</td>
  </tr>
  <tr>
    <td>autoPlay</td>
    <td>zype.autoPlay = true;</td>
    <td>Whether or not videos should autoplay</td>
  </tr>
  <tr>
    <td>appName</td>
    <td>zype.appName = ‘My app name’;</td>
    <td>Name of your app</td>
  </tr>
  <tr>
    <td>showZype</td>
    <td>zype.showZype = true;</td>
    <td>Whether or not to show “Powered by Zype”</td>
  </tr>
  <tr>
    <td>couponsEnabled</td>
    <td>zype.couponsEnabled = true</td>
    <td>Whether or not to have the coupon code field on new subscription sign ups</td>
  </tr>
</table>

<hr id="managing">
## Managing Your Purchase/Rental Settings & Consumers

You can update your Purchase & Rental settings, view your consumers, or each individual transaction.

![manage purchase]({{site.url}}/assets/purchase_and_rental_setup/manage-purchase.png)

Click on “Manage Purchase & Rental Settings” to edit the default settings for your video business.

![edit purchase]({{site.url}}/assets/purchase_and_rental_setup/edit-purchase.png)

Click on “Consumers” to see a list of consumers that have purchased or rented your content. You can then easily edit the details or an individual consumer and see their unique activity:

![consumer details]({{site.url}}/assets/purchase_and_rental_setup/consumer-details.png)

Click “Transactions” to see a list of all your transactions:

![transactions]({{site.url}}/assets/purchase_and_rental_setup/transactions.jpg)

<hr id="analytics">
## Purchase & Rental Analytics

You can track how much revenue you’re generating easily on the Zype Platform. Just go to the Analytics section in the navbar and see your total monthly revenue, number of consumers, and engagement by video.

![analytics]({{site.url}}/assets/purchase_and_rental_setup/analytics.png)

<hr id="purchase_rental_settings">

## Purchase & Rental Settings

In order to manage your Purchase & Rental settings:

- In the nav on the left, click <b>Make Money</b>.
- Click the <b>Manage Purchase & Rental Settings</b> button.

![settings]({{site.url}}/assets/purchase_and_rental_setup/settings.png)

### Logo

This logo will be displayed when users are interacting with your subscription service.

### Email

The email that messages to your customers will be sent from.

### Terms of Service

If you have a TOS that users must agree to before subscribing, add a link to it here.

### Show Zype Branding

By default we display a Zype logo at the bottom of your subscription embeds. To hide it, switch off this setting.

![Powered by Zype]({{site.url}}/assets/Connecting Stripe/powered-by-zype.jpg)

### Default Purchase Price

The default price you'd like your videos to be purchased for.

### Default Rental Price

The default price you'd like your videos to be rented for.

### Default Rental Duration (Days)

The default length of time a rental for this video is valid for.
