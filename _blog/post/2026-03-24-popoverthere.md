---
layout: blog-post
og-title: Zanster Blog
og-type: blog
groups: blog-post

title: HTML Popover Tag
description: Talking about the current image Zoom Popup mechanism
created-at: 2026-03-24T00:48:54+0700
modified-at:
---

# A Popup I Cannot Posses

During the Gallery Zoom Title rewrite. I was mulling about the zoom/pop mechanism. "Is this one really the better one out of the bunch?" I thought, while forgetting why I chose this mechanism in the first place. I avoided checkbox/radio toggle method because I thought there's gonna be a lot of input + label tags with unique ID in the HTML, which is true. There's a way to avoid ID by nesting the input inside the label but that also has issue in accessibility.

<input type="checkbox" id="gal-close_sys">
<div class="gallery-lists img-px compact">
  <div class="gallery-list" tabindex="-1">
    <p>This thing's here</p>
    <div class="gallery-image-wrapper">
      <div class="gallery-image-topbar">
        <label for="gal-close_sys" class="gallery-close"></label>
      </div>
      <div class="gallery-image" tabindex="0">
        <img src="/img/illith-flustered.png">
      </div>
    </div>
  </div>
  <div class="gallery-list" tabindex="-1">
    <p>"Yes, I'm the cutest~"</p>
    <div class="gallery-image-wrapper">
      <div class="gallery-image-topbar">
        <label for="gal-close_sys" class="gallery-close"></label>
      </div>
      <div class="gallery-image" tabindex="0">
        <img src="/img/illith-3.png">
      </div>
    </div>
  </div>
</div>

Slight tangent; I wanted to make the website to be "tab navigation"-friendly in order to limit myself from going overboard, which I did with the recent CSOS and that one took a long time to cook up. It's nice once in a while but I sure don't want to go to that rabbit hole too much. I'll keep them under the basement until proven awesome.

Anyway, using input + label makes the tab-nav very annoying. You must press spacebar to even zoom the image. With the current code, I could make it so if you're in gallery mode, pressing arrow key (radio like category switch) or tab (:has input:checked so the zoomy persist) allows you to switch image during zoomy. I was kinda convinced with the radio but then you cannot scroll with it and the input is confusing since you need to nav to the image to scroll then back to radio if you want to keep scrolling. I can add MORE label after the image, which only display:block if image is focused but wowie that is even MORE tags for a single image!

One other similar method is having the gallery and the zoomy to be in separate container. So if you toggled an image, you will be focused to the zoomy mode, which you can scroll images like image viewer do. This one is cool, but I'm afraid of the long-term performance and HTML bloat. Sure, even if I scale to a thousand image, it won't be as bad as badly written javascript but I do like the (sensible) micro-optimization aspect of web building.

Other mechanism I'm eye-ing for is the HTML popover. It's basically input + label but better. You can press escape to exit out of it, which is, not gonna lie, very enticing. That might be the best method moving forward (and if I decide to hit the id spam in my foot) but I'll need to try that out first when I do some experiment.