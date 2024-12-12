# CSS Pseudo-element Style Inheritance Bug

This repository demonstrates an uncommon bug in CSS where styles applied to a pseudo-element (:before in this case) unexpectedly affect subsequent elements in the DOM. The problem is that the styles intended for only the first list item's marker also apply to subsequent list items.

## Bug Description
The bug occurs because of a lack of specificity. The `:first-of-type` selector only targets the first `<li>` element, but the style is not properly contained. The solution involves adding more specificity to isolate the style application.

## How to reproduce
1. Open `bug.html` in your web browser.
2. Observe that the blue, large '*' marker is applied to all list items, not just the first.