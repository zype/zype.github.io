---
layout: platform
title: Zype Developer Portal | Platform Docs
permalink: /platform_docs/assets/
redirect_to: https://support.zype.com/hc/en-us/articles/360006539093
---

## Assets

<div style="width: 100%;">
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
    <a href="#1">
    Adding Assets to Your Roku App</a>
  </div>
</div>

<hr id="1">

## Adding assets to Your Roku app
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

These assets get loaded via a call to the Zype API every time the Roku Channel gets loaded.

![zype roku app]({{site.url}}/assets/Assets/roku1.png)

![zype roku app]({{site.url}}/assets/Assets/roku2.png)

1. Logo - logo used in the overhang. Suggested size is 125 x 104 pixels HD, 83 x 69 SD, PNG format.

2. Slice - image tiled to create the overhang. Suggested size is 1 x 124 pixels HD and 1 x 83 SD, PNG format.

3. Grid Description Image - image used to contain text on the grid screen. Suggested size is 968 x 258 pixels HD, 502 x 177 pixels SD, PNG format.

4. Grid Border Image - image used for the highlight border on the grid screen. Suggested size is 268 x 190 pixels HD, 158 x 88 pixels SD, PNG format.

5. Info Poster - image used to link to the info page. Suggested size is 266 x 150 pixels HD & SD, PNG format.

6. Search Poster - image used to link to the search page. Suggested size is 266 x 150 pixels HD & SD, PNG format.
