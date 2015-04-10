---
layout: platform
title: Zype Developer Portal | Platform Docs
permalink: /platform_docs/videos/
---
## Videos
Videos are at the core of the Zype experience. You can upload videos or import videos
from a third party source and use Zype to deliver your video content to any device or
geographic location desired.

<div style="width: 100%;">
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
    <a href="#1">
    Learn about Dynamic Player Technology (DPT)</a>
  </div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
    <a href="#2">
    Monitoring your views</a>
  </div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
    <a href="#3">
    Related playlists</a>
  </div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
    <a href="#4">
    Uploading videos to the Zype Platform</a>
  </div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>  
  <a href="#5">
  Importing videos to your Video Library from a third party source</a>
  </div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>  
  <a href="#6">
  Adding a collection of videos from Vimeo</a>
  </div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>  
  <a href="#7">
  Adding single videos from a Vimeo link</a>
  </div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
    <a href="#8">
    Adding videos from a YouTube Channel to the Zype Platform</a>
  </div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
  <a href="#9">
  Adding YouTube videos from a URL</a>
  </div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
    <a href="#10">
    Adding your Crunchyroll videos to Zype</a>
  </div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
    <a href="#11">
    Bulk importing of third party video sources (Advanced)</a>
  </div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
    <a href="#12">
    Uploading videos to Zype using our Ruby Gem</a>
  </div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
    <a href="#13">
    Walkthrough of the Zype API with a sample Rails app</a>
  </div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
    <a href="#14">
    Embedding a player on your site</a>
  </div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
    <a href="#15">
    Search filters on the Zype Platform</a>
  </div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
    <a href="#16">
    Choosing thumbnails for your videos</a>
  </div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
    <a href="#17">
    Deleting a video</a>
  </div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
    <a href="#18">
    Upload formats</a>
  </div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
    <a href="#19">
    Managing video segments</a>
  </div>
</div>

<hr id="1">

## Learn about Dynamic Player Technology (DPT)
Zype’s DPT allows you to create player rules based on geography and device.
For example, you could declare that end users will receive the Hulu Player if he
or she is accessing your video via desktop in the United States or the Zype Player
if he or she is accessing your video via desktop in Australia.

### What you need to start

You will need to have a video collection on the Zype Platform from the video sources
that you want to create player rules for.

1\. Make sure you have imported your videos into your [video catalogue](https://admin.zype.com/video_imports)
on the Zype Platform.

![video imports]({{site.url}}assets/DPT/add_videos.png)


### What you need to do in the Zype Platform

1\. Visit the [Player Rule Page](https://admin.zype.com/player_rules) and click on New Player Rule

![player rules]({{site.url}}assets/DPT/player_rule.png)

2\. Complete the Player Rules form. You will need to know the countries and devices you want for your rule.
Based on countries and devices, you will be given player options that can be served to the end user.

![player rule form]({{site.url}}assets/DPT/player_rule_form.png)

### Using the API

You can query the Zype API to only show videos that dynamically conform to your DPT rules
given an end user's device and geolocation. Set dpt to equal true in your GET request.

<pre><code> GET - https://api.zype.com/videos?dpt=true
</code></pre>

### Using the Player API

1\. Once you have set up your video catalog in the Zype Platform and you have created your player rules, you are ready to use the Zype Player API!

2\. You can find your player key and API key using the [Zype Platform](https://admin.zype.com/site/api)

![site keys]({{site.url}}assets/API/site_key.png)

3a\. To make the API call to get the appropriate player
{% highlight ruby %}
GET http://api.zype.com/videos/{video_id}/player/?api_key={api_key}&player_key={player_key}
{% endhighlight %}

3b\. To use the [Zype Ruby Gem](https://github.com/edla/zype-cli) to get the appropriate player
{% highlight ruby %}
@zype_cli = Zype::Client.new
@video = @zype_cli.videos.find(params[:video_id])
@player = @video.player(player_key: params[:player_key])
{% endhighlight %}

*Check our [previous post](http://dev.zype.com/posts/2014/10/10/adding-zype-to-rails/)
on how to set up your Rails app with the Zype Gem!*

<hr id="2">

## Monitoring your views
In a previous post, we covered how to use Zype’s Dynamic Player Technology (DPT).
In this post, we'll be covering how to use the DPT logs to see what requests are being made for your video content.
For example, let's say you've uploaded a batch of new videos and after the first 30 days, you'd like to get an idea
of who's viewing your content and what times of the day are most popular for viewing.

### Where can I find my logs?

After you've uploaded some video content to the Zype platform, log in through the [admin portal](http://admin.zype.com/)
and navigate to the logs section under the settings dropdown menu. In this post, we'll cover the request logs,
so feel free to click on that link once you see the logs menu.  

![dpt logs navigation]({{site.url}}assets/Monitoring Your Views/log_navigation_1.png)

### What type of information can I see in my request logs?

The request logs screen shows you lots of information about the requests made to view your videos.
Here are the most pertinent pieces of information:

Data | Description
---- | -----------
Video	| The video that was requested
IP Address | The IP address of the requester
Country | The country the request was made from
Device	| The device the request was made from
Player	| The player that served the video
Provider | The provider of the content
Revenue Model	| The revenue model of the viewer
Status	| The status of the request
Created | The date and time the request was created

![dpt logs]({{site.url}}assets/Monitoring Your Views/request_logs.png)

### How can I search the request logs data?

The request logs screen gives you a snapshot of the most recent requests by default.

Sorting the request logs is easy: use the four dropdown menus to select your search parameters
and then click on the search button.


![searching logs]({{site.url}}assets/Monitoring Your Views/request_log_search_3.png)


*Check our [previous post](http://dev.zype.com/posts/2014/10/10/adding-zype-to-rails/)
on how to set up your Rails app with the Zype Gem!*

<hr id="3">

## Related playlists
Let's say you've already got some video content on your Zype destination site, but now you'd like to recommend
additional content based on what your users are watching. The solution we've implemented is called related videos.
In this post, we'll be covering how to create a playlist of related videos that are recommended to a viewer
based on what the video they're watching. Here's an example of the finished product:

![related playlist]({{site.url}}assets/Related Playlists/related_playlists.png)

*The related videos section is automatically created for each video on your site, but if you'd like to be more
specific about which videos are displayed there, follow along as we set up a playlist of related videos.*

### How do I set up a playlist of related videos?

Setting up the playlist can be done from the [admin portal](http://admin.zype.com/). Navigate to the playlist
section on the sidebar and and click "New Playlist". Follow through the menu and create a playlist (make sure it's active!).

![playlist navigation]({{site.url}}assets/Related Playlists/playlist_navigation_2.png)

### How can I choose which videos are shown in the playlist?

This is an easy one. Use the "Add Videos" button to select which videos will appear under the related videos section.

![add videos navigation]({{site.url}}assets/Related Playlists/add_videos_playlist_3.png)

### How can I choose which videos display the playlist?

Choosing the videos that will have your playlist displayed is done through the playlist edit screen. You can get there
quickly by clicking on the name of your playlist here:

![edit your playlist]({{site.url}}assets/Related Playlists/save_your_playlist_4.png)

Use our multiselector to search for the videos you want and click on them to move them into selected videos.
Click "Save Changes" when you're done.

![choose related videos]({{site.url}}assets/Related Playlists/choose_related_videos_5.png)

### Let's confirm

You should take a second and make sure everything is going according to plan. Go to your site and view a video
that you added to selected videos in the previous step. Below the video, under the section "Related Videos",
you should see the playlist you just created and the first few videos you added. You can also update any of your
current playlists to act as a playlist of related videos by following these same steps.


*Check our [previous post](http://dev.zype.com/posts/2014/10/10/adding-zype-to-rails/)
on how to set up your Rails app with the Zype Gem!*

<hr id="4">

## Uploading videos to the Zype Platform from the web

The easiest way to add a video to your video library is to upload a video to the Zype Platform.

We support many popular media formats such as: 3GP, AAC, AVI, FLV, MP4 and MPEG-2.
We do not currently support Apple ProRes, ARRI and RED.

**Step 1:**

Go to Import & Upload, and click the "Upload from My Web Browser" button.

![Upload Videos]({{ site.url }}/assets/Uploading Videos to the Zype Platform from the Web/upload_web_browser.png)

**Step 2:**

By default, we automatically add the video to your library and we activate the video. If you would
like to change this, toggle Add Video or Activate Video off. Then, select the file that you want to upload.

![upload video]({{ site.url }}/assets/Uploading Videos to the Zype Platform from the Web/upload_video_options.png)

**Step 3:**

When the file is finished uploading, you will be redirected to the video's page where you
can add additional metadata. Once your video is finished [transcoding](http://en.wikipedia.org/wiki/Transcoding), you will
be able to play your video and select your video thumbnail.

![add video metadata]({{ site.url }}/assets/Uploading Videos to the Zype Platform from the Web/add_metadata_to_video.png)

<hr id='5'>

## Importing videos from a third party source

We’ve made it easier to import your videos from third party sources like YouTube, Vimeo, or Hulu
to your video library! Now, the default option is to automatically add all video imports to your
video library as new videos.


**Step 1: Add your video source and make sure that add videos is turned on**

![add video source]({{site.url}}assets/video_sources/add_source.png)

**Step 2: Navigate to your Video Library, you should see new videos from your video source that
are active! Note, videos will be added to your video library as they become available**

![video library]({{site.url}}assets/video_sources/video_library.png)

**Advanced importing**

If you do not want to automatically import all of the videos from a video source to your video
library or if you want to merge your video imports to videos preexisting in your library, you can
turn add video ‘off’ when you create a video source and use the “Advanced Video Importing”
option.

![add video source not-auto]({{site.url}}assets/video_sources/add_source_not_auto.png)

Then, navigate to the video imports screen and click on the add button for the videos that you
want to add to your video library or the merge button if you want to merge your video imports to
preexisting videos in your video library.

![advanced video importing]({{site.url}}assets/video_sources/advanced_video_imports.png)

<hr id="6">

## Adding videos from a Vimeo Channel, Group or User
We're happy to provide you with a simple and powerful for importing your Vimeo videos to the Zype Platform. Below are the steps for grabbing your videos, no matter where they exist in Vimeo.

**Step 1:**

Go to Video Sources and click on the Vimeo icon.

![click vimeo]({{site.url}}assets/Adding Videos from a Vimeo Channel, Group or User/click_vimeo.png)

**Step 2:**

Enter a name for your Vimeo video source (something to help you remember it!).

**Step 3:**

You'll need to copy and paste a link to your Vimeo videos from a Group, Channel or User. Here are some quick example links:

<pre><code>https://vimeo.com/channels/staffpicks

https://vimeo.com/user36554072/videos

https://vimeo.com/groups/animation
</code></pre>

First, go to Vimeo and copy the link:

![copy your link]({{site.url}}assets/Adding Videos from a Vimeo Channel, Group or User/vimeo_copy.png)

Then paste the link into the Vimeo Source form:

![paste your link]({{site.url}}assets/Adding Videos from a Vimeo Channel, Group or User/paste_your_link.png)

Then click the 'Save Changes' button.


**Step 4:**

If everything went according to plan, you can see your new video imports by clicking on the green 'Video Imports' button.

![video imports button]({{site.url}}assets/Adding Videos from a Vimeo Channel, Group or User/video_imports_button.png)

<hr id="7">

## Adding Vimeo video from a URL
Check out the [Video Imports Screen](http://admin.zype.com/video_imports) and click on the "Add  Video Import" button to get started.


![navigate to form]({{site.url}}assets/Adding Vimeo Video from a URL/import_videos.png)


The next step is to copy a URL from Vimeo that shows the video you want to add.


![copy url]({{site.url}}assets/Adding Vimeo Video from a URL/copy_url.png)


Paste the URL into the field on this page and click "Add Video Import".


![paste url]({{site.url}}assets/Adding Vimeo Video from a URL/paste_your_url.png)

Then click the 'Save Changes' button.

![save changes]({{site.url}}assets/Adding Vimeo Video from a URL/save_changes.png)

If everything went according to plan, you should see the video imports screen again, with a new import from the link you provided. If you're interested in grabbing a bunch of videos from Vimeo, you may want to follow our guides under [Adding Videos.](http://dev.zype.com/platform_docs/adding_videos/)


<hr id="8">

## Adding videos from a YouTube Channel to the Zype Platform
We simplified the process of searching for and importing a YouTube Channel into the Zype Platform.
Before, you had to manually go to YouTube and find your Channel ID. This was a cumbersome
process. Now you can search for a YouTube Channel from the Zype Platform and we will get the Channel ID for you.

**Step 1:**

Go to Video Sources and click on the YouTube icon.

![click youtube]({{site.url}}assets/Adding Videos from a YouTube Channel to the Zype Platform/click_youtube.png)

**Step 2:**

Enter a name for your YouTube video source (something to help you remember it!) and click the
Search YouTube Channels button

![search youtube channels]({{site.url}}assets/Adding Videos from a YouTube Channel to the Zype Platform/search_youtube_channel.png)

**Step 3:**

Enter the channel name that you are searching for and click Search. You will be
given a list of YouTube Channels that match your search criteria. Click the Select Channel
button for the YouTube Channel that you want to add.

![click select channel]({{site.url}}assets/Adding Videos from a YouTube Channel to the Zype Platform/select_channel.png)

**Step 4:**

This will prepopulate the Channel ID for you. All you need to do is click Save Changes
and the Zype Platform will start to import all of the videos from the channel that you selected!

![click submit]({{site.url}}assets/Adding Videos from a YouTube Channel to the Zype Platform/youtube_save_changes.png)

**Step 5:**

Your imported videos are in your import videos page. You can add videos to your catalog
from there.

![import videos]({{site.url}}assets/Adding Videos from a YouTube Channel to the Zype Platform/add_video.png)

<hr id="9">

## Adding YouTube video from a URL
We're happy to announce that the [Zype Platform](http://admin.zype.com) now grants you the power to import videos from YouTube simply by copying an pasting a YouTube link into the platform.

Check out the [Video Imports Screen](http://admin.zype.com/video_imports) and click on the "Add a YouTube Video Import" button to get started.


![navigate to form]({{site.url}}assets/Adding YouTube Video from a URL/add_video_imports_1.png)


The next step is to copy a URL from YouTube that shows the video you want to add.


![copy url]({{site.url}}assets/Adding YouTube Video from a URL/copy_url.png)


Paste the URL into the field on this page and click "Add Video Import".


![paste url]({{site.url}}assets/Adding YouTube Video from a URL/paste_url.png)


If everything went according to plan, you should see the video imports screen again, with a new import from the link you provided. If you're interested in grabbing a bunch of videos from YouTube, you may want to follow our guides under [Adding Videos.](http://dev.zype.com/platform_docs/adding_videos/)

<hr id="10">

## Adding your Crunchyroll videos to Zype
We know you have a lot of video content and we know that you want it all to be available to your viewers through the Zype Platform. That's why we're proud to announce that you can now use [Crunchyroll](http://www.crunchyroll.com/) as a video source for videos on the Zype Platform!

As part of the announcement, we want to walk you through the setup involved and get you up to speed. If you've added videos to the Zype Platform using video sources in the past, the will look very familiar.



### Navigating to the Crunchyroll Video Source form

First, let's login to the [Zype Platform](https://admin.zype.com/) and go to [Video Sources](https://admin.zype.com/video_sources). Now click on the Crunchyroll icon.

![click crunchyroll]({{site.url}}assets/Adding Your Crunchyroll Videos to Zype/click_crunchy.png)



### Adding your affiliate code

Enter a name for your Crunchyroll video source (something you'll remember!) and your Crunchyroll Affiliate code (this is provided to you by Crunchyroll when you become an affiliate.)

![add name and affiliate code]({{site.url}}assets/Adding Your Crunchyroll Videos to Zype/new_crunchy_source.png)



### Importing your videos

Now sit back while we go get all of your Crunchyroll videos and add them to the Zype Platform as video imports.
Once we've imported all of your videos you will find them under the [Video Imports](https://admin.zype.com/video_imports) tab. The last step is to create new videos from the imports or add the video imports to videos you already have on the Zype Platform.

![video imports]({{site.url}}assets/Adding Your Crunchyroll Videos to Zype/import_conformation.png)



### Confirm

You can confirm that your videos were added by clicking on the videos tab and searching for the ones you've just added.

![videos]({{site.url}}assets/Adding Your Crunchyroll Videos to Zype/show_video_imports.png)

<hr id='11'>

## Bulk importing of third party video sources (Advanced)

To bulk add video imports to your video library, check the videos that you want to add and click
the button “Add to Library.” This will automatically add new videos to your video library. If you
would like to merge videos into preexisting videos in your video library, you will need to click
the merge chain for each video.

![add to library]({{site.url}}assets/video_imports/bulk_add.png)

To bulk remove video imports from your video library, check the videos that you want to remove
and click the button “Remove from Library.” Note, this does not delete the video, it only removes
the chosen video import data source from your video.

![remove from library]({{site.url}}assets/video_imports/bulk_remove.png)

<hr id="12">

## Uploading videos to Zype using our Ruby Gem
We're rolling out a bunch of new ways to add video content to the Zype Platform, like [Youtube Channel Import](http://dev.zype.com/posts/2014/11/18/search-youtube-in-zype/) and [Crunchyroll Video Import](http://dev.zype.com/posts/2014/11/19/adding-crunchyroll-as-a-video-source/). In this post we'll show you how to use the Zype Command Line Interface (or CLI) to upload videos that you have stored on a harddrive.

### Downloading and installing the Zype CLI

First, you'll need to download and set up the Zype CLI. You can find the tool on [gitHub](https://github.com/edla/zype-cli).

![gitHub]({{site.url}}assets/Uploading Videos to Zype Using Our Ruby Gem/copy_clone.png)

You'll need to clone down the repo, then run the following commands:

<pre><code>$ gem build zype.gemspec
</code></pre>

<pre><code>$ gem install ./zype-1.0.0.gem
</code></pre>

You can confirm that your installation succeeded by entering

<pre><code>$ zype
</code></pre>

which will display a list of available commands for the Zype CLI. Remember this command in case you have questions about what the Zype CLI can do!

![CLI Interface]({{site.url}}assets/Uploading Videos to Zype Using Our Ruby Gem/commands.png)


### Logging in through the Zype CLI

Let's make sure that you can login and that your Zype CLI is linked to your instance of the Zype Platform.

Enter the command below:

<pre><code>$ zype account:login
</code></pre>

You'll be prompted to enter your Zype API Key. You can find this by logging in to the [Zype Platform](https://admin.zype.com) and clicking on API within the settings menu at the top of the screen. Grab your API key and enter it into the terminal to continue.

### Uploading your videos

You'll need to know which directory contains the videos you want to upload. Once you know where they live, you can run the upload command.

If all of the files live in a single directory, run the following command, replacing the example directory ("/myDir/videos") with your own.

<pre><code>$ zype video:upload --directory="/myDir/videos"
</code></pre>

If you have multiple subdirectories that contain videos, you can pass in a wildcard character (*) at the end of the parent directory to grab all of the videos within each subdirectory. Like this:

<pre><code>$ zype video:upload --directory="/myDir/videos/*"
</code></pre>

Now sit back while we upload all of your videos and add them to the Zype Platform as video imports. Once we've imported all of your videos you will find them under the [Video Imports](https://admin.zype.com/video_imports) tab. The last step is to create new videos from the imports or add the video imports to videos you already have on the Zype Platform.

![video imports]({{site.url}}assets/Uploading Videos to Zype Using Our Ruby Gem/imports.png)

### Confirm

You can confirm that your videos were added by clicking on the videos tab and searching for the ones you've just added.

![videos]({{site.url}}assets/Uploading Videos to Zype Using Our Ruby Gem/confirm.png)

<hr id="13">

## Walkthrough of the Zype API with a sample Rails app
We want to make the Zype Platform accessible to as many types of developers as possible. To do this,
we have provided [API documentation](http://dev.zype.com/api_docs/intro/) and are happy
to <a href='mailto:contact@zypemedia.com'>talk with you</a> about creating a turnkey app.

As a developer, I always like to learn by example, so we have created
a template Rails app to show you what you can do with the Zype Platform using our Ruby Gem and also provide you with a starter template if you want to build off of it for your own web app.

We intentionally kept the styling simple and used [Bootstrap](http://getbootstrap.com/) if
you would like to use this example as a foundation to your Rails app.
Feel free to clone the repo [here](https://github.com/zype/zype-rails). You will
need your Zype API and player keys from the Zype Platform. The README has directions
to how you can find your keys.

*The Zype Rails sample app has the following pages and features.*

**Home Page**

The homepage includes all of your playlists, a link in the header to view all videos,
and a search box to search for a specific video. The playlists can be configured
in the Zype Platform and can be fetched via the Ruby Gem.

![homepage]({{site.url}}assets/Walkthrough of the Zype API with a Sample Rails App/home.png)

**Playlist Page**

You can click on any playlist to view all the videos that belong to that playlist. You can sort
the videos based on release date, name, or popularity. Also note that there are Zype videos
and YouTube videos in the same player. The Zype Platform and Zype API allows you to
seamlessly combine the two.

![playlist page]({{site.url}}assets/Walkthrough of the Zype API with a Sample Rails App/playlist.png)


**Browse all Videos**

The browse all videos uses the Ruby Gem to query the Zype API to get all the videos.
When you hover over a video, you will see the description. Feel free to read the [Video API Documentation](http://dev.zype.com/api_docs/videos/) to see what other information
gets returned when you query for the videos.

![browse videos]({{site.url}}assets/Walkthrough of the Zype API with a Sample Rails App/browse.png)

**Video Page**

When you click on a video's thumbnail, you get directed to the video's page. The video's page
contains the title, description, and video player. The Zype API will deliver the appropriate
player based on where the video source comes from and what Player Rules you set.

![video page]({{site.url}}assets/Walkthrough of the Zype API with a Sample Rails App/video.png)

Have questions about implementing our sample Rails app or want to see examples of
other features or in other languages? Feel free to comment below!

<hr id="14">

## Embedding a player on your site
The Zype Platform allows you to manage all of your video content in one place and
then deliver your video content across any platform or device. In this tutorial, I
will map out how to embed a video uploaded to the Zype Platform on any web page.

**Step 1**

Navigate to your video's page and click on the Embed Code tab.

![Go to Embed Code]({{site.url}}assets/Embedding a Player on Your Site/embed_tab.png)


**Step 2**

Copy the embed code.

![Copy Embed Code]({{site.url}}assets/Embedding a Player on Your Site/click_copy_clip.png)

**Step 3**

You will need to place the div with the id 'zype_player' where you want your player
to be located on your page.

Currently, you can pass in autoplay, player_key, and subscription_id params.
The player_key is required and can be found in Settings > API. Autoplay and subscription_id
are optional.

{% highlight html %}

<div id='zype_player'></div>
<script id='zype_player_js' src='https://api.zype.com/embed/{video_id}.js?autoplay={boolean}&player_key={player_key}&subscription_id={subscription_id}' type='text/javascript'></script>

{% endhighlight %}

<hr id="15">

## Search filters on the Zype Platform
If you've been busy adding video content to the [Zype Platform](http://admin.zype.com) and creating playlists, you might be at the point where you've got a few pages of each. To help you better manage your content, we've added a set of filters to the videos and playlists pages:

![video filtering]({{site.url}}assets/Search Filters on the Zype Platform/video_lib.png)


![playlist filtering]({{site.url}}assets/Search Filters on the Zype Platform/playlist_search.png)


The filter buttons let you select as many parameters for your search as you'd like. Each button has a dropdown you can use to select a value to search by. The default search options are the categories you've created for your site and "Active" (whether or not the video is marked as active). You can create and manage your categories [here.](https://admin.zype.com/categories)

Once you've selected all of the filters you want to use, click the search button to see the results.

You can search by entering a search term, using the filters or both!

If the filter buttons are grayed out, that's because you don't have any videos or playlists yet.

Check out our previous blog post on [defining categories and playlists](http://dev.zype.com/posts/2014/12/04/defining-categories-and-playlists/), if you have questions about getting started.

<hr id="16">

## Choosing thumbnails for your videos
When you upload a video to the Zype Platform, Zype will create thumbnails for your video.
To change your the thumbnail for your video, follow the steps below. Note, this is only
to change your thumbnail from a video uploaded directly to the Zype Platform. It does not apply to
thumbnails from an external data source like YouTube or Vimeo.

**Step 1:**

![thumbnail 1]({{site.url}}assets/thumbnails/thumbnails_1.png)

From your video library, click on the video that you want to change the thumbnail
for and click on the "Thumbnails" tab.

**Step 2:**

![thumbnail 2]({{site.url}}assets/thumbnails/thumbnails_2.png)

Select the thumbnail that you want. The thumbnail will automatically be updated!

<hr id='17'>

## Deleting a video

To delete a video, navigate to your Video Library and click on the trash can for the video
that you want to remove.

![remove video]({{site.url}}assets/videos/remove_video.png)

Note, when you delete a video, the video is removed from all playlists, the video import and/or upload
is released, and video favorites/ratings are removed.

<hr id='18'>

## Upload formats

Zype supports [uploading](https://admin.zype.com/uploads/new) in the following popular media formats:

- 3GP
- AAC
- AVI
- FLV
- MP4
- MPEG-2

We do not currently support the following:

- Apple ProRes
- ARRI
- RED

<hr id='19'>

## Managing video segments

Video segments help you highlight specific time blocks in a video.
This is additional metadata for your video that is exposed via the Zype API.
Each segment can have a start time, an end time, and a description.

To manage a video's segments, navigate to the video's details page and click on
the "Segments" tab. Then, click on the "New Segment" button. You will be prompted
to enter the time in HH:MM:SS format.

![manage segments]({{site.url}}assets/videos/segments.png)
