# Page Gallery Colors

### Snippet

Also available [here](https://github.com/t-if/gastrodon/blob/main/Snippets/Gallery%20Colors.css)

```css
css
/* original by t-if  
🔗https://github.com/t-if */

/* @settings

name: Page Gallery Colors
id: css-page-gallery-colors
description: Change colors of the page gallery plugin.
settings:
    - 
        id: gallery-bg-color-focus
        title: Focus Background Color
        type: variable-themed-color
        format: rgb
        default-light: '#'
        default-dark: '#'
    -
        id: gallery-bg-color-focus-hover
        title: Focus Hover Background Color
        type: variable-themed-color
        format: rgb
        default-light: '#'
        default-dark: '#'
    -
        id: gallery-bg-color-selected
        title: Selected Background Color
        type: variable-themed-color
        format: rgb
        default-light: '#'
        default-dark: '#'
    -
        id: gallery-bg-color-selected-shadow
        title: Selected Background Shadow Color
        type: variable-themed-color
        format: rgb
        default-light: '#'
        default-dark: '#'
    -
        id: tile-image-bg-color
        title: Tile Image Background Color
        type: variable-themed-color
        format: rgb
        default-light: '#'
        default-dark: '#'
    -
        id: tile-image-bg-color-shadow
        title: Tile Image Background Shadow Color
        type: variable-themed-color
        format: rgb
        default-light: '#'
        default-dark: '#'
    -
        id: tile-image-box-shadow
        title: Tile Image Box Shadow Color
        type: variable-themed-color
        format: rgb
        default-light: '#'
        default-dark: '#'
*/

.page-gallery__views-header-item:focus,
.page-gallery__views-header-item:hover {
  background: linear-gradient(to bottom right, var(--gallery-bg-color-focus), var(--gallery-bg-color-focus-hover));
  cursor: pointer;
}

.page-gallery__views-header-item.selected {
  background: linear-gradient(to bottom right, var(--gallery-bg-color-selected), var(--gallery-bg-color-selected-shadow));
  box-shadow: 2px 2px 2px '#';
}

.page-gallery__views-header-item-count {
  margin-left: 0.2em;
}

.page-gallery__tile-image--content {
  background: linear-gradient(to bottom right, var(--tile-image-bg-color), var(--tile-image-bg-color-shadow));
  border-radius: var(--border-radius, 10px);
  box-shadow: 2px 2px 2px var(--tile-image-box-shadow);
  display: block;
  position: relative;
  text-decoration: none !important;
}

.page-gallery__tile-image--content-sizer {
  display: block;
  padding-bottom: var(--image-height);
}

.page-gallery__tile-image--content-wrapper {
  bottom: 0;
  left: 0;
  overflow: auto;
  padding: 0.5em;
  position: absolute;
  right: 0;
  top: 0;
}

body.theme-dark .page-gallery__views-header-item:focus,
body.theme-dark .page-gallery__views-header-item:hover {
  background: linear-gradient(to bottom right, var(--gallery-bg-color-focus-dark), var(--gallery-bg-color-focus-hover-dark));
}

body.theme-dark .page-gallery__views-header-item.selected {
  background: linear-gradient(to bottom right, var(--gallery-bg-color-selected-dark), var(--gallery-bg-color-selected-shadow-dark));
}

body.theme-dark .page-gallery__tile-image--content {
  background: linear-gradient(to bottom right, var(--tile-image-bg-color-dark), var(--tile-image-bg-color-shadow-dark));
  box-shadow: 2px 2px 2px var(--tile-image-box-shadow-dark);
}
```

## Showcase

![image](https://github.com/user-attachments/assets/6b38e065-e238-4417-852a-18aacad80de0)

![image](https://github.com/user-attachments/assets/5b793370-698b-4521-b8a0-0b01adfb99a5)
