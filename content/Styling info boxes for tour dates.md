---
draft: false
---

![](https://slabstatic.com/prod/uploads/c4fy7myx/posts/images/2YJXkz4rCAazaBt90h3ojMnr.png)

## Info Box Module Settings

![](https://slabstatic.com/prod/uploads/c4fy7myx/posts/images/7nAynP0JiP3LR7N7_rI_Y6HO.png)

![](https://slabstatic.com/prod/uploads/c4fy7myx/posts/images/bKMDhQyN4OR2bL24Zkj52eN9.png)

## Different types of buttons

The default styling for the buttons used a beige color. By adding classes to the infobox, we were able to style the low tickets and sold out buttons differently. We added `.low` to the infobox for low tickets and `.soldout` to the infobox for sold out dates.

## Code

```scss
#book-tour .pp-infobox {
    display: grid;
    grid-template-columns: 30% 70%;
}

/* Fix for grid not working correctly with info boxes */
#book-tour .pp-infobox::before {
    display: none;
}

#book-tour .pp-heading-wrapper {
    padding-right: 30px;
}

#book-tour .pp-infobox-title-wrapper {
    margin-left: 20px;
}

#book-tour .pp-infobox-description {
    display: grid;
    grid-template-columns: 67% 33%;
}

#book-tour .pp-description-wrap {
    padding-right: 30px;
}

#book-tour .pp-infobox-description p {
    margin-bottom: 0;
}

/* Styles the 3rd paragraph in the description differently */
#book-tour .pp-infobox-description p:nth-of-type(3n):last-of-type {
    color: #FFFCF4;
    font-family: headline;
    font-size: 15px;
    font-style: normal;
    font-weight: 400;
    line-height: normal;
    letter-spacing: 1.5px;
    text-transform: uppercase;
    margin-top: 10px;
}

#book-tour .pp-infobox-button a::after {
    content: "\e903";
    font-family: 'brownstone-boys-icons';
    font-size: 22px;
    font-weight: 400;
    height: 100%;
    vertical-align: text-top;
    padding-left: 10px;
}

#book-tour .pp-infobox-button a {
    color: #E3D6C0 !important;
    text-decoration: none;
}

/* Styles buttons for low tickets */
#book-tour .low .pp-infobox-button a {
    color: #BF9A64 !important;
}

/* Styles buttons for sold out dates */
#book-tour .soldout .pp-infobox-button a {
    color: #BC8D41 !important;
}

#book-tour .pp-infobox-button a:hover,
#book-tour .low .pp-infobox-button a:hover,
#book-tour .soldout .pp-infobox-button a:hover {
    color: #BC8D41 !important;
}

#book-tour .soldout .pp-infobox-button a:hover {
    cursor: default;
}

#book-tour .soldout .pp-infobox-button a::after {
    content: "";
}

@media only screen and (max-width: 992px) {
    #book-tour .pp-infobox {
        grid-template-columns: 40% 60%;
    }
    
    #book-tour .pp-infobox-description {
        grid-template-columns: 100%;
    }
    
    #book-tour .pp-more-link {
        padding-left: 0;
    }
    
    #book-tour .pp-infobox-title-wrapper {
        margin-left: 0;
    }
}

@media only screen and (max-width: 768px) {
    #book-tour .pp-infobox {
        grid-template-columns: 100%;
    }
    
    #book-tour .pp-description-wrap {
        padding-right: 0;
    }
    
    #book-tour .pp-heading-wrapper {
        padding-right: 0;
        padding-bottom: 20px;
    }
    
    #book-tour .pp-infobox-title {
        font-size: 22px;
        letter-spacing: 2px;
    }
    
    #book-tour .pp-infobox-description {
        font-size: 18px;
    }
}
```

[[code]] [[Beaver Builder]] [[Powerpack]] [[CSS]] 