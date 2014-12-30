---
layout: api
title: Zype Developer Portal | Apps
permalink: /api_docs/apps/
---

## Apps
<hr>
### Retrieve an App
Retrieve configuration settings for an App.
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
