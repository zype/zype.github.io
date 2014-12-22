---
layout: platform
title: Zype Developer Portal | Platform Docs
permalink: /platform_docs/zobjects/
---
##All About Zobjects
The Zype Platform is feature rich, so we want to provide you with a place to learn more about it.
Below are a bunch of short tutorials (with pictures!) to help you with zobjects.

<div style="width: 100%;">
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
    <a href="#1">
    Zobjects on the Zype Platform</a>
  </div>
</div>

<hr id="1">

## Zobjects on the Zype Platform
A central component of the Zype Platform is a 'Zobject.' A zobject is additional
metadata that you can create and associate with your videos. In the tutorial below,
we will show how to associate an the actor John Boyega to the newest Star Wars trailer.
To do this, we will create a zobject type called actors and then create a zobject actor for John Boyega.
Lastly, we will associate John Boyega with the Star Wars trailer.

**Step 1: Create a Zobject Type**

Since zobjects can be whatever metadata you want, you first need to create a zobject type
to define the your zobject data structure. You can access zobject types using the
settings toolbar at the top of your dashboard.

![zobject type settings](http://i.imgur.com/tlg7ik8.png)

We will call our zobject type actor so that it is easy to reference.

![zobject type title](http://i.imgur.com/tEzQf7F.png)

For our actor zobject, we need a field for name, which is a string.
You can use any familiar data structure when creating a zobject type.
You can access zobject types using the settings toolbar at the top of your dashboard. To add an attribute,
click the button Add Attribute. You can always return to this page to add additional
attributes.

![zobject type add attribute](http://i.imgur.com/DOq76qY.png)

**Step 2: Add an Actor Zobject John Boyega for the Zobject Type Actor**

Click on your Zobject in the right hand navigation or via the appropriate tile on
the dashboard home screen.

![access zobject](http://i.imgur.com/kA0xlr7.png)

Next, click on 'Add New Actor'. You will be prompted to fill out all the information
that you laid out when you created your zobject type. We have included keyword
and description as additional fields that you can leave blank.

![insert actor info](http://i.imgur.com/oSewGUE.png)

**Step 3: Link the Zobject to the Video**

Click on the Videos tab to associate videos with the actor

![associate videos](http://i.imgur.com/mRdieLV.png)

Once you click save, your zobject will be associated with that video! You can double
check by going to the video and looking at its metadata.

![video metadata](http://i.imgur.com/bkPlwIV.png)
