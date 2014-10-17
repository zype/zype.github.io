---
layout: post
title:  "Filter Playlists by a Category in a Rails App"
date:   2014-10-13 15:53:00
categories: rails ruby playlists categories
---

To organize your playlists using the Zype Platform, you can assign categories to
your playlists and filter your playlists based on a category and its value.
In this tutorial, I will walk through how to query for all the playlists that have
a category named ‘zone’ and a value of ‘home.’ At Zype, we use this
strategy to get all the playlists that we want to be displayed on the home page.

**Step 1: Go to admin.zype.com/categories and click the create new category button**

![new category](http://i.imgur.com/nweBnRo.png)

**Step 2: Fill out the category title and category values. You can have multiple
values (and you can always go back and edit these category values!)**

![new category](http://i.imgur.com/DmREstQ.png)


**Step 3: Create a playlist and assign it the Zone Category of home**

![new category](http://i.imgur.com/0algUs9.png)


**Step 4: In your Rails App, query for playlists that have the category zone value of home.**
{% highlight ruby %}
@playlists = @zype.playlists(zone: 'home')
{% endhighlight %}
