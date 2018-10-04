---
layout: platform
title: Zype Developer Portal | Google Analytics Integration
permalink: /platform_docs/google_analytics/
redirect_to: https://support.zype.com/hc/en-us/articles/216673017
---
## Enabling Google Analytics integration
Zype Analytics can integrate with Google Analytics to deliver a consolidated source of analytics for your web destination.

<div style="width: 100%;">
<div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
<a href="#1">
Requirements</a>
</div>
<div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
<a href="#2">
Enabling Google Analytics Integration</a>
</div>
<div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
<a href="#3">
Events Overview</a>
</div>
</div>

<hr id="1">

## Requirements

To use Google Analytics with Zype Analytics you need to have a [Google Analytics](http://www.google.com/analytics/) account and a web tracking code installed on your web destination.

A web tracking code for Google Analytics looks similar to the following:

<pre>
&lt;script&gt;
  (function(i,s,o,g,r,a,m){i[&#39;GoogleAnalyticsObject&#39;]=r;i[r]=i[r]||function(){
    (i[r].q=i[r].q||[]).push(arguments)},i[r].l=1*new Date();a=s.createElement(o),
    m=s.getElementsByTagName(o)[0];a.async=1;a.src=g;m.parentNode.insertBefore(a,m)
  })(window,document,&#39;script&#39;,&#39;//www.google-analytics.com/analytics.js&#39;,&#39;ga&#39;);

  ga(&#39;create&#39;, &#39;YOUR-TRACKING-ID&#39;, &#39;auto&#39;);
  ga(&#39;send&#39;, &#39;pageview&#39;);
&lt;/script&gt;
</pre>



<hr id="2">

## Enabling Google Analytics integration

To enable Google Analytics integration select the 'Enable Google Analytics' option under 'Zype Analytics settings'. The integration will use the existing Google Analytics tracking object on the page so you don't need to enter your Google Analytics Tracking ID.

You can optionally change the tracking object name. Most installations use the default name 'ga'. If you have not changed the name of the tracking object on your web destination you should use the default setting.

![google analytics]({{site.url}}/assets/Analytics/analytics.png)

<hr id='3'>

## Events Overview

After you've enabled Google Analytics integration and watched a few videos on your web destination you will start seeing the following events in your Google Analytics dashboard.

![consumer information]({{site.url}}/assets/Analytics/report.png)

<p><strong>JW Player Video</strong>: This category contains events for starts, stops, resumes and buffers along with the name of the video.</p>
<p><strong>JW Player Video Plays</strong>: This category contains play events along with the name of the video and the referring URL.</p>
<p><strong>JW Player Video Completes</strong>: This category contains completion events along with the name of the video and the referring URL.</p>
