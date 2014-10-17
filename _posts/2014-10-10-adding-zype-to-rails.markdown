---
layout: post
title:  "Adding Zype to a Rails Application"
date:   2014-10-10 15:53:00
categories: rails ruby
---
At Zype, we use our [Zype Gem](link: https://github.com/edla/zype-cli) to
build fully branded video experiences on the web. Below is a step-by-step
guide for how to integrate the Zype Gem into a Rails App.

1\. Create a new Rails App
{% highlight ruby %}
  $rails new
{% endhighlight %}

2\. Add the Zype Gem to your Gemfile and bundle.
  {% highlight ruby %}
    gem 'zype', :git => 'git://github.com/edla/zype-cli.git'
  {% endhighlight %}

3\. Add your Zype Configurations to the initializers

  {% highlight ruby %}
  # Create a new file config/initializers/zype.rb

  Zype.configure do |config|
    config.api_key = {api_key}
    config.host    =  "api.zype.com"
    config.port    =  80
    config.use_ssl = false
  end
  {% endhighlight %}


*You can find your api key from the [Zype Platform](http://admin.zype.com/site/api)*

4\. Add the following javascript to your layout.html.erb to be able to power the appropriate player javascript.
{% highlight html %}
<script type="text/javascript" src="http://api.zype.com/player.js"></script>
<script type="text/javascript"> zype.player_key = {player_key};</script>
{% endhighlight %}

*You can find your player key from the [Zype Platform](http://admin.zype.com/site/api)*

5\. Create a new instance of your Zype Client so that you can query the Zype Platform
to get your videos, playlists, categories, zobjects, and appropriate video players
from your Rails App.
{% highlight ruby %}
@zype = Zype::Client.new
{% endhighlight %}


6\. Some things that you can do with your Zype Client that could be useful for a web app:

- Get all your videos
{% highlight ruby %}@zype.videos{% endhighlight %}

- Get a specific video
{% highlight ruby %}
@zype.videos.find(params[:video_id])
{% endhighlight %}


- Change pagination
{% highlight ruby %}
@zype.videos.all(per_page: 500)
{% endhighlight %}

- Pagination
{% highlight ruby %}
@zype.videos.all(page: 2, per_page: 50)
{% endhighlight %}

- Sort (ex. sort by video title)
{% highlight ruby %}
@zype.videos.all(sort: ‘title’, order: ‘asc’)
{% endhighlight %}

- Query by zobject type (example: genre)
{% highlight ruby %}
@zype.zobjects.all(‘zobject_name’, {})
{% endhighlight %}

- Query videos by category (example genre)
{% highlight ruby %}
@zype.videos.all(category: {genre: ‘Comedy’})
{% endhighlight %}


- Get the player for a video
{% highlight ruby %}
@video = @zype.videos.find(params[:video_id])
@player = @video.player(player_opts)
{% endhighlight %}

7\. Display the video player in your HTML view
{% highlight erb %}
<%= @player['body'].html_safe %>
{% endhighlight %}
