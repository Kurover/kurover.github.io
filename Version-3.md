# Version 3
This iteration focuses on adding more assets (Background, UI theme, Icon, etc.). I'm also rewriting the HTML and CSS mainly to reorganize the structure, naming, and to better use Jekyll automation, since rebuilding it is more manageable to me than editing it.

## Current Changes
Changes may or may not immediately deployed on main site.
- Rebuild HTML and CSS.
- Compress HTML via [Jekyll Compress HTML](https://github.com/penibelst/jekyll-compress-html).
- Compress CSS via built-in Jekyll compression by converting it to SCSS. I'm not going to use the SASS feature because I don't need it.
- Navigation:
  - Removed title for now. Custom logo later?
  - Custom icon, finaly. Slightly smaller width.
  - Mobile view navigation now sticky on bottom.
- Index:
  - Added custom layout with big button and less text, turning it into a hub page. Prototype on the [Lab Page](https://kurover.github.io/lab) | [New Home](https://kurover.github.io/lab/new-home).
- Gallery:
  - Use "_data" for art list. I like this way more so far, easy to manage.
  - Use flexbox better for art list, using flex horizontal line to divide row instead of every 2-3 art in a div to break row. This reduces nesting divs significantly, though the new zoom function balances out that div usage lol.
  - Fixed height and width (visually) frame for the list. Hover to expand to the side if it's stacked on a row.
  - Remove zoom hover, instead click-to-zoom (popup-like). Honestly still on the fence with this one. But I don't want to bite the bullet and brute force it with massive lightbox feature (so many duplicate on link, label, input, and button ugh..).
  - Caption on hover only, mainly to reduce reading in an art-based page.
  - Sticky and bigger category selector with integrated pagination system (on animation only for now) instead of that gimmicky hovering tabs within tab on the side.
  - :red_square: Removed version changing (normal or loop) for now. Waiting for better system.
- Blog:
  - N/A
- File (AKA Download):
  - Renamed to file as it's shorter and has better context, I think.
- Links:
  - N/A
- 404 Page:
  - Not a linktree clone anymore. Much more compact.
  - :yellow_square: Asset still pending (icon and background). 
- Old page is still up and online. Blog entry still use the old system. As of why I deploy the new one immediately despite being unfinished is that I honestly don't like the old one.

## :green_square: TO-DO

### :zap: Big stuff
- :star: Home to be a game-esque menu screen with funny li'l companion. Less fluff but more in the face for everything I can offer.
  - :star: Background, night scenery either on the tower foreseeing the sea or in front of the tower entrance.
  - :blush: Illith portrait (entrance, 2-3 idle, speaking).
  - Custom navigation asset, different from general nav icon.
- :sleeping: Custom animated 404 error page on the sea.
- :envelope: Large navigation buttons, at least 96px and wide.
- :star: Custom page to test cursor.

### :blossom: Sprite / Icon
- :star: Home: Buttons with border and background, separated. Separate from main sprite file (since it's only at home).
- :leaves: Border: Navigation, Gallery, Tooltip, Button.
- :leaves: Navigation: Home, Gallery, Blog, Download, Links, "More"?
- :leaves: Links: Mail, Misskey, Twitter, Discord, Github.
- :seedling: Links: Pixiv, Steam, Lab page, Old page.
- :herb: Flavor: Arrows, Close Button, Image Loading Placeholder, Bottom border decor.

### :snowflake: Misc Stuff (low-priority)
- :blush: Illith nag / fixed companion (bottom left). Clickable to go to top and point of interest.
- :memo: 404 page where its text is a windows error popup, can be minimized, maximize is greyed out, and close to go to secret place.