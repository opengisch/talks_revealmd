---
title: Model Baker Pitch 02
description: QGIS Model Baker Journey in Pictures
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

![Logo](./assets/modelbaker_logo.png)

---

### Abstract

**Model Baker** is a **QGIS plugin** that can be used to create projects from an **INTERLIS** model. **Model Baker** uses **ili2db** to import a model into a **physical database** and additional meta information to automatically configure **layer tree, forms, relations and more**. It is **open source** and freely available.

---

### INTERLIS Geodatamodel

<!-- We have **INTERLIS** geodata models locally or on an online repository.-->

```
MODEL Wildruhezonen_LV95_V2_1 (de)
VERSION "2020-04-21"  =
  IMPORTS GeometryCHLV95_V1,LocalisationCH_V1,CHAdminCodes_V1,Wildruhezonen_Codelisten_V2_1;

  TOPIC Wildruhezonen =
    DEPENDS ON Wildruhezonen_Codelisten_V2_1.Codelisten;

    DOMAIN
      Polygon = SURFACE WITH (STRAIGHTS) VERTEX GeometryCHLV95_V1.Coord2 WITHOUT OVERLAPS > 0.001

    CLASS Wildruhezone =
      ObjNummer : MANDATORY 0 .. 9999;
      Kanton : MANDATORY CHAdminCodes_V1.CHCantonCode;
      Name : MANDATORY TEXT*80;
      Schutzstatus : MANDATORY Wildruhezonen_Codelisten_V2_1.Codelisten.Schutzstatus_CatRef;
      Grundlage : MANDATORY TEXT*250;
      Beschlussjahr : MANDATORY INTERLIS.GregorianYear;
      Mutationsdatum : INTERLIS.XMLDate;
      Mutationsgrund : LocalisationCH_V1.MultilingualMText;
    END Wildruhezone;

    CLASS Routennetz =
      Geo_Obj : MANDATORY Linie;
      Wegtyp : MANDATORY Wildruhezonen_Codelisten_V2_1.Codelisten.Wegtyp_CatRef;
      Einschraenkung : TEXT*254;
    MANDATORY CONSTRAINT NOT (Wegtyp->Reference->Code == "W1") OR NOT (DEFINED (Einschraenkung));
    END Routennetz;

    CLASS Wildruhezone_Teilobjekt =
      TeilObjNummer : MANDATORY TEXT*30;
      Bestimmungen : MANDATORY Wildruhezonen_Codelisten_V2_1.Codelisten.Bestimmungen_CatRef;
      Bestimmungen_Kt : LocalisationCH_V1.MultilingualMText;
      Zusatzinformation : TEXT*500;
      RefKanton : INTERLIS.URI;
      Schutzzeit : MANDATORY TEXT*250;
      Geo_Obj : MANDATORY Polygon;
    MANDATORY CONSTRAINT NOT (Bestimmungen->Reference->Code == "R900" OR Bestimmungen->Reference->Code == "E900") OR DEFINED (Bestimmungen_Kt);
    END Wildruhezone_Teilobjekt;

    ASSOCIATION RoutennetzWildruhezone =
      WRZ_Routennetz -- {0..*} Routennetz;
      WRZ -<#> {1} Wildruhezone;
    END RoutennetzWildruhezone;

    ASSOCIATION Wildruhezone_TeilobjektWildruhezone =
      WRZ_Teilobjekt -- {1..*} Wildruhmodel
END Wildruhezonen_LV95_V2_1.
```

---

### Model Baker gets the info

![wizard](./assets/modelbaker_wizard.png)

<!-- **Model Baker** finds the relevant information and creates the database using **ili2db**.-->

---

### QGIS Project is generated

<!-- Database and INTERLIS metadata are analyzed to automatically configure a QGIS project with layertree, forms, relations and much more.-->

![projekt](./assets/modelbaker_projekt.png)


