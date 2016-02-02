---
layout: platform
title: Zype Developer Portal | Platform Docs
permalink: /platform_docs/adding_videos/
---
##Adding videos to the Zype Platform
You can add videos to your Zype Library in two different ways. The first way is to upload
videos directly to the Zype Platform. The second way is to import videos from a third-party source such as YouTube, Hulu, or Crunchyroll. Videos that are uploaded will have a Zype
video source, all other videos will have a video source from the respected third-party.

<div style="width: 100%;">
<div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
  <a href="#0">
  Uploading videos to the Zype Platform from the web</a>
</div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
    <a href="#1">
    Adding videos from a YouTube Channel to the Zype Platform</a>
  </div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
  <a href="#2">
  Adding videos from a Vimeo Channel, Group or User to the Zype Platform</a>
  </div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
  <a href="#3">
  Adding videos from a Vimeo PRO account to the Zype Platform</a>
  </div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
    <a href="#4">
    Adding your Crunchyroll videos to the Zype Platform</a>
  </div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
    <a href="#5">
    Uploading videos to the Zype Platform using our Ruby Gem</a>
  </div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
  <a href="#6">
  Adding YouTube videos from a URL</a>
  </div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
  <a href="#7">
  Adding Vimeo videos from a URL</a>
  </div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
  <a href="#8">
  Adding Livestream.com Events and Clips</a>
  </div>
</div>

<hr id="0">
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

<hr id="1">

## Adding videos from a YouTube Channel
We've made the process of importing videos from your YouTube Channel even simpler. You can upload a single video, a channel, or import videos from an authenticated YouTube account.

### Overview ###

Go to the Zype dashboard and from the left nav click Import & Upload, then click YouTube.

![click youtube]({{site.url}}/assets/Adding Videos from a YouTube Channel to the Zype Platform/youtube-import/image06.png)

### Import a Single Video ###

To import a single video, paste a single video URL and click the Continue button:

![click youtube]({{site.url}}/assets/Adding Videos from a YouTube Channel to the Zype Platform/youtube-import/image07.png)

Once you’ve successfully imported your video you can view it by clicking the Manage Video button:

![click youtube]({{site.url}}/assets/Adding Videos from a YouTube Channel to the Zype Platform/youtube-import/image03.png)

### Import a Channel ###

To import an entire channel, paste a YouTube channel URL into the text field and click the Continue button:

![click youtube]({{site.url}}/assets/Adding Videos from a YouTube Channel to the Zype Platform/youtube-import/image02.png)

If you don’t have an URL, you can look for a channel using keywords in the same text field.
If the search is successful you can see a drop-down with all YouTube channel suggestions. Select any channel name and click the Continue button to proceed.

![click youtube]({{site.url}}/assets/Adding Videos from a YouTube Channel to the Zype Platform/youtube-import/image05.png)

### Import from a Connected Account ###

You also have the ability to import videos from your own YouTube channel by clicking the
Connect To Account button and proceeding with the Google authorization instructions:

![click youtube]({{site.url}}/assets/Adding Videos from a YouTube Channel to the Zype Platform/youtube-import/image08.png)

The next step is to review and select videos from a chosen YouTube channel.
Select the videos you'd like to add into Video Library and click the Next button. You may also filter video results using the text field in the table header or select all videos by clicking the choose all checkbox.

![click youtube]({{site.url}}/assets/Adding Videos from a YouTube Channel to the Zype Platform/youtube-import/image01.png)

The next step allows you to customize your import.

![click youtube]({{site.url}}/assets/Adding Videos from a YouTube Channel to the Zype Platform/youtube-import/image00.png)

There are several controls that allow you to customize your import:

1. By clicking this checkbox only the metadata of selected videos will be imported.
2. By clicking this checkbox the video content and metadata of selected videos will be imported.
3. When turned on, new videos uploaded to this channel will automatically be added to your library.
4. When turned on, new videos uploaded to this channel will automatically be made active when added to your video library.
5. Name for the import (and newly created video source object ). Only you will see this name as a way of organizing your imports.

When you’re all set, click the Complete Import button.

Once you’ve successfully imported your YouTube channel you can find all the new videos in Video Imports and selected videos in Video Library.

![click youtube]({{site.url}}/assets/Adding Videos from a YouTube Channel to the Zype Platform/youtube-import/image04.png)

<hr id="2">

## Adding videos from a Vimeo Channel, Group or User
We're happy to provide you with a simple and powerful tool for importing your Vimeo videos to the Zype Platform. Below are the steps for grabbing your videos, no matter where they exist in Vimeo.

**Step 1:**

Go to Video Sources and click on the Vimeo icon.

![click vimeo]({{site.url}}/assets/Adding Videos from a Vimeo Channel, Group or User/click_vimeo.png)

**Step 2:**

Enter a name for your Vimeo video source (something to help you remember it!).

**Step 3:**

You'll need to copy and paste a link to your Vimeo videos from a Group, Channel or User. Here are some quick example links:

<pre><code>https://vimeo.com/channels/staffpicks

https://vimeo.com/user36554072/videos

https://vimeo.com/groups/animation
</code></pre>

First, go to Vimeo and copy the link:

![copy your link]({{site.url}}/assets/Adding Videos from a Vimeo Channel, Group or User/vimeo_copy.png)

Then paste the link into the Vimeo Source form:

![paste your link]({{site.url}}/assets/Adding Videos from a Vimeo Channel, Group or User/paste_your_link.png)

Then click the 'Save Changes' button.


**Step 4:**

If everything went according to plan, you can see your new video imports by clicking on the green 'Video Imports' button.

![video imports button]({{site.url}}/assets/Adding Videos from a Vimeo Channel, Group or User/video_imports_button.png)


<hr id="3">

## Adding videos from a Vimeo PRO account

You can import videos from Vimeo PRO to your Video Library. Videos that have a Vimeo PRO video source are
playable on all devices including Roku and Fire TV and plays natively on iPhone and Android just
like videos that are uploaded directly to the Zype Platform.

Here's how.

**Step 1:**

Navigate to the [Import & Upload dashboard](https://admin.zype.com/import_upload) and
click on Vimeo PRO.

![video imports]({{site.url}}/assets/Adding Videos from a Vimeo PRO Account/dashboard.png)

**Step 2:**

Click on the "Import from Vimeo PRO" button to send you to vimeo.com to authenticate.

![video imports]({{site.url}}/assets/Adding Videos from a Vimeo PRO Account/go_to_vimeo.png)

**Step 3:**

Enter your Vimeo PRO email and password credentials.

![video imports]({{site.url}}/assets/Adding Videos from a Vimeo PRO Account/Log_In.png)

**Step 4:**

Agree to connect "Zype" to your Vimeo account.

![video imports]({{site.url}}/assets/Adding Videos from a Vimeo PRO Account/Vimeo_Auth.png)

**Step 5:**

Decide whether you want your Vimeo PRO imports to automatically get added to your video library
and whether these videos should automatically be active when they appear in your video library.

![video imports]({{site.url}}/assets/Adding Videos from a Vimeo PRO Account/import.png)

**Step 6:**

Congrats, you have linked Vimeo PRO successfully! If the videos are automatically add your
Vimeo PRO imports to your video library, they can be found in your [video library](https://admin.zype.com/videos).
If not, they can be found in your [video imports](https://admin.zype.com/video_imports).

![video imports]({{site.url}}/assets/Adding Videos from a Vimeo PRO Account/success.png)

**Step 7:**

Confirm that you have the appropriate player rules set up to expose your Vimeo PRO players so
that it can deliver content to all devices including web and Roku. Go to [player rules](https://admin.zype.com/player_rules)
and make sure that you have a Vimeo Pro (Native) Player, a Vimeo Pro (Zype) Player, and a Zype Roku Pro Player. If you do
not have a proper player rule, click on the "New Player Rule" button and create Vimeo PRO player rules for the
desired device and Vimeo PRO Player. For more information on player rules, go to the [player rules platform docs](http://dev.zype.com/platform_docs/player_rules/).

![vimeo pro player rule]({{site.url}}/assets/Adding Videos from a Vimeo PRO Account/player_rules.png)

<hr id="4">

## Adding your Crunchyroll videos
We know you have a lot of video content and we know that you want it all to be available to your viewers through the Zype Platform. That's why we're proud to announce that you can now use [Crunchyroll](http://www.crunchyroll.com/) as a video source for videos on the Zype Platform!

As part of the announcement, we want to walk you through the setup involved and get you up to speed. If you've added videos to the Zype Platform using video sources in the past, the will look very familiar.



### Navigating to the Crunchyroll Video Source form

First, let's login to the [Zype Platform](https://admin.zype.com/) and go to [Video Sources](https://admin.zype.com/video_sources). Now click on the Crunchyroll icon.

![click crunchyroll]({{site.url}}/assets/Adding Your Crunchyroll Videos to Zype/click_crunchy.png)



### Adding your affiliate code

Enter a name for your Crunchyroll video source (something you'll remember!) and your Crunchyroll Affiliate code (this is provided to you by Crunchyroll when you become an affiliate.)

![add name and affiliate code]({{site.url}}/assets/Adding Your Crunchyroll Videos to Zype/new_crunchy_source.png)



### Importing your videos

Now sit back while we go get all of your Crunchyroll videos and add them to the Zype Platform as video imports.
Once we've imported all of your videos you will find them under the [Video Imports](https://admin.zype.com/video_imports) tab. The last step is to create new videos from the imports or add the video imports to videos you already have on the Zype Platform.

![video imports]({{site.url}}/assets/Adding Your Crunchyroll Videos to Zype/import_conformation.png)



### Confirm

You can confirm that your videos were added by clicking on the videos tab and searching for the ones you've just added.

![videos]({{site.url}}/assets/Adding Your Crunchyroll Videos to Zype/show_video_imports.png)


<hr id="5">

## Uploading videos to the Zype Platform using our Ruby Gem
We're rolling out a bunch of new ways to add video content to the Zype Platform, like [Youtube Channel Import](http://dev.zype.com/posts/2014/11/18/search-youtube-in-zype/) and [Crunchyroll Video Import](http://dev.zype.com/posts/2014/11/19/adding-crunchyroll-as-a-video-source/). In this post we'll show you how to use the Zype Command Line Interface (or CLI) to upload videos that you have stored on a hard drive.

### Downloading and installing the Zype CLI

First, you'll need to download and set up the Zype CLI. You can find the tool on [gitHub](https://github.com/edla/zype-cli).

![gitHub]({{site.url}}/assets/Uploading Videos to Zype Using Our Ruby Gem/copy_clone.png)

You'll need to clone down the repo, then run the following commands:

<pre><code>$ gem build zype.gemspec
</code></pre>

<pre><code>$ gem install ./zype-1.0.0.gem
</code></pre>

You can confirm that your installation succeeded by entering

<pre><code>$ zype
</code></pre>

which will display a list of available commands for the Zype CLI. Remember this command in case you have questions about what the Zype CLI can do!

![CLI Interface]({{site.url}}/assets/Uploading Videos to Zype Using Our Ruby Gem/commands.png)


### Logging in through the Zype CLI

Let's make sure that you can login and that your Zype CLI is linked to your instance of the Zype Platform.

Enter the command below:

<pre><code>$ zype account:login
</code></pre>

You'll be prompted to enter your Zype API Key. You can find this by logging in to the [Zype Platform](https://admin.zype.com) and clicking on API within the settings menu at the top of the screen. Grab your API Key and enter it into the terminal to continue.

### Uploading your videos

You'll need to know which directory contains the videos you want to upload. Once you know where they live, you can run the upload command.

If all of the files live in a single directory, run the following command, replacing the example directory ("/myDir/videos") with your own.

<pre><code>$ zype video:upload --directory="/myDir/videos"
</code></pre>

If you have multiple subdirectories that contain videos, you can pass in a wildcard character (*) at the end of the parent directory to grab all of the videos within each subdirectory. Like this:

<pre><code>$ zype video:upload --directory="/myDir/videos/*"
</code></pre>

Now sit back while we upload all of your videos and add them to the Zype Platform as video imports. Once we've imported all of your videos you will find them under the [Video Imports](https://admin.zype.com/video_imports) tab. The last step is to create new videos from the imports or add the video imports to videos you already have on the Zype Platform.

![video imports]({{site.url}}/assets/Uploading Videos to Zype Using Our Ruby Gem/imports.png)

### Confirm

You can confirm that your videos were added by clicking on the videos tab and searching for the ones you've just added.

![videos]({{site.url}}/assets/Uploading Videos to Zype Using Our Ruby Gem/confirm.png)

<hr id="6">

## Adding YouTube video from a URL
We're happy to announce that the [Zype Platform](http://admin.zype.com) now grants you the power to import videos from YouTube simply by copying an pasting a YouTube link into the platform.

Check out the [Video Imports Screen](http://admin.zype.com/video_imports) and click on the "Add Video Import" button to get started.


![navigate to form]({{site.url}}/assets/Adding YouTube Video from a URL/add_video_imports_1.png)


The next step is to copy a URL from YouTube that shows the video you want to add.


![copy url]({{site.url}}/assets/Adding YouTube Video from a URL/copy_url.png)


Paste the URL into the field on this page and click "Add Video Import".


![paste url]({{site.url}}/assets/Adding YouTube Video from a URL/paste_url.png)


If everything went according to plan, you should see the video imports screen again, with a new import from the link you provided. If you're interested in grabbing a bunch of videos from YouTube, you may want to follow our guides under [Adding Videos.](http://dev.zype.com/platform_docs/adding_videos/)

<hr id="7">

## Adding Vimeo video from a URL
Check out the [Video Imports Screen](http://admin.zype.com/video_imports) and click on the "Add  Video Import" button to get started.


![navigate to form]({{site.url}}/assets/Adding Vimeo Video from a URL/import_videos.png)


The next step is to copy a URL from Vimeo that shows the video you want to add.


![copy url]({{site.url}}/assets/Adding Vimeo Video from a URL/copy_url.png)


Paste the URL into the field on this page and click "Add Video Import".


![paste url]({{site.url}}/assets/Adding Vimeo Video from a URL/paste_your_url.png)

Then click the 'Save Changes' button.

![save changes]({{site.url}}/assets/Adding Vimeo Video from a URL/save_changes.png)

If everything went according to plan, you should see the video imports screen again, with a new import from the link you provided. If you're interested in grabbing a bunch of videos from Vimeo, you may want to follow our guides under [Adding Videos.](http://dev.zype.com/platform_docs/adding_videos/)

<hr id='8'>

## Adding Livestream.com Events and Clips

Navigate to the [Import & Upload dashboard](https://admin.zype.com/import_upload) and click on Livestream.

![livestream 1]({{site.url}}/assets/livestream/livestream_1.png)

Enter the Livestream.com Event or Livestream.com Clip url for the video that you want
to import. You can add additional metadata such as the title and the description. If
the "Add Video" button is toggled on, your Livestream.com video will automatically be
added into your video library.

![livestream 2]({{site.url}}/assets/livestream/livestream_2.png)

**What is the difference between an event and a clip?**

An event is a live event that is currently streaming. A clip is a recorded video.
