# Tooltip Colors

Change color of Obsidian tooltips in Style Settings. 

### Snippet
Available for download [here](https://github.com/t-if/gastrodon/blob/main/Snippets/Tooltip%20Colors.css).

```css
/* @settings

name: Tooltip Colors
id: css-tooltip-colors
description: Change colors of tooltips.
settings:
    - 
        id: bg-color
        title: Background Color
        type: variable-themed-color
        opacity: true
        format: hex
        default-light: '#'
        default-dark: '#'
*/

body {
	--background-modifier-message: var(--bg-color)
}
```

## Showcase
![image](https://github.com/user-attachments/assets/afa59123-1493-4df1-bb58-2c33ddc83cdf) 
#### The dark/light mode values here have different opacities, if you're wondering why I needed this snippet.
![image](https://github.com/user-attachments/assets/93f37923-d015-4fd0-9356-aa201b11db82) 
