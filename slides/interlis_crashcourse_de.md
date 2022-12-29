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


<h1 style="-webkit-text-stroke: 2px var(--opengisch-dark) !important; color: lightgray !important; font-size:4.5em !important; text-align: center !important;">INTERLIS CRASHKURS</h1>

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

# Fragen (15 Minuten) 🙋

-->

---

### Ziele des Crashkurses

- Wissen was INTERLIS ist und wie es angewendet wird.
- Ein Modell lesen zu können und sich darin zurechtfinden. 

--v--

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

---

Kurze Einführung...

## Was ist INTERLIS überhaupt?

--v--

- **INTER** **L**and **I**nfomations **S**ysteme
- Eine konzeptionelle Beschreibungsprache, mit spezieller Berücksichtigung von **Geodaten**
- Lesbar von Menschen und Maschinen
- Objektorientiert und Erweiterbar
- Systemneutral (Plattformunabhängig)
- Strikte Trennung zwischen Modell und Transferdaten

<!-- 
**INTER** **L**and **I**nfomations **S**ysteme -> dient der Zusammenarbeit von (Geographischen) Informations Systemen. Alle beteiligten Systeme sollen die Konzepte kennen, die für die Zusammenarbeit wichtig sind. 

Es umfasst also eine **konzeptionelle Beschreibungssprache**, welche die Realwelt beschreibt. Ist also lesbar von Menschen wie von Maschinen und ideal als Grundlage zur Diskusion zwischen IT-Nerds und thematischen Fachleuten.

Objektorientiert seit Version 2 (gängige version ist 2.3 obwohl 2.4 die aktuelle ist). Die Tatsache, dass es Objektorientiert ist führt dazu, dass es ideal ist für den Datenaustausch zwischen Bundesstellen / Kantonsstellen etc.
-->

--v--

### Modelldatei und Transferdatei

Das Modell (die Struktur) ist geschrieben in INTERLIS und gespeichert als `.ili` Datei.

Die Daten sind geschrieben in XML (gemäss Modell) und gespeichert als `.xtf` Datei (früher `.itf`).

--v--

### Wieso du INTERLIS mögen könntest

Du hast dein Datenbankschema in der Hosentasche.

Es ist "einfach" lesbar und sehr präzise.

Dank den Tools ist es einfach in deiner Datenbank und in QGIS zu implementieren und die Daten zu validieren.

<!-- 
Es gibt bestimmt genügend Gründe, INTERLIS nicht zu mögen.

Verglichen zu SQL Scripts ist es systemunabhängig und einfach zu erweitern. -->

---

Aber beginnen wir von vorn...
## Schreiben des erstes Modells

--v--

### Ausgangslage

Clemens ist nicht glücklich. Bei jedem Datenaustausch muss er sich ransetzen und die Daten **überprüfen** und **bereinigen**.

- Werte sind nicht konsistent
- Einträge sind teilweise doppelt

Er schickt mir ein [Datensatz als CSV](./assets/interlis_crashcourse/gebaeude_clean.csv).

--v--

Lasst uns dafür ein supereasy Modell schreiben...
### Basic INTERLIS Syntax

--v--

![structure](./assets/interlis_model_structure.png){ style="display: block; margin: 0 auto" }

--v--

### MODEL

<!-- echte syntax kodierung zeigen oder eben nicht? -->
```NONE
INTERLIS 2.3;

MODEL Wildruhezonen_LV95_V2_1 (de)

AT "https://models.geo.admin.ch/BAFU/"

VERSION "2020-04-21"  =



  [...]



END Wildruhezonen_LV95_V2_1.
```

--v--

### TOPIC
<!-- echte syntax kodierung zeigen oder eben nicht? -->

```NONE
INTERLIS 2.3;

MODEL Wildruhezonen_LV95_V2_1 (de)

AT "https://models.geo.admin.ch/BAFU/"

VERSION "2020-04-21"  =

  TOPIC Wildruhezonen =

    [...]

  END Wildruhezonen;

END Wildruhezonen_LV95_V2_1.
```

--v--

### CLASS
<!-- echte syntax kodierung zeigen oder eben nicht? -->

<code>
INTERLIS 2.3;

MODEL Wildruhezonen_LV95_V2_1 (de)

AT "https://models.geo.admin.ch/BAFU/"

VERSION "2020-04-21"  =

  **TOPIC Wildruhezonen =**

    [...]

  **END Wildruhezonen;**

END Wildruhezonen_LV95_V2_1.
</code>

---