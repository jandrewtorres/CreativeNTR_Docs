---
description: 'What we didn''t get to, and how we would fix it if we had time.'
---

# Limitations

## Doodles don't work with really long pages

The DoodleCanvas element is capped at 10k pixels tall, because it gets too slow when the canvas is massive. To fix this, we could tile smaller canvases to cover the entire screen.

## Doodles only work on some webpages

Currently the DoodleCanvas is hardcoded to anchor on the  `main-content` element, which only exists on certain pages. We chose this element for our MVP because it is present on the PolyPublishing site, and prevents users from doodling on the non-content parts of the page \(sidebar, footer, etc.\) This could probably be changed to the `body` element, allowing it to work on all pages. The only downside to this is users could doodle on any part of the page. However, this is consistent with current Hypothes.is functionality, so it is likely not a problem.



