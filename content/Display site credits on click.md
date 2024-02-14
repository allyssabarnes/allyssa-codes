---
draft: false
---

## Setup modules

Create 2 text modules: one for the text that will be displayed all the time and a second which will be displayed upon click.

In the first module, add the credits link with a class of `.site-credits-link`.

Add an id of `#site-credits-content` to the 2nd module.

## Add CSS
```scss
.site-credits-link:hover {
    cursor: pointer;
}

body:not(.fl-builder-edit) #site-credits-content {
    display: none;
    overflow: hidden;
}
```

## Add JS
```javascript
var coll = document.getElementsByClassName("site-credits-link");
var i;

for (i = 0; i < coll.length; i++) {
  coll[i].addEventListener("click", function() {
    this.classList.toggle("active");
    var content = document.getElementById('site-credits-content');
    if (content.style.display === "block") {
      content.style.display = "none";
    } else {
      content.style.display = "block";
    }
  });
}
```