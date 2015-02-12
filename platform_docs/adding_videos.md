---
layout: platform
title: Zype Developer Portal | Platform Docs
permalink: /platform_docs/adding_videos/
---
##Adding Videos to the Zype Platform
You can add videos to your Zype Library in two different ways. The first way is to upload
videos directly to the Zype Platform. The second way is to import videos from a third-party source such as YouTube, Hulu, or Crunchyroll. Videos that are uploaded will have a Zype
Video Source, all other videos will have a video source from the respected third-party.

<div style="width: 100%;">
<div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
  <a href="#0">
  Uploading Videos to the Zype Platform from the Web</a>
</div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
    <a href="#1">
    Adding Videos from a YouTube Channel to the Zype Platform</a>
  </div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
  <a href="#2">
  Adding Videos from a Vimeo Channel, Group or User to the Zype Platform</a>
  </div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
    <a href="#3">
    Adding Your Crunchyroll Videos to the Zype Platform</a>
  </div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
    <a href="#4">
    Uploading Videos to the Zype Platform Using Our Ruby Gem</a>
  </div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
  <a href="#5">
  Adding YouTube Videos from a URL</a>
  </div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
  <a href="#6">
  Adding Vimeo Videos from a URL</a>
  </div>
</div>

<hr id="0">
## Uploading Videos to the Zype Platform from the Web
The easiest way to add a video to your video library is to upload a video to the Zype Platform.

**Step 1:**

Go to Uploads, click the upload button, and select the video that you want from your computer.

![Upload Videos]({{ site.url }}/assets/Uploading Videos to the Zype Platform from the Web/upload_video_1.png)

**Step 2:**

When the video is finished uploading, click add video. This will start to transcode your video.
All uploaded videos will need to be transcoded before being able to be viewed.

![add video]({{ site.url }}/assets/Uploading Videos to the Zype Platform from the Web/add_video_import_button.png)

<hr id="1">

## Adding Videos from a YouTube Channel
We simplified the process of searching for and importing a YouTube Channel into the Zype Platform.
Before, you had to manually go to YouTube and find your Channel ID. This was a cumbersome
process. Now you can search for a YouTube Channel from the Zype Platform and we will get the Channel ID for you.

**Step 1:**

Go to Video Sources and click on the YouTube icon.

![click youtube]({{site.url}}assets/Adding Videos from a YouTube Channel to the Zype Platform/click_youtube.png)
**Step 2:**

Enter a name for your YouTube Video Source (something to help you remember it!) and click the
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

Your imported videos are in your import videos page. You can add videos to your catalogue
from there.

![import videos]({{site.url}}assets/Adding Videos from a YouTube Channel to the Zype Platform/add_video.png)

<hr id="2">

## Adding Videos from a Vimeo Channel, Group or User
We're happy to provide you with a simple and powerful for importing your Vimeo videos to the Zype Platform. Below are the steps for grabbing your videos, no matter where they exist in Vimeo.

**Step 1:**

Go to Video Sources and click on the Vimeo icon.

![click vimeo]({{site.url}}assets/Adding Videos from a Vimeo Channel, Group or User/click_vimeo.png)

**Step 2:**

Enter a name for your Vimeo Video Source (something to help you remember it!).

**Step 3:**

You'll need to copy and paste a link to your Vimeo videos from a group, channel or user. Here are some quick example links:

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


<hr id="3">

## Adding Your Crunchyroll Videos
We know you have a lot of video content and we know that you want it all to be available to your viewers through the Zype Platform. That's why we're proud to announce that you can now use [Crunchyroll](http://www.crunchyroll.com/) as a video source for videos on the Zype Platform!

As part of the announcement, we want to walk you through the setup involved and get you up to speed. If you've added videos to the Zype Platform using video sources in the past, the will look very familiar.



### Navigating to the Crunchyroll Video Source form

First, let's login to the [Zype Platform](https://admin.zype.com/) and go to [Video Sources](https://admin.zype.com/video_sources). Now click on the Crunchyroll icon.

![click crunchyroll]({{site.url}}assets/Adding Your Crunchyroll Videos to Zype/click_crunchy.png)



### Adding your affiliate code

Enter a name for your Crunchyroll Video Source (something you'll remember!) and your Crunchyroll Affiliate code (this is provided to you by Crunchyroll when you become an affiliate.)

![add name and affiliate code]({{site.url}}assets/Adding Your Crunchyroll Videos to Zype/new_crunchy_source.png)



### Importing your videos

Now sit back while we go get all of your Crunchyroll videos and add them to the Zype Platform as video imports.
Once we've imported all of your videos you will find them under the [Video Imports](https://admin.zype.com/video_imports) tab. The last step is to create new videos from the imports or add the video imports to videos you already have on the Zype Platform.

![video imports]({{site.url}}assets/Adding Your Crunchyroll Videos to Zype/import_conformation.png)



### Confirm

You can confirm that your videos were added by clicking on the videos tab and searching for the ones you've just added.

![videos]({{site.url}}assets/Adding Your Crunchyroll Videos to Zype/show_video_imports.png)


<hr id="4">

## Uploading Videos to the Zype Platform Using Our Ruby Gem
We're rolling out a bunch of new ways to add video content to the Zype Platform, like [Youtube Channel Import](http://dev.zype.com/posts/2014/11/18/search-youtube-in-zype/) and [Crunchyroll Video Import](http://dev.zype.com/posts/2014/11/19/adding-crunchyroll-as-a-video-source/). In this post we'll show you how to use the Zype Command Line Interface (or CLI) to upload videos that you have stored on a harddrive.

### Downloading and Installing the Zype CLI

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

<hr id="5">

## Adding YouTube Video from a URL
We're happy to announce that the [Zype Platform](http://admin.zype.com) now grants you the power to import videos from YouTube simply by copying an pasting a YouTube link into the platform.

Check out the [Video Imports Screen](http://admin.zype.com/video_imports) and click on the "Add Video Import" button to get started.


![navigate to form]({{site.url}}assets/Adding YouTube Video from a URL/add_video_imports_1.png)


The next step is to copy a URL from YouTube that shows the video you want to add.


![copy url]({{site.url}}assets/Adding YouTube Video from a URL/copy_url.png)


Paste the URL into the field on this page and click "Add Video Import".


![paste url]({{site.url}}assets/Adding YouTube Video from a URL/paste_url.png)


If everything went according to plan, you should see the video imports screen again, with a new import from the link you provided. If you're interested in grabbing a bunch of videos from YouTube, you may want to follow our guides under [Adding Videos.](http://dev.zype.com/platform_docs/adding_videos/)

<hr id="6">

## Adding Vimeo Video from a URL
Check out the [Video Imports Screen](http://admin.zype.com/video_imports) and click on the "Add  Video Import" button to get started.


![navigate to form]({{site.url}}assets/Adding Vimeo Video from a URL/import_videos.png)


The next step is to copy a URL from Vimeo that shows the video you want to add.


![copy url]({{site.url}}assets/Adding Vimeo Video from a URL/copy_url.png)


Paste the URL into the field on this page and click "Add Video Import".


![paste url]({{site.url}}assets/Adding Vimeo Video from a URL/paste_your_url.png)

Then click the 'Save Changes' button.

![save changes]({{site.url}}assets/Adding Vimeo Video from a URL/save_changes.png)

If everything went according to plan, you should see the video imports screen again, with a new import from the link you provided. If you're interested in grabbing a bunch of videos from Vimeo, you may want to follow our guides under [Adding Videos.](http://dev.zype.com/platform_docs/adding_videos/)
