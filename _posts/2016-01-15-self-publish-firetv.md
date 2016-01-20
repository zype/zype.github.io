---
layout: post
title:  "Publishing an Amazon Fire TV on the Zype Platform"
date:   2016-01-15 10:37:55
categories: developers
---

Follow the steps below to setup your Amazon Fire TV app in the Zype Dashboard and submit your app to Amazon. You can also have Zype handle the app submission process.

**Create an Amazon Fire TV Video App on the Zype Dashboard**

1. Go to __Dashboard > Video Apps__.
2. Click __Create An App.__
3. Click __Amazon Fire TV.__
4. Fill out the form and click __Next.__
5. If you’d like to self publish click __I Want To Self-Publish__ and continue the steps below. If you’d like to have Zype handle your publishing click __Publish My App For Me__ and we’ll handle the rest (fees may apply).

**Advanced Settings**

In order to setup your app for Ads, Subscription,  or Purchase you’ll need to edit the Advanced Settings. You can also edit the Colors, add Nested Categories, and make fine tuned adjustments of your header logo.


**Monetization Tab**

* __AVOD (Advertising Video On Demand)__
    - If you have set up [Ad Tags](https://admin.zype.com/ad_tags) for your site and would like to display ads in your AFTV channel toggle the AVOD switch to On.

* __In App Purchasing__
    - __In App Purchasing__ includes Subscription and Purchase for your Amazon app. The purchase is handled through Amazon and happens directly in the app. For more info see https://developer.amazon.com/public/apis/earn/in-app-purchasing.
    - Toggle this switch switch to enable In App Purchasing. If you are using Subscriptions you must Create a [New Plan](https://admin.zype.com/plans) with an Amazon ID in the Zype dashboard. Then, set up In App Purchasing items in the Amazon Dashboard. See the documentation below for more details.


<hr id="subscriptions-zype">
**Add Subscription Plans on Zype**

1. Go to [Dashboard > Plans](https://admin.zype.com/plans).
2. Click __New Plan.__
3. Give the plan a descriptive name. This name will appear in your Amazon Fire TV app.
4. Set the __Amazon ID.__ This id must be unique for your developer account. Be sure to make a note of this Amazon ID as you will need it later when you set up In App Purchasing in your Amazon Developer account. We recommend using a good descriptive id such as __subscriptionMonthly123__ (where 123 is your app id).

**Setup videos for subscription or purchase**

You will need to set your videos to be either subscription or purchase.

1. Go to __Dashboard > Videos > Edit > Video > Monetization Tab__ and
toggle __Subscription Required__ or__ Purchase Required__ as appropriate.

<hr id="submit">
**Submit Your App On The Amazon Developer Console**

* Go to the [Amazon Developer Console](https://developer.amazon.com/home.html)  and login or create an account.
* Click __Add New App.__
* Choose __Mobile Web.__ 

![Mobile Web]({{site.url}}assets/amazon_fire/mobile-web.png)

* Fill out the form and click __Save.__ You must complete every tab in the interface.
* __Availability & Pricing__
    - You can choose here whether you want to charge users to download your app.
* __Description__
    - These descriptions are displayed in the Amazon App Store and help users find your app.
* __Images & Multimedia__
    -  The small and large icons are used to display your app on the home page. This is called the Store Icon in the Zype platform.
    -  For screenshots you will need to run the app locally in a browser and take screenshots. See the README.md in the app package for instructions to run locally, or contact Zype for help.
* __Content Rating__
    - Choose appropriate ratings depending on your app’s content.
* __App File(s)__
    - The app files tab is where you upload your packaged app.
* __Apply Amazon DRM?__
    - Yes.
*  __Select the type of web app you want to submit__
    - You can choose zip and upload the zip we emailed you, or
    -  You can choose URL and provide the URL of the files (you must make them available via http).
    -  For pros/cons of the two approaches see: https://developer.amazon.com/public/solutions/platforms/webapps/docs/differences-between-packaged-and-hosted-apps
* __Web App Features__
    - Check __In-App Purchasing__ (if you are using it).
    - Check __Prevent Sleep for Video Playback.__
* __Device Support.__ Uncheck all items except:
    - Fire TV (2014)
    - Fire TV Stick
    - Fire TV (2015)
* Click __Save.__
* Click In-App Items if you want to set up In App Purchasing (Subscription and Purchase) for your Amazon app. __You will need to set up In App Items with your banking information if you haven’t already.__

**In App Items: Subscriptions**

If you are using Subscriptions with In App Purchasing you must set up each subscription in the Amazon dashboard.

* Click __In-App Items__.
* Click __Add a Subscription__.
* __General Information__
    - __Title:__ 
        + Monthly Subscription (choose an appropriate title).
    - __SKU:__
        + This is the Plan's Amazon ID you set up earlier on the Zype dashboard. (ie __subscriptionMonthly-123__)
        + __Note: You must enter the Amazon ID from the Plan you set up in the Zype platform here. It must match exactly or subscriptions will not work.__
    - __Content delivery:__
        + No additional file required
* __Subscription Periods__
    - __Subscription period:__
        + Choose a subscription period
    - __SKU:__
        + Enter the Amazon ID here, but __repeat it with a dot separator.__
        + For example:   __subscriptionMonthly-123.subscriptionMonthly-123__
        + (Note the dot and the repetition! This is due to the unique way Amazon handle purchase receipts.)
        + If you want to have multiple subscription periods you must set up multiple plans in the Zype platform and repeat the above process. Note that you must create a new subscription each time. Do not add multiple Subscription Periods under the same parent sku.
* The following subscription periods are available for Amazon:
    - Weekly
    - BiWeekly
    - Monthly
    - BiMonthly
    - Quarterly
    - SemiAnnually
    - Annually


**In App Items: Entitlements**

* Click __Add an Entitlement__.
* __General Information__
    - __Title__
        + The title of your video 
    - __SKU__
        + This is the zype id of the video, ie __5629232e4d656c4e94b10000__
        + To find the Video ID in the Zype platform go to __Dashboard > Video Library.__ The __Video ID__ is shown in the Details tab.
    - __Type__
        + Entitlement
    - __Content Delivery__
        + No additional files required


That's it!
