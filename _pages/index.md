---
layout: defaults/page
permalink: index.html
narrow: true
---

{% include components/intro.md %}

[More about Ian LIM.]({{ site.baseurl}}{% link _pages/about.md %})

### What else?

I like to look around especially when researching at work or during leisure when something crops up on the mind. 

There are a bunch of tips about how to use Friday Theme. There's the three most-recent posts below, or here's [all posts by year.]({{ site.baseurl }}{% link list/posts.html %})

<div class="card mb-3">
    <a data-flickr-embed="true"  href="https://www.flickr.com/photos/vanganhxinh/7764826966/" title="look at me">
    <img class="card-img-top" src="https://farm8.staticflickr.com/7257/7764826966_6bf7380fd3_z.jpg" alt="look at me">
    </a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>
    <div class="card-body bg-light">
        <div class="card-text">This picture reminds me about Craftsman.</div>
    </div>
</div>

### Recent Posts

{% for post in site.posts limit:3 %}
{% include components/post-card.html %}
{% endfor %}


