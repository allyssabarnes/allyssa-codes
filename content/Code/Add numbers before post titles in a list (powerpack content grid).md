---
draft: false
---

![[numbered-list.png|300]]

Add a powerpack content grid module with the class `numbered-posts`.

## CSS
```css
/* Centers titles vertically with numbers */
.numbered-posts .pp-content-post .pp-post-title {
    display: flex;
    justify-content: flex-start;
    align-items: center;
}

/* Styling the numbers */
.numbered-posts .pp-content-post .pp-post-title:before {
    color: #ED1C24;
    font-style: italic;
    font-size: 44px;
    margin-right: 30px;
    font-weight: 300;
    padding-left: 4px;
}

/* Setting the number before each title */
.numbered-posts .pp-content-post:nth-of-type(1) .pp-post-title:before {
    content: '1';
}

.numbered-posts .pp-content-post:nth-of-type(2) .pp-post-title:before {
    content: '2';
}

.numbered-posts .pp-content-post:nth-of-type(3) .pp-post-title:before {
    content: '3';
}

.numbered-posts .pp-content-post:nth-of-type(4) .pp-post-title:before {
    content: '4';
}
```
