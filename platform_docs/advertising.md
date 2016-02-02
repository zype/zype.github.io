---
layout: platform
title: Zype Developer Portal | Platform Docs
permalink: /platform_docs/advertising/
---


## Getting Started with Advertising in Zype

Zype empowers you to build and make money from branded streaming destinations. It’s easy to start earning revenue from your videos with the Zype platform.
In this guide, we’ll provide an overview of in-video display advertising so you can start monetizing your video views. Zype supports any VAST/VPAID standards-based ad display solution, including Google IMA. Today, we’ll be setting you up with Google Adsense and DoubleClick for Publishers (DFP) and showing you how to create your first ad unit to display through the Zype player.


### Background
The online video ad ecosystem consists of multiple layers. The players involved are advertisers, ad networks such as AdSense who distribute ads, and ad servers such as DFP who allow you to host ads on your properties and choose which ads to display based on rules you set. These ads are ultimately embedded in your video player through VAST and/or VPAID tags, which pass information about the ads to display to the player - the equivalent of the embed code to place a video player on your website.

![The video display advertising ecosystem]({{site.url}}/assets/advertising.png)

The video display advertising ecosystem
In DFP, every space in which you display an advertisement is called an ‘ad unit’. Zype allows you to create an ad unit within your Zype video player to display ads, whether from DFP or another ad server. You may use any ad server or network that supports VAST/VPAID standards to show your ads through Zype, but for the purposes of this guide, we’ll be setting you up with AdSense to load ads and DFP to serve them in your video players.


### Setting Up Google AdSense and DFP
If you do not already have a Google AdSense account, you will need to [apply for one](http://www.google.com/adsense/start/) now. Follow the instructions in the application to enable AdSense on your Google account. Save your AdSense property code - we’ll need it soon.
Once you have Google AdSense set up, you will need to [enable your account](https://www.google.com/doubleclick/publishers/welcome/) for DFP access. DFP allows you to serve ads from multiple sources, including AdSense, other competing ad networks, as well as your own content. This could be material you create to promote your own content, or ads you sell directly to partners outside of third-party networks. Check out Google’s [DFP overview](https://support.google.com/dfp_premium/answer/6021030) for more information on how it works.


### Creating an Ad Unit to Display Video Ads
Once you’re in DFP, the first thing we need to do is add your Zype player as a new ad unit in your inventory.   [Click here](https://support.google.com/dfp_premium/answer/177203) for instructions on creating a new ad unit - we’ll use the first method, defining a new ad unit in DoubleClick for Publishers before adding them to ad tags.
Zype gives you the option to either (1) use a single ad unit for video players on all devices, or (2) use different ad units on different devices. For example, online web, mobile, and set-top players could each be different ad units with different settings for target, types of ads, and length/size of ads. If you would like to use multiple ad units, simply create as many as you need (up to 3, for the devices listed above).


### Delivering Ads to Your Ad Units
Now that we have added your Zype player to your ad unit inventory, we can go ahead and set it up to display ads. We’ll be creating a new ‘order’ for AdSense ads to be delivered to your ad unit. See the following description from Google on the components of DFP ad campaigns:


In DFP, orders contain line items, and line items contain creatives. An order is a representation in DFP of an agreement with an advertiser. It has start and end dates, and it can contain one or more line items.


A **line item** holds information about the specific run dates, targeting, and pricing of one or a set of creatives that will be delivered, including which ad units and placements are targeted. Every line item is contained within an order.


A **creative** is a specific advertisement, such as an image file, a video file, or other content. It's what gets delivered to users. To be delivered, a creative must be associated with a line item. One creative can be associated with more than one line item.


Now, we’ll connect your DFP account with your AdSense account and then create an campaign to deliver AdSense ads to your new ad unit. [Click here](https://support.google.com/dfp_premium/answer/1734048) for detailed instructions from Google on how to complete these steps.
At this point, you can also [add other types of campaign line items or orders](https://support.google.com/dfp_premium/answer/1047444) to deliver through your ad units. For example, if you contract directly with companies to display their advertisements, you can import them for display. You can also display “house” ads - your own content to display if there is no paying content available to show. DFP allows you to set various priorities on these items so you can control where and when they are shown. More information about delivery priority options can be found in [this article](https://support.google.com/dfp_premium/answer/177279).



### Adding Your Ad Tags to Zype
Finally, we’ll need to embed your newly created ad unit into your Zype player. Follow [these instructions](https://support.google.com/dfp_premium/answer/1181016) to generate video ad tags (VAST tags) for the ad unit(s) you created. Then, head to the Zype Dashboard and go to the Make Money page. Under Advertising, click Submit Ad Tags and follow the prompts to give Zype the tags to embed in your video players.
That’s it! Now you’ll be on your way to making money from your video content, no coding or development experience needed. If you need any help with setting up advertising with AdSense/DFP and Zype, check out the [DFP documentation](https://support.google.com/dfp_premium#topic=28132) or contact our team through the blue help icon on the bottom right of the Zype Dashboard.
