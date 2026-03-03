---
layout: blog-post
og-title: Zanster Blog
og-type: blog
groups: blog-post

title: Post I go
description: Random post number 1
---

{% assign posts = site.lab | where: "name", "Cursor Simulator" %}

# Welcome

**Hello world**, this is my first Jekyll blog post.

I hope you like it!

Yeah right, anyway- I decided to make a makeshift "post" type after mulling it over. I tried the _posts system in the past, didn't like it. I tried it again, still don't. The link pointing to like `site/2026/01/02/post.html` is mildly infuriating to me and we can't really change the system. So with a little hackjob here and there, I expanded the "blog" collection into a group category via front-matter, voila!

Having `groups: blog-post` for this page means it belong top the fake post page system, while `groups: blog` is the original collection. So the current blog page liquid are these:

```
{% raw %}
{% assign blogs = site.blog | where: "groups","blog" | sort: "order" %}
{% for blog in blogs %}
  <li class="blog-list">
    <a href="{{ blog.url }}" target="_blank">{{ blog.title-short }}</a>
    <p>{{ blog.description }}</p>
  </li>
{% endfor %}
{% endraw %}
```

Yeah, for now the mini post is located at the home page as I'm still drafting the layout for blog page. But first I do need to complete the {% for post in posts %}[cursor simulator]({{ post.url }}){% endfor %}..

Technical-side aside, I wanted to use this post-like system for quick easy yap where I don't have to assign `<p></p>` and all that just to write a couple of points without getting mad about the date in the link path. Who knows, maybe I spam enough of these, I can make a full glossary out of it~!

Still need to work on the colors, at the very least I want it good for light reading with enough attention-grabbing element on whatever its assigned for a bit of oomph.

