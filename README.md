## Creating and editing presentations

1. Install VS Code wiht the extension vscode-reveal

2. 

## Header Section of your file
```yaml
---
title: QField
description: QField Feature presentation
theme: white
customTheme: themes/pitch-theme
---
```

Use pitch-theme for heavy titled talk-presentations like this:
<image of marcos slide>

Use teaching-theme for slimmer font for workshop and teaching presentations.
<image of teaching slide>

## Tipps and Tricks

### Override font style
If you want to override `#QField` style being pink, you can make it manually with CSS inline:
```html
<h1 style="color:pink">QField</h1>
```

### Using of images

When you want to have an image as background use this:
```html
<!-- .slide: data-background="./assets/mercator-bw.jpg"-->
```

To set the size of the image use this syntax:
```md
![](./assets/qfield_device_landscape.png){width="100%" height="30%"}
```

