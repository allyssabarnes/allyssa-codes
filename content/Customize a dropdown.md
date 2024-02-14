---
draft: false
---

![[dropdowns.png]]

## CSS
```css
select {
  /* Image 1 = Icon; Image 2 = Arrow */
  background-image: url(IMAGE 1), url(IMAGE 2);
  
  /* Position Image 1, then Image 2 */
  background-position: 10px center, right 10px center;
  
  /* Image 1 size, Image 2 size */
  background-size: 12px, 18px;
  
  /* More customizations to select box */
  background-repeat: no-repeat;
  border: 2px solid red;
  border-radius: 36px;
  color: red;
  font-family: Arial;
  font-size: 16px;
  font-style: normal;
  font-weight: 600;
  line-height: 1.4;
  padding: 8px 30px;
  
  /* Hide default arrow */
  -webkit-appearance: none !important;
  -moz-appearance: none !important;
}
```