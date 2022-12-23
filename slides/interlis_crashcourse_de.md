---
title: INTERLIS Crashkurs
description: INTERLIS Crashkurs 120 Minuten
theme: theme/softteaching-theme.css
customTheme: _assets/theme/softteaching-theme
verticalSeparator: --v--
transition: none
revealOptions: {
  transition: 'none',
  slideNumber: false,
  overview: true,
  autoPlayMedia: true,
}
---

<!-- .slide: data-background="./assets/interlis_crashcourse.png" -->


<h1 style="color:#93bfe5 !important;">INTERLIS CRASHKURS</h1>

---

<!--
# Einführung (15 Minuten)
- Begrüssung
- Programm
- Was ist INTERLIS

# Erstes Modell (25 Minuten)
- Fallbeispiel EGID
- Basic INTERLIS Syntax (Model, Topic, Class)
- Erstes supereasy Model

# Datentypen und Constraints (20 Minuten)
- Erstelle die Datentypen
- Erstelle Constraints

# Pause (15 Minuten)

# Beziehungen und Referenzen (10 Minuten)
- ASSOCIATIONS und STRUCTURES
- BAG OF und LIST OF

# Vererbungen (20 Minuten)

# Kataloge (15 Minuten)

# Interlis Repositories und Tools (15 Minuten)

# Fragen (15 Minuten)

-->

### Programm

- Was ist INTERLIS überhaupt?
- Schreiben des erstes Modells
- Datentypen und Bedingungen
- ☕

--v--

### Programm

- Beziehungen und Referenzen
- Vererbungen
- Aufzählungen und Kataloge
- Repositorien (Schweizer Geodatenmodelle)
- 🙋

---

## Was ist INTERLIS überhaupt?

---

- INTER Land Information Systems
- A data description language with special consideration of **geodata**
- Object oriented and extendable
- System neutral (platform independent)
- Readable by humans and machines
- Model driven approach

<!-- [INTERLIS](https://www.interlis.ch/) (INTER Land Information Systems) is a data description language and a transfer format with special consideration of geodata. INTERLIS offers the possibility to describe spatial data precisely, to integrate them in conformity with the model and to exchange them easily among different users. INTERLIS has been bindingly anchored in Swiss geoinformation legislation since 2008. Since INTERLIS has been object-oriented since version 2, it can be extended very easily. This means that, for example, the federal government defines a model that the cantonal authorities can derive and extend according to their needs. 

- Supports Geometries
- Since version 2 object oriented - perfect for data exchange between authorities. This is important since it's anchored in Swiss geoinformation legislation since 2008 to use INTERLIS.
- Perfect for the discussion between ITs and thematic specialists
- Strict division between the transfer part and the modeling part
-->

---

## Model file and transfer data file

The model is defined in INTERLIS language and stored in an `.ili` file.

The data is in xml (considering the model) and stored as an `.xtf` file (former `.itf`).

---

## Why you could like INTERLIS

You have your database schema in your poket. 

It's easy readable and precice.

Thanks to the nice tools, it's easy to implement in your database and in QGIS.

<!--  Compared to e.g. SQL Scripts you can simply extend it. -->

---