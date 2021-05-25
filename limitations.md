---
description: 'What we didn''t get to, and how we would fix it if we had time.'
---

# Limitations

## Doodles don't work with really long pages

The DoodleCanvas element is capped at 10k pixels tall, because it gets too slow when the canvas is massive. To fix this, we could tile smaller canvases to cover the entire screen.

## Doodles only work on some webpages

Currently the DoodleCanvas is hardcoded to anchor on the  `main-content` element, which only exists on certain pages. We chose this element for our MVP because it is present on the PolyPublishing site, and prevents users from doodling on the non-content parts of the page \(sidebar, footer, etc.\) This could probably be changed to the `body` element, allowing it to work on all pages. The only downside to this is users could doodle on any part of the page. However, this is consistent with current Hypothes.is functionality, so it is likely not a problem.

## Doodles don't work with changing page sizes

When a doodle is drawn, it's positioned relative to the exact pixel coordinates it previously was in the page. If, when re-displaying it, the page width is different, then often it won't be doodling over the element that it used to, as that element has moved.

This is fixable, but with a significant amount of work: instead of storing coordinates relative to the DoodleCanvas anchor element \(`main-content` for now\), we could determine which element to attach it to and store coordinates relative to that. This, however, will take a significant amount of reworking how doodles are saved and displayed.

## 



