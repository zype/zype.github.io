---
layout: post
title:  "Upload and Search Embeddable Widgets"
date:   2016-02-01 10:37:55
categories: developers
redirect_to: https://support.zype.com/hc/en-us/articles/216217868
---

Now you can easily add upload and search functionality directly on your own website. This allows you to use the power of the Zype platform with the ease of a CMS system on your own site.

<iframe allowfullscreen="allowfullscreen" frameborder="0" height="315" src="https://player.zype.com/embed/56b4e8b369702d0802b14000.html?autoplay=false&app_key=ePc03QlhcUwIzcykavPjyS7mcZv4HA8TxCUobbEVEkJ8zDQqYGeo7FdYUbdaYWks" width="560"></iframe>

## Upload Embed

The Zype upload embeddable widget allows you to upload videos to the Zype platform from your own website.

_Note: You should only put this widget in a secure place on your website as it allows any user to upload content directly to your account._

![Upload Embed]({{site.url}}/assets/upload-search/upload-embed.png)

### How To Use the Upload Embed

1. From the Zype dashboard, in the top right click the Settings icon (gear icon), then choose [Tools & SDK.](https://admin.zype.com/tools)
2. Click the [Upload Embed link](https://admin.zype.com/tools/upload).
3. Click Copy to Clipboard to grab the embed code.
4. Paste the code into your website, ideally in a secure place.
5. That's it!

### Customizing the Upload Embed

There are a number of customization options available for the Upload Embed. You can choose the main category to allow users to tag videos on upload, show/hide various fields, and customize the text labels allowing for easy internationalization.

For security we allow you to add an Embed Domain Whitelist. This lets you to specify which domains are allowed to hosted your upload embed widget, helping to prevent unauthorized users from hosting the upload on their sites.

1. From the Zype dashboard, in the top right click the Settings icon (gear icon), then choose [Tools & SDK.](https://admin.zype.com/tools)
2. Click the [Upload Embed link](https://admin.zype.com/tools/upload).
3. Click the Upload Embed Settings Tab.

Option | Description
---- | -----------
Upload Category | The selection category for uploads. Allows you to choose a category type on video upload.
Auto Add | Auto add video to video library on upload.
Auto Activate | Auto activate video to video library on upload.
Show Embed Code | Show the embed code after successful upload.
Show Title Field | Toggles title field.
Show Description Field | Toggles description field.
Show Category Field | Toggle category field.
Title Label | Label text for title field.
Description Label | Label text for description field.
Select Video Label | Label text for select video label and button.
Upload Button Text | Text for upload (form submit) button.
Upload Widget Success Message | Text for upload success.
Embed Code Copy Button Text | Text for embed copy button.
Embed Domain Whitelist | Restrict your embed for use only on certain domains. Leaving this box empty will allow *all* domains. Enter a domain to restrict to that domain only, for example: mysite.com. Do not enter the full path (enter __mysite.com__, NOT http://mysite.com). For multiple values separate with a comma.

## Securing the Upload Embed

To increase the security of the upload embed you can restrict access to only certain domains.

1. From the Zype dashboard, in the top right click the Settings icon (gear icon), then choose [Tools & SDK.](https://admin.zype.com/tools)
2. Click the [Upload Embed link](https://admin.zype.com/tools/upload).
3. Click the Upload Embed Settings Tab.
4. In the Embed Domain Whitelist textarea add the domain of your website. For example enter __mysite.com__ (NOT http://mysite.com). Leaving this box empty will allow *all* domains. For multiple values separate with a comma.

## Search Embed

The search embed allows you to perform searches of your video library from your own website.

![Search Embed]({{site.url}}/assets/upload-search/search-embed.png)

### How To Use the Search Embed

1. From the Zype dashboard, in the top right click the Settings icon (gear icon), then choose [Tools & SDK.](https://admin.zype.com/tools)
2. Click the [Search Embed link](https://admin.zype.com/tools/search).
3. Click Copy to Clipboard to grab the embed code.
4. Paste the code into your website.
5. That's it!

### Customizing the Search Embed

You can toggle which search filters are displayed on the search embed.

For security we allow you to add an Embed Domain Whitelist. This lets you to specify which domains are allowed to hosted your search embed widget, helping to prevent unauthorized users from hosting the search form on their sites.

Main Filter Button | Display the main filter button.
Active Button | Display the "active" filter button which allows users to search for videos that are active or not active.
Video Source Search Filter | Display the filter for searching by video source.
Embed Domain Whitelist | Restrict your embed for use only on certain domains. Leaving this box empty will allow *all* domains. Enter a domain to restrict to that domain only, for example: mysite.com. Do not enter the full path (enter __mysite.com__, NOT http://mysite.com). For multiple values separate with a comma.

## Securing the Search Embed

To increase the security of the search embed you can restrict access to only certain domains.

1. From the Zype dashboard, in the top right click the Settings icon (gear icon), then choose [Tools & SDK.](https://admin.zype.com/tools)
2. Click the [Search Embed link](https://admin.zype.com/tools/search).
3. Click the Search Embed Settings Tab.
4. In the Embed Domain Whitelist textarea add the domain of your website. For example enter __mysite.com__ (NOT http://mysite.com). Leaving this box empty will allow *all* domains. For multiple values separate with a comma.