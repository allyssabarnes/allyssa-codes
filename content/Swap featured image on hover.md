---
draft: false
---

## Create a custom field for the alternate featured image
Create a custom field for an image that returns the image's URL.
## Use Powerpack's content grid with the following custom layout:
```html
[wpbb-if post:featured_image]
<div class="project-thumbnail grid-thumbnail">
<!-- main featured image -->
<img src="[wpbb post:featured_image size='full' display='url']" class="featured-image" />

<!-- alternate featured image to show on hover, set via CPT -->
<img src="[wpbb post:acf type='image' name='alternate_featured_image' image_size='full' display='url']" class="featured-image-alt" />
</div>
[/wpbb-if]
```

## Add this CSS:
```css
/* Swap featured image on hover */
#project-grid .project-thumbnail {
	position: relative;
	aspect-ratio: 2/3;
}

#project-grid .featured-image,
#project-grid .featured-image-alt {
	position: absolute;
}

#project-grid .featured-image-alt, 
#project-grid .pp-content-post:hover .featured-image {
   opacity: 0;
}

#project-grid .featured-image, 
#project-grid .pp-content-post:hover .featured-image-alt{
   opacity: 1;
}

#project-grid .pp-content-post  .featured-image,
#project-grid .pp-content-post  .featured-image-alt {
	-webkit-transition: opacity 0.7s ease-in-out;
	transition: opacity 0.7s ease-in-out;
}
```

## Add a class to the row
`#project-grid` was added to the row.