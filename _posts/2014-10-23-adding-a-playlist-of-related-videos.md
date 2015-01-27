---
layout: post
title:  "Adding a playlist of related videos"
date:   2014-10-23 06:37:55
categories: videos
---
Let's say you've already got some video content on your zype destination site, but now you'd like to recommend
additional content based on what your users are watching. The solution we've implemented is called related videos.
In this post, we'll be covering how to create a playlist of related videos that are recommended to a viewer
based on what the video they're watching. Here's an example of the finished product:

![related playlist](http://i.imgur.com/wPXZ772.png)

*The related videos section is automatically created for each video on your site, but if you'd like to be more
specific about which videos are displayed there, follow along as we set up a playlist of related videos.*

### How do I set up a playlist of related videos?

Setting up the playlist can be done from the [admin portal](http://admin.zype.com/). Navigate to the playlist
section on the sidebar and and click "New Playlist". Follow through the menu and create a playlist (make sure it's active!).

![playlist navigation](http://i.imgur.com/oXi3Dlg.png)

### How can I choose which videos are shown in the playlist?

This is an easy one. Use the "Add Videos" button to select which videos will appear under the related videos section.

![add videos navigation](http://i.imgur.com/hMAkhgQ.png)

### How can I choose which videos display the playlist?

Choosing the videos that will have your playlist displayed is done through the playlist edit screen. You can get there
quickly by clicking on the name of your playlist here:

![edit your playlist](http://i.imgur.com/XSvwXVR.png)

Use our multiselector to search for the videos you want and click on them to move them into selected videos.
Click "Save Changes" when you're done.

![choose related videos](http://i.imgur.com/WRtRv8m.png)

### Let's confirm

You should take a second and make sure everything's going according to plan. Go to your site and view a video
that you added to selected videos in the previous step. Below the video, under the section "Related Videos",
you should see the playlist you just created and the first few videos you added. You can also update any of your
current playlists to act as a playlist of related videos by following these same steps.


*Check our [previous post](http://dev.zype.com/posts/2014/10/10/adding-zype-to-rails/)
on how to set up your Rails App with the Zype Gem!*
