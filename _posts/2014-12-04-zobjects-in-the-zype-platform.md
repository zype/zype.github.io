---
layout: post
title:  "Zobjects in the Zype Platform"
date:   2014-12-04 12:37:55
categories: developers
redirect_to: https://support.zype.com/hc/en-us/sections/115002657128-Metadata
---

A central component of the Zype Platform is a 'Zobject.' A zobject is additional
metadata that you can create and associate with your videos. In the tutorial below,
we will show how to associate an the actor John Boyega to the newest Star Wars trailer.
To do this, we will create a zobject type called actors and then create a zobject actor for John Boyega.
Lastly, we will associate John Boyega with the Star Wars trailer.

**Step 1: Create a Zobject Type**

Since zobjects can be whatever metadata you want, you first need to create a zobject type
to define the your zobject data structure. You can access zobject types using the
settings toolbar at the top of your dashboard.

![zobject type settings]({{site.url}}/assets/Zobjects/nav_zobject.png)

We will call our zobject type actor so that it is easy to reference.

![zobject type title]({{site.url}}/assets/Zobjects/new_zobject.png)

For our actor zobject, we need a field for name, which is a string.
You can use any familiar data structure when creating a zobject type.
You can access zobject types using the settings toolbar at the top of your dashboard. To add an attribute,
click the button Add Attribute. You can always return to this page to add additional
attributes.

![zobject type add attribute]({{site.url}}/assets/Zobjects/new_attribute.png)

**Step 2: Add an Actor Zobject John Boyega for the Zobject Type Actor**

Click on your Zobject in the right hand navigation or via the appropriate tile on
the dashboard home screen.

![access zobject]({{site.url}}/assets/Zobjects/actors_nav.png)

Next, click on 'Add New Actor'. You will be prompted to fill out all the information
that you laid out when you created your zobject type. We have included keyword
and description as additional fields that you can leave blank.

![insert actor info]({{site.url}}/assets/Zobjects/stallone_actor.png)

**Step 3: Link the Zobject to the Video**

Click on the Videos tab to associate videos with the actor

![associate videos]({{site.url}}/assets/Zobjects/select_movie.png)

Once you click save, your zobject will be associated with that video! You can double
check by going to the video and looking at its metadata.

![video metadata]({{site.url}}/assets/Zobjects/video_assoc.png)
