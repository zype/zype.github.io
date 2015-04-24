---
layout: platform
title: Zype Developer Portal | Platform Docs
permalink: /platform_docs/zobjects/
---
## Zobjects
A Zobject is additional metadata that you can create and associate with your videos.

<div style="width: 100%;">
  <div style="margin: 20px;"><span class="fa fa-file-text" style="margin-right: 4px;"></span>
    <a href="#1">
    Zobjects on the Zype Platform</a>
  </div>
</div>

<hr id="1">

## Zobjects on the Zype Platform
A central component of the Zype Platform is a 'Zobject.' A Zobject is additional
metadata that you can create and associate with your videos. In the tutorial below,
we will show how to associate an the actor John Boyega to the newest Star Wars trailer.
To do this, we will create a Zobject type called actors and then create a Zobject actor for John Boyega.
Lastly, we will associate John Boyega with the Star Wars trailer.

**Step 1: Create a Zobject type**

Since Zobjects can be whatever metadata you want, you first need to create a Zobject type
to define the your Zobject data structure. You can access Zobject types using the
settings toolbar at the top of your dashboard.

![zobject type settings]({{site.url}}assets/Zobjects/nav_zobject.png)

We will call our Zobject type actor so that it is easy to reference.

![zobject type title]({{site.url}}assets/Zobjects/new_zobject.png)

For our actor Zobject, we need a field for name, which is a string.
You can use any familiar data structure when creating a Zobject type.
You can access Zobject types using the settings toolbar at the top of your dashboard. To add an attribute,
click the button Add Attribute. You can always return to this page to add additional
attributes.

![zobject type add attribute]({{site.url}}assets/Zobjects/new_attribute.png)

**Step 2: Add an actor Zobject Sylvester Stallone for the Zobject type actor**

Click on your Zobject in the right hand navigation.

![access zobject]({{site.url}}assets/Zobjects/actors_nav.png)

Next, click on 'Add New Actor'. You will be prompted to fill out all the information
that you laid out when you created your Zobject type. We have included keyword
and description as additional fields that you can leave blank.

![insert actor info]({{site.url}}assets/Zobjects/stallone_actor.png)

**Step 3: Link the Zobject to the video**

Click on the Videos tab to associate videos with the actor

![associate videos]({{site.url}}assets/Zobjects/select_movie.png)

Once you click save, your Zobject will be associated with that video! You can double
check by going to the video and looking at its metadata.

![video metadata]({{site.url}}assets/Zobjects/video_assoc.png)
