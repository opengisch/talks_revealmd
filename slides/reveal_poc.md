---
title: Reveal PoC
description: PoC for reveal.js
theme: theme/teaching-theme.css
customTheme: _assets/theme/teaching-theme
verticalSeparator: --v--
transition: none
revealOptions: {
  transition: 'none',
  slideNumber: false,
  overview: true,
  autoPlayMedia: true,
}
---

# Modernize the Talks repository
<h3 class=dark>And it's challenges</h3>

---

## Given state
- /talks repository with html
- /public-talks repository with some MARP prototyping

---

## Goal

- Decide for a way to go
- Set up a working repository
- PoC with QField Presentation
- Docs (!)

---

<div class="container">
<div class="col">
<h3> Pros of MARP </h3 >

- Markdown (of course)
- Integration VS Code
- Easy to build
</div>
<div class="col">
<h3> Cons of MARP </h3 >

- Limitations of styling (needs lots of CSS)
- Small community
</div>

---

<div class="container">
<div class="col">
<h3> Pros of Reveal.js</h3 >

(with reveal-md)

- Markdown (of course)
- Integration VS Code
- Easy to build
- Big community
</div>
<div class="col">
<h3> Cons of Reveal.js</h3 >

(with reveal-md)

- Limitations of styling (needs lots of CSS)
</div>

---

## Reveal.js

Note: Though there is no big winner, we decided to go on with Reveal.js. The VS Code integration is nicer, the community is bigger and one can influence more the backend.

---

## Let's see some examples

---

### Standard markdown stuff

---

#### Quotes

```md
> This is quoted text.
```

looks like this:

> This is quoted text.

---

#### Tables

```md
> This is quoted text.
```

looks like this:

> This is quoted text.

---

#### Lists with formated text

```md
1. **First** *item*
1. Second Item
1. Third `item`
1. Fourth item 
```

looks like this:

1. **First** *item*
1. Second Item
1. Third `item`
1. Fourth item

---

### Tables

<div class="container">
<div class="col">
<h3> In md </h3 >

```{md}
| item   | description         |
|--------|---------------------|
| list A | Contains A elements |
| list B | Contains B elements |
```

</div>
<div class="col">
<h3> Rendered </h3 >

| item   | description         |
|--------|---------------------|
| list A | Contains A elements |
| list B | Contains B elements |

</div>

---

### Or using HTML and CSS

---

#### Multiple columns

```html
<div class="container">
<div class="col">column 1</div>
<div class="col">column 2</div>
<div class="col">column 3</div>
</div>
```
looks like this:

<div class="container">
<div class="col">column 1</div>
<div class="col">column 2</div>
<div class="col">column 3</div>
</div>

---

#### Background image

```html
<!-- .slide: data-background="./assets/mercator-bw.jpg"-->
```

---

#### Override styles

```html
<h1 style="color:pink">Just use CSS</h1>
```
looks like:
<h1 style="color:yellow">Just use CSS</h1>

---

## Final state
- Theme-Prototypes for Pitch and for Teaching
- Running Repository www.github.com/opengisch/talks-reveal_md
- README.md for "Starters"

---

## To do's
- Finetune CSS (improve teaching theme)
- Update Presentations
- Improve CIs
- Change Repository to official talks

---

## Happy markdown 🎉
