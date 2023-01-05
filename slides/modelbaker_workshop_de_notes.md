### Postgres DB erstellen mit Extensions (Mitmachen)

- Datenbank erstellen
- Extensions installieren

> **Ziel:** 
Dass man mit weiter, weiter, weiter zu einem "Resultat" kommt.

- Zeige Slides von github.ch/opengisch/talks/modelbaker:

- Drag-and-drop - don't stop, don't turn back
- Hintergrundkarte einfügen - zeigen was es gibt
- Formular öffnen Punkte / Formular öffnen Polygons -> Problem mit Geometry Mapping

### Wizzard (dave) 90'

#### Drag-and-drop XTF, ILI, XML (Mitmachen)

> **Ziel:** 
Dass man mit weiter, weiter, weiter zu einem "Resultat" kommt.

- Drag-and-drop - don't stop, don't turn back
- Hintergrundkarte einfügen - zeigen was es gibt
- Formular öffnen Punkte / Formular öffnen Polygons -> Problem mit Geometry Mapping

 #### Nochmal von vorne nur mit XTF (Mitmachen)

 > **Ziel:**
Wissen woher die Models kommen.

- Drag-and-drop XTF von SH
- File / Repo Browser erklären
- DB Page durchgehen (Super-User erwähnen)
- Erklären, dass Model nun aus XTF geparst und auf Repo gesucht wurde.
- Check ili2db Command
- Erwähnen dass der Katalog fehlt
- Import funktioniert auch so - auch hier Polygon Structure übergang zum nächsten Schritt.

#### Advanced Options (TOML) (Mitmachen)
> **Ziel:**
Wissen was die Advanced Options sollen und was TOMLs sind und können. 

- Drag-and-drop XTF von SH und auch des Katalogs
- Select Advanced Options sind Optionen, die dem ili2db übegeben werden:
  - Smart Inheritance ist wie die Vererbungen abgebildet werden -> See later on.
  - Create Basked Column definiert das Basket Handling -> See later on.
  - Stroke Arcs definiert ob Curves zu Polygonen werden sollen.
  - SQL Scripts sind User definierte SQL Scripts die vor oder nach der DB-Erstellung ausgeführt werden.
  - Extra Model Information Files sind das was wir brauchen -> Romedi
- Weiter gehts und erwähnen, dass der Katalog zuerst geladen werden muss.

#### Smart Inheritance Mapping Exkurs (Theorie)
> **Ziel:**
Wissen inwiefern unterschiede in den Strategien bestehen und was ungefähr Smart1 und Smart2 tun.

- Um zu zeigen was Smart Inheritance ist, werden wir ein anderes Model verwenden: Building_Smart_Parking -> Check Model und Vererbungen
- Zeige Folien von hier: https://signedav.github.io/interlis_relations_in_qgis/#23 bis Seite 38
- Drag-and-drop building_smart_parking.ili
- Machs auf PG
- Erstellen ohne Baskets und mit **Smart1**
- Rename "Tables" zu "Smart1Tables"
- Drag-and-drop building_smart_parking.ili
- Machs auf PG
- Erstellen ohne Baskets und mit **Smart2**
- Vergleiche und evtl. zeig nochmals Folien

#### Katalog automatisch mit ilidata.xml und Demo UsabILIty Hub

> **Ziel:** 
Wissen dass es UsabILIty Hub und ildata.xml Daten-Verlinkung gibt und ModelBaker diese unterstützt.

- Die Metaconfig Toppings haben wir bisher noch übersprungen.
- Erklären der Möglichkeit, dass man Topping Files (ili2db Parameter, Katalog-Daten und QGIS Projektsettings) auch auf den Repos ablegen kann. Wie's genau funktioniert sehen wir später.
#### Datenimport / Baskets (Mitmachen)

> **Ziel:**
Wissen was Baskets / Datasets sind. Wissen wie man Datset Selector und Dataset Manager benützt.

- Zeige Topics **Codelisten** und **Belastete_Standorte**. Da man die Daten der Codelisten nicht bearbeiten können soll und die von Belastete_Standorte schon, kann man die Topics einzeln behandeln. Diese sind strukturell voneinander getrennt.
    Nehmen wir aber an wir möchten die Datensätze von Schaffhausen und Thurgau in der gleichen Datenbank bearbeiten, sie aber dann einzeln validieren / updaten / exportieren. Dafür gibts Datasets und Baskets.
    Keine Grafik. Dafür evtl. auf **FLIPCHART** zeichnen.

    > Datasets sind Datensätze eines bestimmten räumlichen oder thematischen Bereichs, die aber die Modellstruktur nicht tangieren. Eine kleinere Instanz sind die Baskets oder Behälter. Währenddem die Datasets meist das ganze Modell umfassen, sind die Behälter meist Teil eines Topics. Oftmals sind sie sogar die Teilmenge von Topic und Dataset.

- Drag-and-drop ch.tg.kataster....xtf und KbS_V1_5_SH.xtf
- Erstelle Dataset "Schaffhausen" und "Thurgau"
- Darstellung anhand von t_basket
- Zeige Technische Tabellen
- Zeige Dataset Selector

#### Nach Romedis Erklärung UsabILIty Hub

- Drag-and-drop XTF von SH
- Wähle Metaconfig, zeige wie TOML gesetzt wird, zeige wie Kataloge geladen werden automatisch.
- Zeige wie Katalog zur Auswahl steht im Datenimport

