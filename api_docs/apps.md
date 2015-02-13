---
layout: api
title: Zype Developer Portal | Apps
permalink: /api_docs/apps/
---

## Apps
<hr>
### Retrieve Roku Channel Configurations
Retrieve configuration settings for a Roku Channel.
<hr>
<pre><code>GET - https://api.zype.com/app/?app_key=app_key
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
app_key   | The app key | String

#### Response
200
Content-Type: application/json

<pre><code>{
  "response": {
    "_id": "12345",
    "active": true,
    "app_type_id": "12345",
    "bottom_description_zobject": "director",
    "category_id": "1234basc",
    "color_background": "#ffffff",
    "color_brand": "#C2D43C",
    "color_dark": "#000000",
    "color_light": "#ffffff",
    "color_muted": "#666666",
    "featured_playlist_id": "1234abc",
    "grid_border_offset_hd": "(-1, 0)",
    "grid_border_offset_sd": "(-1, 0)",
    "grid_description_image_offset_hd": "(216, 20)",
    "grid_description_image_offset_sd": "(216, 20)",
    "grid_layout": "two-row-flat-landscape-custom",
    "grid_logo_offset_hd_x": "60",
    "grid_logo_offset_hd_y": "20",
    "grid_logo_offset_sd_x": "60",
    "grid_logo_offset_sd_y": "20",
    "grid_overhang_height_hd": "138",
    "grid_overhang_height_sd": "138",
    "home_name": "Home",
    "info_description": "Learn all about your favorite app",
    "info_title": "Info",
    "logo_offset_hd_x": "60",
    "logo_offset_hd_y": "20",
    "logo_offset_sd_x": "60",
    "logo_offset_sd_y": "20",
    "per_page": 100,
    "play_button_text": "Watch from beginning",
    "prepend_category_name": false,
    "scale_mode": "photo-fit",
    "search_button_text": "Submit!",
    "search_description": "Search for things!",
    "search_error_text": "No results.",
    "search_help_text": "Enter your search.",
    "search_layout": "flat-episodic-16x9",
    "search_title": "Search",
    "site_id": "abc1234",
    "springboard_description_style": "movie",
    "springboard_poster_style": "rounded-rect-16x9-generic",
    "switching_strategy": "minimum-adaptation",
    "title": "Roku Title",
    "toolbar_title": "Tools",
    "top_description_zobject": "actor",
    "version": 1.0,
    "app_images": [
      {
        "logo_hd": "http://u.zype.com/roku/54651b7369702d7c99b20000/logo_hd/1415984896/original.png?1415984896"
      },
      {
      "logo_sd": "http://u.zype.com/roku/54651b7369702d7c99b20000/logo_sd/1415984896/original.png?1415984896"
      },
      {
      "slice_hd": "http://u.zype.com/roku/54651b7369702d7c99b20000/slice_hd/1415984896/original.png?1415984896"
      },
      {
      "slice_sd": "http://u.zype.com/roku/54651b7369702d7c99b20000/slice_sd/1415984897/original.png?1415984897"
      },
      {
        "grid_description_image_hd": "http://u.zype.com/roku/54651b7369702d7c99b20000/grid_description_image_hd/1415984897/original.png?1415984897"
      },
      {
        "grid_description_image_sd": "http://u.zype.com/roku/54651b7369702d7c99b20000/grid_description_image_sd/1415984897/original.png?1415984897"
      },
      {
        "info_poster_hd": "http://u.zype.com/roku/54651b7369702d7c99b20000/info_poster_hd/1415984898/original.png?1415984898"
      },
      {
        "info_poster_sd": "http://u.zype.com/roku/54651b7369702d7c99b20000/info_poster_sd/1415984898/original.png?1415984898"
      },
      {
        "search_poster_hd": "http://u.zype.com/roku/54651b7369702d7c99b20000/search_poster_hd/1415984898/original.png?1415984898"
      },
      {
        "search_poster_sd": "http://u.zype.com/roku/54651b7369702d7c99b20000/search_poster_sd/1415984899/original.png?1415984899"
      },
      {
        "grid_border_image_hd": "http://u.zype.com/roku/54651b7369702d7c99b20000/grid_border_image_hd/1415984899/original.png?1415984899"
      },
      {
        "grid_border_image_sd": "http://u.zype.com/roku/54651b7369702d7c99b20000/grid_border_image_sd/1415984899/original.png?1415984899"
      }
    ],
    "video_sources": [...]
  }
}
</code></pre>

<hr>
### Retrieve iPhone App Configurations
Retrieve configuration settings for an iPhone App.
<hr>
<pre><code>GET - https://api.zype.com/app/?app_key=app_key
</code></pre>

#### Parameters

Parameter | Function | Type
--------- | -------- | ----
app_key   | The app key | String

#### Response
200
Content-Type: application/json

<pre><code>{
  "response": {
    "_id": "53a9cd3069702d56d8000000",
    "active": true,
    "app_type_id": null,
    "channel": {
      "_id": "53a9cdf169702d5834010000",
      "background_color": "#000000",
      "font_color": "#FFFFFF",
      "title": 0,
      "banner_url": "http://u.zype.com/app/channel/53a9cdf169702d5834010000/banner/original.png?1407812250",
      "large_banner_url": "http://u.zype.com/app/channel/53a9cdf169702d5834010000/large_banner/original.png?1407812288",
      "icon_url": "http://u.zype.com/app/channel/53a9cdf169702d5834010000/icon/original.jpg?1407812317"
    },
    "device_id": null,
    "site_id": "53c0457a69702d4d66030000",
    "store_id": null,
    "tiles": [
    {
      "_id": "53b17eb869702d4ade000000",
      "background_color": "#C154C1",
      "font_color": "#FFFFFF",
      "position": 2,
      "text": "Some descriptive information about Tile 2",
      "title": "Favorites",
      "url": "favorites",
      "icon_url": "http://u.zype.com/app/tile/53b17eb869702d4ade000000/icon/original.png?1407811649"
    },
    {
      "_id": "53b17ec369702d4ade020000",
      "background_color": "#FF7F00",
      "font_color": "#FFFFFF",
      "position": 4,
      "text": "Some descriptive information about Tile 4",
      "title": "Google+",
      "url": "https://plus.google.com/u/0/113521400992096024513",
      "icon_url": "http://u.zype.com/app/tile/53b17ec369702d4ade020000/icon/original.png?1407811698"
    },
    {
      "_id": "53b17ecc69702d4ade030000",
      "background_color": "#C154C1",
      "font_color": "#FFFFFF",
      "position": 0,
      "text": "Some descriptive information about Tile 5",
      "title": "Video",
      "url": "videos",
      "icon_url": "http://u.zype.com/app/tile/53b17ecc69702d4ade030000/icon/original.png?1407811738"
    },
    {
      "_id": "53b17ecd69702d4ade040000",
      "background_color": "#BFFF00",
      "font_color": "#FFFFFF",
      "position": 6,
      "text": "Some descriptive information about Tile 6",
      "title": "Twitter",
      "url": "http://twitter.com/ryanckulp",
      "icon_url": "http://u.zype.com/app/tile/53b17ecd69702d4ade040000/icon/original.png?1407811765"
    },
    {
      "_id": "53b17ed669702d4ade050000",
      "background_color": "#008080",
      "font_color": "#FFFFFF",
      "position": 7,
      "text": "Some descriptive information about Tile 7",
      "title": "Blog",
      "url": "http://ryanckulp.com/",
      "icon_url": "http://u.zype.com/app/tile/53b17ed669702d4ade050000/icon/original.png?1407811787"
    },
    {
      "_id": "53b17ed769702d4ade060000",
      "background_color": "#FF7F00",
      "font_color": "#FFFFFF",
      "position": 8,
      "text": "Some descriptive information about Tile 8",
      "title": "Music",
      "url": "http://lastnamekulp.com/",
      "icon_url": "http://u.zype.com/app/tile/53b17ed769702d4ade060000/icon/original.png?1407811884"
    },
    {
      "_id": "53babe6269702d012e000000",
      "background_color": "#FF7F00",
      "font_color": "#FFFFFF",
      "position": 9,
      "text": "Some descriptive information about Tile 9",
      "title": "Facebook",
      "url": "https://www.facebook.com/ryanckulp",
      "icon_url": "http://u.zype.com/app/tile/53babe6269702d012e000000/icon/original.png?1407811904"
    }
    ],
    "title": "Ryan Kulp Guitar Ninja",
    "version": "0.0.0",
    "store_icon_url": null,
    "video_sources": [
      {
      "_id": "53acf2b669702d2b8f010000",
      "_keywords": [
        "videosource",
        "youtube"
      ],
      "created_at": "2014-06-27T00:27:41.895-04:00",
      "deleteable": true,
      "deleted_at": null,
      "editable": true,
      "guid": "UC7iW0FatScRqIGHeA-5cFiw",
      "name": null,
      "provider_id": null,
      "refreshed_at": "2015-02-10T06:59:59.187-05:00",
      "site_id": "53c0457a69702d4d66030000",
      "updated_at": "2015-02-10T07:00:01.937-05:00",
      "video_count": 0
      }
    ]
  }
}
</code></pre>
