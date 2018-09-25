---
layout: post
title:  "MRSS Import Format"
date:   2016-05-31 10:37:55
categories: developers
redirect_to: https://support.zype.com/hc/en-us/articles/115011037147
---

Below is an example of a MRSS feed that is compatible with Zype. In order to properly import videos from an MRSS feed, you must format your feed to match this example.

{% highlight xml %}
<rss xmlns:media="http://search.yahoo.com/mrss/" xmlns:dcterms="http://purl.org/dc/terms/" version="2.0">
    <channel>
        <title>MRSS Format Example</title>
        <link/>
        <description/>
        <item>
            <title>My Video 1</title>
            <guid>0_qwert</guid>
            <link>0_qwert</link>
            <pubDate>Mon, 16 May 2016 20:42:45</pubDate>
            <endDate/>
            <media:content url="http://www.mrss-example.com/p/123/sp/12300/playManifest/entryId/0_qwert/flavorId/0_4lidycd2/protocol/http/format/url/a.mp4?clientTag=feed:abcd" duration="31" width="1920" height="1080">
                <media:title>My Video 1</media:title>
                <media:description>Description text goes here</media:description>
                <media:keywords>example, video, mrss</media:keywords>
                <media:thumbnail url="http://mrss-example-img.revnm.com/p/123/sp/12300/thumbnail/entry_id/0_qwert/version/100012/acv/202/width/1920/height/1080" width="1920" height="1080" />
                <media:category>
                    Example Category
                </media:category>
                <media:player url="http://www.mrss-example.com/kwidget/wid/_123/entry_id/0_qwert/ui_conf" />
            </media:content>
        </item>
        <item>
            <title>My Video 2</title>
            <guid>0_123abc</guid>
            <link>0_123abc</link>
            <pubDate>Mon, 16 May 2016 20:35:14</pubDate>
            <endDate/>
            <media:content url="http://www.mrss-example.com/p/123/sp/12300/playManifest/entryId/0_123abc/flavorId/0_thxezdy6/protocol/http/format/url/a.mp4?clientTag=feed:abcd" duration="52" width="1920" height="1080">
                <media:title>My Video 2</media:title>
                <media:description>Description text goes here</media:description>
                <media:keywords>example, video 2, mrss</media:keywords>
                <media:thumbnail url="http://mrss-example-img.revnm.com/p/123/sp/12300/thumbnail/entry_id/0_123abc/version/100012/acv/212/width/1920/height/1080" width="1920" height="1080" />
                <media:category>
                    Example Category
                </media:category>
                <media:player url="http://www.mrss-example.com/kwidget/wid/_123/entry_id/0_123abc/ui_conf" />
            </media:content>
        </item>
    </channel>
</rss>
{% endhighlight %}

### Explanation of MRSS Elements

Element | Function
--------- | --------
channel:title   | Sets the title of the channel (the set of your video items). Zype will interpret this as the main category title. *required*
item:guid        | The unique ID of the item *required*
item:pubDate     | The publication date of the item *required*
media:content:url     | The link to the mp4 of your video item *required*
media:content:duration     | The duration in seconds of your video item *required*
media:content:width     | The width in pixels of your video item *required*
media:content:height     | The height in pixels of your video item *required*
media:title     | The title of your video item *required*
media:description     | The description of your video item
media:keywords     | The keywords to associate with your video item. Must be a comma-delimeted list
media:thumbnail:url     | The link to the jpg or png of your video thumbnail *required*
media:thumbnail:width     | The width in pixels of your video thumbnail *required*
media:thumbnail:height     | The height in pixels of your video thumbnail *required*
media:category     | The category value of your video item. Will be categorized under the main category heading as set in the channel:title, or in another category if specified while importing



<style type="text/css">
    figure.highlight {
        margin-left: 0;
        width: 1300px;
    }
</style>
