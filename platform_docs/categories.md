---
layout: platform
title: Zype Developer Portal | Platform Docs
permalink: /platform_docs/categories/
---
##All About Categories
The Zype Platform is feature rich, so we want to provide you with a place to learn more about it.
Below are a bunch of short tutorials (with pictures!) to help you with categories.

<div style="width: 100%;">
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
    <a href="#1">
    Categories and Playlists on the Zype Platform</a>
  </div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
    <a href="#2">
    Categories, Playlists and Your Roku App</a>
  </div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
    <a href="#3">
    Search Filters on the Zype Platform</a>
  </div>
</div>

<hr id="1">

## Categories and Playlists on the Zype Platform
As you make your way through the [Zype Platform](http://admin.zype.com), you might have some
questions about the differences between a playlist and a category. At the end of the day, both
are used to return a set of videos, but they aren't exactly the same thing. This blog post
will look at categories and playlists and help you better understand how and when to use them.

### What are playlists and how do I use them?
A playlist on the Zype Platform is a collection of videos that you assemble under a title.
Common playlists might include: Trending Videos, Most Popular, Editor's Choice, etc. Playlists
are great for when you want to create and curate, by hand, a set of videos that might not fall
under a specific category.

### What are categories and how do I use them?
A category on the Zype Platform is a label that you can create and assign to any number of
videos. Common categories for video content might include: Genre, Tag, Type, Season, Series,
etc. Categories are more generic than playlists and can be mass assigned to videos in your
[Video Library.](http://admin.zype.com/videos)

### I'm using the Zype Platform to create a Roku app, what's the difference for me?
Roku apps will treat categories and playlists the same, as they are both just a collection of
videos. For an in-depth guide on how to create your Roku App, make sure you check out [this blog post](http://dev.zype.com/posts/2014/12/03/categories-playlists-zobjects-roku/)


<hr id="2">

## Categories, Playlists and Your Roku App
We aim to make the development process of a Roku Channel as easy as possible using
our [Zype Roku SDK](https://github.com/zype/zype-roku). To do this, our sample Roku Channel
focuses on three major components of the Zype Platform: playlists, categories, and zobjects.
Since the playlists, categories, and zobjects are being pulled into your Roku channel
using the Zype API, they are all editable using the Zype Platform and do not require
republishing to the Roku Channel Store to make a change.

We will be using screenshots from our sample Roku Channel to highlight what you can do.

![playlists and categories](http://i.imgur.com/VVuBjU4.png)

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

![Zobjects in video detail](http://i.imgur.com/gS2W1Em.png)

You also have the option to provide additional metadata about your videos in the video
detail screen. You select one zobject to be above the description and one zobject to be
below the description. In the example above, we selected the Zobject 'Actor' to be above the description
and it lists the actors that we have associated with the video. Similarly, we selected
the Zobject 'Director' to be below the description.


<hr id="3">

## Search Filters on the Zype Platform
If you've been busy adding video content to the [Zype Platform](http://admin.zype.com) and creating playlists, you might be at the point where you've got a few pages of each. To help you better manage your content, we've added a set of filters to the videos and playlists pages:

![video filtering](http://i.imgur.com/BOCwSVG.png)


![playlist filtering](http://i.imgur.com/CVg7VSJ.png)


The filter buttons let you select as many parameters for your search as you'd like. Each button has a dropdown you can use to select a value to search by. The default search options are the categories you've created for your site and "Active" (whether or not the video is marked as active). You can create and manage your categories [here.](https://admin.zype.com/categories)

Once you've selected all of the filters you want to use, click the search button to see the results.

You can search by entering a search term, using the filters or both!

If the filter buttons are greyed out, that's because you don't have any videos or playlists yet.

Check out our previous blog post on [defining categories and playlists](http://dev.zype.com/posts/2014/12/04/defining-categories-and-playlists/), if you have questions about getting started.
