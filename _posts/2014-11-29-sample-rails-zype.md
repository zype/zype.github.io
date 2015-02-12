---
layout: post
title:  "Sample Rails App using the Zype Platform and API"
date:   2014-11-29 12:37:55
categories: developers
---

We want to make the Zype Platform accessible to as many types of developers as possible. To do this,
we have provided [API documentation](http://dev.zype.com/api_docs/intro/) and are happy
to <a href='mailto:contact@zypemedia.com'>talk with you</a> about creating a turnkey app.

As a developer, I always like to learn by example, so we have created
a template Rails app to show you what you can do with the Zype Platform using our Ruby Gem and also provide you with a starter template if you want to build off of it for your own web app.

We intentionally kept the styling simple and used [Bootstrap](http://getbootstrap.com/) if
you would like to use this example as a foundation to your Rails app.
Feel free to clone the repo [here](https://github.com/zype/zype-rails). You will
need your Zype API and Player Keys from the Zype Platform. The README has directions
to how you can find your keys.

*The Zype Rails Sample App has the following pages and features.*

**Home Page**

The homepage includes all of your playlists, a link in the header to view all videos,
and a search box to search for a specific video. The Playlists can be configured
in the Zype Platform and can be fetched via the Ruby Gem.

![homepage]({{site.url}}assets/Walkthrough of the Zype API with a Sample Rails App/home.png)

**Playlist Page**

You can click on any playlist to view all the videos that belong to that playlist. You can sort
the videos based on release date, name, or popularity. Also note that there are Zype Videos
and YouTube videos in the same player. The Zype Platform and Zype API allows you to
seamlessly combine the two.

![playlist page]({{site.url}}assets/Walkthrough of the Zype API with a Sample Rails App/playlist.png)


**Browse all Videos**

The browse all videos uses the Ruby Gem to query the Zype API to get all the videos.
When you hover over a video, you will see the description. Feel free to read the [Video API Documentation](http://dev.zype.com/api_docs/videos/) to see what other information
gtes returned when you query for the videos.

![browse videos]({{site.url}}assets/Walkthrough of the Zype API with a Sample Rails App/browse.png)

**Video Page**

When you click on a video's thumbnail, you get directed to the video's page. The video's page
contains the title, description, and video player. The Zype API will deliver the appropriate
player based on where the video source comes from and what Player Rules you set.

![video page]({{site.url}}assets/Walkthrough of the Zype API with a Sample Rails App/video.png)

Have questions about implementing our sample Rails app or want to see examples of
other features or in other languages? Feel free to comment below!
