---
description: 'What we didn''t get to, and how we would fix it if we had time.'
---

# Limitations

## Doodles don't work with really long pages

The DoodleCanvas element is capped at 10k pixels tall, because it gets too slow when the canvas is massive. To fix this, we could tile smaller canvases to cover the entire screen.

## Doodles don't work with changing page sizes

When a doodle is drawn, it's positioned relative to the element it covers. When re-displaying on doodle load, it's repositioned to stay over that element. However, if the user then changes page sizes after annotations are loaded, there's no code to keep it attaching to that element, and it instead remains in it's old position regardless of if the element moves or not.

## 



