## Overview

## Creating and editing presentations

1. Install VSCode with the extension vscode-reveal
2. Clone this repository, to re-use existing contents, and later add your contributions.
```{bash}
git clone git@github.com:opengisch/talks_revealmd.git
```
3. Create a new branch named after your new presentation
```{bash}
git checkout -b slides/<my-example-presentation>
```
4. Create a new markdown file, `<my-example-presentation>.md`.

## Header Section of your file

Start with adding a header section to the `.md` file:

```{yaml}
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

## Preview the slides

![](doc/img/reveal-md_code-plugin.png)

A comfortable way to edit and live-preview contents is using VSCode and enabling
the `VSCode Reveal` plugin. You can just click on the plugin on the left bar,
which features a slide overview and currently four toolbar buttons at the top.
If you split the editor right and click on `"Revealjs: Show presentation by
side"`, then you can instantly navigate through the current snapshot of your
presentation.

## Build the slides

If you like the docker way of doing things, simply render the slides like this:

```{bash}
docker run --rm -v $(pwd)/slides:/slides \
  -v $(pwd)/html:/html webpronl/ryeveal-md:latest /slides \
  --static /html --assets-dir assets --static-dirs _assets/theme
```

Alternatively, you can get the lastest stable version with the npm manager
(might need to upgrade/install npm before):

```{bash}
# Using Ubuntu
curl -fsSL https://deb.nodesource.com/setup_current.x | sudo -E bash -
sudo apt-get install -y nodejs
# sudo npm install -g npm@latest
npm install -g reveal-md
```

Build the slides with

```{bash}
reveal-md slides/qfield.md
```

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

```{html}
<!-- .slide: data-background="./assets/mercator-bw.jpg"-->
```

To set the size of the image, use this syntax:

```{md}
![](./assets/qfield_device_landscape.png){width="100%" height="30%"}
```

Note that you need to specify both `width` and `height`.

### Tables

### Handling multiple lines


### Having two or more equal sized columns

If you want to place text and other elements, you can use containers:

```{html}
<div class="container">
<div class="col">column 1</div>
<div class="col">column 2</div>
<div class="col">column 3</div>
</div>
```

Please not that the HTML tags MUST be without any indentation, otherwise the
content is not correctly parsed from the `.md` file.
