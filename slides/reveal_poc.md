---
title: Reveal PoC
description: PoC for reveal.js
theme: theme/teaching-theme.css
customTheme: _assets/theme/teaching-theme
verticalSeparator: --v--
revealOptions: {
  transition: 'none',
  slideNumber: false,
  overview: true,
  autoPlayMedia: true
}
---

# Modernize the Talks repository
<h3 class=dark>And it's challenges</h3>

---

## Given state
----

- [github/opengisch/talks](github/opengisch/talks) repository with html
- [github/opengisch/public-talks](github/opengisch/public-talks) repository with some MARP prototyping

---

##  Goal
----

- Decide for a way to go
- Set up a working repository
- Proof of Concepts with QField Presentation
- Accessability: easy entry point, documentation

---

## MARP
----
<div class="container">
<div class="col">

#### Pros 

- Markdown (of course)
- Integration VS Code
- Easy to build
</div>
<div class="col">

#### Cons

- Limitations of styling (needs lots of CSS)
- Small community
</div>

---

## Reveal.js 
##### (with reveal-md)
----

<div class="container">
<div class="col">

####  Pros

- Markdown (of course)
- Integration VS Code
- Easy to build
- Big community
</div>
<div class="col">

#### Cons

- Limitations of styling (needs lots of CSS)
</div>

---

## Decition for Reveal.js
----

Note: Though there is no big winner, we decided to go on with Reveal.js. The VS Code integration is nicer, the community is bigger and one can influence more the backend.

---

## Standard markdown stuff

---

### Quotes
----

**Markdown:**

```md
> This is quoted text.
```

**Looks like**

> This is quoted text.

---

### Lists with formated text
----

**Markdown:**
```md
1. **First** *item*
1. Second Item
1. Third `item`
1. Fourth item
```

**Looks like**

1. **First** *item*
1. Second Item
1. Third `item`
1. Fourth item

---

### Tables
----

<div class="container">
<div class="col">

**Markdown**

```{md}
| item   | description         |
|--------|---------------------|
| list A | Contains A elements |
| list B | Contains B elements |
```

</div>
<div class="col">

**Looks like**

| item   | description         |
|--------|---------------------|
| list A | Contains A elements |
| list B | Contains B elements |

</div>

---

### Hacky stuff

---

### Override style
----

**HTML:**
```html
<h1 style="color:purple !important;">QField</h1>
```

**Looks like**

<h1 style="color:purple !important;">QField</h1>

---

### Background Image
----

**HTML:**
```html
<!-- .slide: data-background="./assets/customer.JPG"-->
```

**Looks like this**

---

### Multiple Columns
----

**HTML:**

```html
<div class="container">
<div class="col">column 1</div>
<div class="col">column 2</div>
<div class="col">column 3</div>
</div>
```

**Looks like this**

<div class="container">
<div class="col">column 1</div>
<div class="col">column 2</div>
<div class="col">column 3</div>
</div>

---

## Final state
- Running repository
- Theme templates for teaching and pitches with PoC presentations
- README.md for "starters"

---

## To dos
- Checkout plugins
- Finetune themes
- Finalize README.md
- Update presentations
- Change repository to official talks

---

## Plugins 
- For speaker notes
- Things like `{width="100%" height="30%"}`

---

## Happy markdown 🎉
