---
layout: post
title:  "Russian Doll Caching in Rails 4"
date:   2014-10-24 10:57:55
categories: developers
---

While developing, we always keep the user experience in mind and one of the most important things for a content heavy application
is load times. In rails, this usually comes down to how quickly you can render the requested view. Today I want to take a quick look
at how to nest caching statements in rails 4 for maximum effectiveness.

### What is Russian doll caching?

Russian-doll caching is a convention used in Rails 4 to improve the load time of your views. It involves using nested fragment caching statements so that only the page content that has changed since the last request needs to be regenerated. All the other elements of the page are simply read from their still-valid caches.

Here’s an example of some nested fragment caching statements in a view for a gallery of videos:

![nested cache statements](http://i.imgur.com/cCQLi4g.png)

Each level of nesting ensures that you only pay to read the caches of the content nested above it, not regenerate it, when the content nested below it changes. This has a reverse cascading effect, so the more strategic you can be with your caching statements, the less time you’ll spend trying to re-render the page.

### Where should I start adding Russian doll caching?

The parts of your app that are viewed most often will likely be your best targets for russian doll caching. Anywhere that you’re displaying a mix of dynamic and static content is also a good target because you can eliminate the need to reload the entire page when only a portion of the content has changed.

Take a look at your views and see if you can compartmentalize them based on content, this will be easier if you’re already using partials in the same way.

Here’s a visual example of the nested nature of the caching statements from the code above:

![seeing the nests in your view](http://i.imgur.com/8PxC8mg.png)


### Further reading

You can read up about cache expiration and best practices from DHH himself:

[Here ](https://signalvnoise.com/posts/3112-how-basecamp-next-got-to-be-so-damn-fast-without-using-much-client-side-ui)  [- and here.](https://signalvnoise.com/posts/3113-how-key-based-cache-expiration-works)
