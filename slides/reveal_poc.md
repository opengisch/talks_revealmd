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
  autoPlayMedia: true,
}
---

# Modernize the Talks repository
<h3 class=dark>And it's challenges</h3>

---

<section data-vertical-align-top> 
## Given state

- [github/opengisch/talks](github/opengisch/talks) repository with html
- [github/opengisch/public-talks](github/opengisch/public-talks) repository with some MARP prototyping
</section>

---

### Goal

- Decide for a way to go
- Set up a working repository
- Proof of Concepts with QField Presentation
- Accessability: easy entry point, documentation

---

## MARP

<div class="container">
<div class="col">
<h3> Pros </h3 >

- Markdown (of course)
- Integration VS Code
- Easy to build
</div>
<div class="col">
<h3> Cons </h3 >

- Limitations of styling (needs lots of CSS)
- Small community
</div>

---

## Reveal.js

<div class="container">
<div class="col">
<h3> Pros</h3>

(with reveal-md)

- Markdown (of course)
- Integration VS Code
- Easy to build
- Big community
</div>
<div class="col">
<h3> Cons</h3>

(with reveal-md)

- Limitations of styling (needs lots of CSS)
</div>

---

### Reveal.js

Note: Though there is no big winner, we decided to go on with Reveal.js. The VS Code integration is nicer, the community is bigger and one can influence more the backend.

---

### Let's see some examples

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
<h3> In md </h3>

```{md}
| item   | description         |
|--------|---------------------|
| list A | Contains A elements |
| list B | Contains B elements |
```

</div>
<div class="col">
<h3> Rendered </h3>

| item   | description         |
|--------|---------------------|
| list A | Contains A elements |
| list B | Contains B elements |

</div>

---

## Final state
- Running Repository
- README.md for "Starters"

---

## To dos
- Update Presentations
- Running Repository
- Change Repository to official talks

---

## Problems 
- Talker Notes
- {width="100%" height="30%"}

---

## Happy markdown 🎉
