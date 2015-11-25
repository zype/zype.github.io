---
layout: platform
title: Zype Developer Portal | Platform Docs
permalink: /platform_docs/embeddable_playlist_widget/
---
#Embeddable Playlist Widget
The Zype Embeddable Playlist Widget allows you to easily create and customize an embeddable playlist video player from any of your existing Zype Playlists. The playlist widget may be created in 3 simple steps and embedded on any website.

<div style="width: 100%;">
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
    <a href="#1">
    Select a Playlist</a>
  </div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
  <a href="#2">
  Customize the Playlist Widget</a>
  </div>
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
  <a href="#3">
  Embed the Playlist Widget</a>
  </div>
</div>

<hr />

<div id="1"></div>

# Select a Playlist
1. From the Zype admin, select Playlists. (For more information about Playlists and how to create them, see [http://dev.zype.com/platform_docs/playlists/](http://dev.zype.com/platform_docs/playlists/))
2. Your existing playlists are displayed in a table. On the rightmost column of each row is a set of icons. Click the "Preview" button (video camera icon) to configure the playlist widget of your choice. Note: only Active playlists may be embedded

![select playlist]({{site.url}}assets/embeddable_playlist_widget/embed-playlist-01--select-playlist.jpg)

<div id="2"></div>

# Customize the Playlist Widget
The **Embed Code** tab allows you to easily customize the visual appearance of the playlist widget using the options on the left side of the page. The right side of the page displays a live preview of what the playlist embed will look like.

## Basic Options

### Format
Choose **JavaScript** if you want your playlist widget to be *responsive* (automatically adapt to the width of the page it is on), otherwise choose **iFrame**.

### Playlist Skin
There are 4 different types of pre-defined Playlist Skins, which control the appearance of the playlist widget:

- **Grid, Thumbnails, &amp; Titles** — Playlist videos are displayed in a grid with thumbnails and titles.

- **Grid, Thumbnails** — Playlist videos are displayed in a grid with thumbnails only.

- **List, Thumbnails, &amp; Titles** — Playlist videos are displayed in a list with thumbnails and titles.

- **List, Titles** — Playlist videos are displayed in a list with titles only.

### Auto Play
Choose whether your playlist will automatically start playing. Defaults to "On".

### Auto Loop
Choose whether your playlist will automatically start playing from the beginning after the last videos ends. Defaults to "Off".

### Resolution (iFrame Only)
Choose the dimensions of your embed.

![basic options]({{site.url}}assets/embeddable_playlist_widget/embed-playlist-02--basic-options.jpg)

## Advanced Options

### Playlist Background Color
Choose the default color for the background of the playlist.

### Playlist Font Color

- **Font Color** — The font color for the playlist items

- **Font Active Color** — The font color for the playlist item currently being viewed

- **Font Hover Color** — The font color for the playlist item currently being hovered over

### Playlist Item Spacing
Modify the spacing between playlist items

![advanced options]({{site.url}}assets/embeddable_playlist_widget/embed-playlist-03--advanced-options.jpg)

<div id="3"></div>

# Embed the Playlist Widget
When you're ready to embed your playlist widget, simply click the **Copy to Clipboard** button located just above the playlist widget preview. Paste the embed code to website of your choice by using **Edit > Paste** from your web browser or **Control + V** (**Command + V on Mac**) from your keyboard.

![embed code]({{site.url}}assets/embeddable_playlist_widget/embed-playlist-04--copy-embed-code.jpg)
