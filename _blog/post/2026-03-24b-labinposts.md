---
layout: blog-post
og-title: Zanster Blog
og-type: blog
groups: blog-post

title: Lab in Posts
description: Testing a new feature in a posts
created-at: 2026-03-24T13:34:23+0700
modified-at: 2026-03-25T11:51:46+0700
---

# Hello, Don't Mind This Post!

{% include blog-toc.md %}

This post is to test out (automatic) table of contents styling! To make it scalable :tm: we use jekyll include to inject the tags after the first header as following:

```
{% raw %}
{% include blog-toc.md %}
{% endraw %}

Add "{% raw %}{: .no_toc }{% endraw %}" after a header to prevent it from indexed.

```

Previously I tried to make it numbered like normal but styling it is quite difficult since I have no control over what tags is generated on the table of content table. This iteration use no number but rely on the lines instead to give context which's content is which.

# Header 1
Lorem?

## Body
Body of lorem.

## Left Leg
Left leg of lorem.

### Left Leg's Big Toe of Overflowing Division
Ermm what the sigma?

## Right Leg
Right leg of lorem. Said to bring good luck.. somehow?

# Topic 3
UOGGGGHHH KANIIII!11!!! (Microsoft pls dont ban me)
