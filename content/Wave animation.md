---
draft: true
---

## Add an html module with the following svg:
```xml
<svg class="waves" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 24 150 28" preserveAspectRatio="none" shape-rendering="auto">
            <defs>
                <path id="gentle-wave" d="M-160 44c30 0 58-18 88-18s 58 18 88 18 58-18 88-18 58 18 88 18 v44h-352z" />
            </defs>
            <g class="parallax">
                <use xlink:href="#gentle-wave" x="48" y="0" />
               
            </g>
        </svg>
    
```

## Customize with CSS
```css
/* Waves Animation start */
.hero_area {
    position: relative;
    height: 100vh;
    background-color: #fff;
}

.waves {
    position: absolute;
    width: 100%;
    height: 200px;
    min-height: 100px;
    max-height: 150px;
    bottom: 0;
    left: 0;
}

.parallax>use {
    animation: move-forever 10s cubic-bezier(.55, .5, .45, .5) infinite;
  fill: #54c0da;
}

@keyframes move-forever {
    0% {
        transform: translate3d(-90px, 0, 0);
    }

    100% {
        transform: translate3d(85px, 0, 0);
    }
}


/*Shrinking for mobile*/
@media (max-width: 768px) {
    .waves {
        height: 40px;
        min-height: 40px;
    }
}

/* Waves Animation end */
```

Preview here: [Html Css Wave Animation](https://codepen.com/allyssabarnes/pen/MWLeBRN)