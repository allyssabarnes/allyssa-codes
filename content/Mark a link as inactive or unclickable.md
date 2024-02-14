---
draft: false
---


Here's how to make a link/button unclickable/inactive via CSS. This is great when you have a list of tour dates and want to mark one as sold out.

## CSS

```css
.soldout {
   pointer-events: none;
   cursor: default;
}
```

## Usage

Add the code above to your stylesheet. Then add the `soldout` class to your button or link.

## Source

Found here: [https://stackoverflow.com/questions/6727659/is-it-possible-to-make-an-html-anchor-tag-not-clickable-linkable-using-css](https://stackoverflow.com/questions/6727659/is-it-possible-to-make-an-html-anchor-tag-not-clickable-linkable-using-css)