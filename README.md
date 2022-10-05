## Overview

## Creating and editing presentations

1. Install VS Code with the extension vscode-reveal


## Header Section of your file
```yaml
---
title: QField
description: QField Feature presentation
theme: white
customTheme: themes/pitch-theme
---
```

Use `pitch-theme` for heavy-titled slides for pitches like this:
<image of marcos slide>

Use `teaching-theme` for slimmer font for workshop and teaching presentations.
<image of teaching slide>

## Build the slides

    docker run --rm -v $(pwd)/slides:/slides -v $(pwd)/html:/html webpronl/reveal-md:latest /slides --static /html --assets-dir assets --static-dirs _assets/theme

## Tipps and Tricks

### Overriding font styling

If you want to override section levels of `#QField` style to pink, you can
do this manually with CSS inlining:

```html
<h1 style="color:pink">QField</h1>
```

Classes used in <span> (not only)

### Images

If you want to set an image as slide background, use this:

```html
<!-- .slide: data-background="./assets/mercator-bw.jpg"-->
```

To set the size of the image, use this syntax:

```md
![](./assets/qfield_device_landscape.png){width="100%" height="30%"}
```

Note that you need to specify both `width` and `height`.

### Handling multiple lines


### Having two or more equal sized columns

If you want to place text and other elements, you can use containers:

```html
<div class="container">
<div class="col">column 1</div>
<div class="col">column 2</div>
<div class="col">column 3</div>
</div>
```

Please not that the HTML tags MUST be without any indentation, otherwise the
content is not correctly parsed from the `.md` file.
