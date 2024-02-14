---
draft: false
---

## To move the arrows below the carousel:
```css
.pp-content-post-carousel .owl-theme .owl-controls .owl-buttons div,
.pp-content-post-carousel .owl-nav button {
    position: relative;
}

.pp-content-post-carousel .owl-nav {
    display: flex;
    justify-content: center;
    gap: 44px;
}

.pp-content-post-carousel .owl-nav button.owl-prev {
    left: 0 !important;
}

.pp-content-post-carousel .owl-nav button.owl-next {
    right: 0 !important;
}

.owl-prev,
.owl-next {
    padding: 0 !important;
}

.owl-prev span:first-of-type svg path,
.owl-next span:first-of-type svg path {
    display: none !important;
}

.owl-prev span:first-of-type svg,
.owl-next span:first-of-type svg {
    width: 29px !important;
    height: 10px !important;
    content: ' ' !important;
    background-repeat: no-repeat;
    background-size: 29px !important;
}

.owl-prev span:first-of-type svg {
    background-image: url('SVG HERE') !important;
}

.owl-next span:first-of-type svg {
    background-image: url('SVG HERE') !important;
}
```

Use [SVG to CSS converter](https://www.svgbackgrounds.com/tools/svg-to-css/) to get the correct format for the backgrounds.