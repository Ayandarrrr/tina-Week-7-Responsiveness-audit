# tina-Week-7-Responsiveness-audit
 tina-audit




## Audit Information

**Page Audited:** Mzansi Eats Food Delivery

**Screen Sizes Tested:**

* Mobile (375px)
* Tablet (768px)
* Desktop (1280px)



## Issue 1: Hero Image Overflow

### Problem

The hero image used a fixed width of 1200px, causing horizontal scrolling on smaller screens.

### Fix Applied

```css
.hero img {
    width: 100%;
    height: 400px;
    object-fit: cover;
}
```



## Issue 2: Card Grid Overflow

### Problem

The card grid used fixed column widths (`repeat(4, 250px)`), causing content to overflow on smaller screens.

### Fix Applied

```css
.card-grid {
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
}
```



## Issue 3: Contact Section Width

### Problem

The contact section used a fixed width of 800px, which exceeded the viewport on mobile devices.

### Fix Applied

```css
.contact-inner {
    width: 90%;
    max-width: 800px;
    margin: 0 auto;
}
```



## Issue 4: Mobile Layout Issues

### Problem

The header, footer, and contact section did not adapt properly to smaller screens.

### Fix Applied

Media queries were added to:

* Stack header items vertically.
* Wrap navigation links.
* Change the contact section to a single column.
* Stack footer content vertically.

```css
@media (max-width: 768px) {
    header {
        flex-direction: column;
    }

    .contact-grid {
        grid-template-columns: 1fr;
    }

    footer {
        flex-direction: column;
    }
}
```



## Summary

Four responsiveness issues were identified and fixed. The page now adapts correctly across mobile, tablet, and desktop screen sizes, improving usability and accessibility.

