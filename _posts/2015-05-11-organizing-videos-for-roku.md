---
layout: post
title:  "Organizing your videos for your Roku Channel"
date:   2015-05-11 10:37:55
categories: developers
---

Now that you have set up your Roku Channel and have tested the private channel, you
can organize how the videos are displayed on your Roku Channel. To do this,
you will need to create a featured playlist and a featured category on the Zype Platform. The first row
of your Roku Channel displays your featured playlist while the remaining rows iterate
through your the values in your featured category.

![playlist and categories]({{site.url}}assets/Categories,%20Playlists%20and%20Your%20Roku%20App/roku_playlist.png)

**Create your featured playlist**

To create your featured playlist, navigate to the Playlists dashboard via the lefthand
menu and click on "New Playlist"

![playlist 1]({{site.url}}assets/roku/playlist_1.png)

Then, fill in the information for the playlist. The title will be what appears as the
name of the video row on your Roku Channel. Make sure that you mark the playlist as active.

![playlist 2]({{site.url}}assets/roku/playlist_2.png)

Next, you need to add videos to your playlists. Go to the playlist and click "Add Videos."
Note, Roku can only play videos that are from Zype or Vimeo Pro. If you want this playlist
to play on Roku, you will need to only add videos that have these video sources. You
can order videos in your playlists by dragging the videos.

![playlist 2b]({{site.url}}assets/roku/playlist_2b.png)

Last, search for the videos that you would like to be included in your playlist. You
can search for the videos by title in the search box.

![playlist 3]({{site.url}}assets/roku/playlist_3.png)

Once you have a featured playlist, go to your Roku Channel in the Zype Platform and
click on Edit Advanced Settings. In the "Main Configurations" tab, you can select
the featured playlist. Click save changes.

![category playlist update]({{site.url}}assets/roku/update_channel_playlist.png)


**Create your featured category**

To create your featured category, navigate to the Category dashboard via the lefthand
menu and click on "New Category"

![category 1]({{site.url}}assets/roku/category_1.png)

Then, fill in the information for your category. The values of the category are what get
seen on your Roku. They are displayed in the order that are in the list. Each value
gets its own row on Roku. You can determine whether or not to prepend the category name
to the value in your advanced Roku settings. You can order videos in your category by setting
the episode number.

![category 2]({{site.url}}assets/roku/category_2.png)

Now that you have your category values, you will need to assign these values to each
of your videos. Go to your video and select the metadata tab. Then, check the values
that you want and click save. You can also mass assign categories from the Video Library screen.

![category 3]({{site.url}}assets/roku/category_3.png)

Once you have a featured category, go to your Roku Channel in the Zype Platform and
click on Edit Advanced Settings. In the "Main Configurations" tab, you can select
the featured category, and whether or not to prepend your category name.
Click save changes.

![category playlist update]({{site.url}}assets/roku/update_channel_playlist.png)

Reload your Roku Channel, you should see the first row be your featured playlist and the
remaining rows be the your category values!
