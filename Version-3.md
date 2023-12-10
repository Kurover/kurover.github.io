# Version 3
This iteration focuses on adding more assets (Background, UI theme, Icon, etc.). I'm also rewriting the HTML and CSS mainly to reorganize the structure, naming, and to betterr use Jekyll automation, since rebuilding it is more manageable to me than editing it.

## Current Changes
- Rebuild HTML and CSS.
- Compress HTML via [Jekyll Compress HTML](https://github.com/penibelst/jekyll-compress-html).
- Compress CSS via built-in Jekyll compression by converting it to SCSS. I'm not going to use the SASS feature because I don't need it.
- Navigation:
  - Removed title for now. Custom logo later?
  - Custom icon, finaly. Slightly smaller width.
  - Mobile view navigation now sticky on bottom.
- Index:
  - N/A
- Gallery:
  - Use "_data" for art list. I like this way more so far, easy to manage.
  - Use flexbox better for art list, using flex horizontal line to divide row instead of every 2-3 art in a div to break row. This reduces nesting divs significantly.
  - Fixed height and width (visually) frame for the list. Hover to expand to the side if it's stacked on a row.
  - Remove zoom hover, instead click-to-zoom (popup-like). More divs, so it balances out previous point lol.
  - Caption on hover only, mainly to reduce reading in an art-based page.
  - Sticky and bigger category selector with integrated pagination system (on animation only for now) instead of that gimmicky hovering tabs within tab on the side.
- Blog:
  - N/A
- File (AKA Download):
  - Renamed to file as it's shorter and has better context, I think.
- Links:
  - N/A
- Old page is still up and online. Blog entry still use the old system. As of why I deploy the new one immediately despite being unfinished is that I honestly don't like the old one.

## :green_square: TO-DO

### :zap: Big stuff
- :star: Main background - night scenery either on the tower foreseeing the sea or in front of the tower entrance
- :blush: Illith portrait (entrance, 2-3 idle, speaking)
- :sleeping: Stylla 404 error page on the sea
- :envelope: Large navigation buttons, at least 96px and wide.

### :blossom: Sprite / Icon
- :leaves: Border: Navigation, Gallery, Tooltip, Button
- :leaves: Navigation: Home, Gallery, Blog, Download, Links, "More"?
- :leaves: Links: Mail, Misskey, Twitter, Discord, Github
- :seedling: Links: Pixiv, Steam
- :herb: Flavor: Arrows, Close Button, Image Loading Placeholder

### :snowflake: Misc Stuff (low-priority)
- :blush: Illith nag / fixed companion (bottom left). Clickable to go to top and point of interest
- :memo: 404 page where its text is a windows error popup, can be minimized, maximize is greyed out, and close to go to secret place
