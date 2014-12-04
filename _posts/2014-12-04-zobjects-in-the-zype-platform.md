---
layout: post
title:  "Zobjects in the Zype Platform"
date:   2014-12-04 12:37:55
categories: developers
---

A central component of the Zype Platform is a 'Zobject.' A zobject is additional
metadata that you can create and associate to your videos. In the tutorial below,
we will be showing how to associate an actor to a video by creating a zobject type
called actors and then creating zobjects to link an actor to a movie. This is super helpful because the Zype API
gives all zobject information in a video request and you can query for videos
with a specific zobject value.

**Step 1: Create a Zobject Type**

Since zobjects can be whatever metadata you want, you first need to define the your
zobject data structure. You can access zobject types using the settings toolbar at
the top of your dashboard.

![zobject type settings](http://i.imgur.com/tlg7ik8.png)

We will call our zobject type actor so that it is easy to reference.

![zobject type title](http://i.imgur.com/tEzQf7F.png)

For our actor zobject, we need a field for name, which is a string.
You can use any familiar data structure when creating a zobject type.
You can access zobject types using the settings toolbar at the top of your dashboard. To add an attribute,
click the button Add Attribute.

![zobject type add attribute](http://i.imgur.com/DOq76qY.png)

**Step 2: Add a Zobject for your Zobject Type**

Click on your Zobject in the right hand navigation or via the appropriate tile on
the dashboard home screen.

![access zobject](http://i.imgur.com/kA0xlr7.png)

Next, click on 'Add New Actor'. You will be prompted to fill out all the information
that you laid out when you created your zobject type.

![insert actor info](http://i.imgur.com/oSewGUE.png)

**Step 3: Link the Zobject to the Video**

Click on the Videos tab to associate videos with the actor

![associate videos](http://i.imgur.com/mRdieLV.png)

Once you click save, your zobject will be associated with that video! You can double
check by going to the video and looking at its metadata.

![video metadata](http://i.imgur.com/bkPlwIV.png)
