---
description: Bestimmte Inhalte, die im Karussell-Viewer angezeigt werden, unterliegen der lokale Anpassung. Dazu gehören Navigationsschaltflächen für Dias.
seo-description: Bestimmte Inhalte, die im Karussell-Viewer angezeigt werden, unterliegen der lokale Anpassung. Dazu gehören Navigationsschaltflächen für Dias.
seo-title: Lokale Anpassung der Elemente der Benutzeroberfläche
solution: Experience Manager
title: Lokale Anpassung der Elemente der Benutzeroberfläche
topic: Dynamic media
uuid: 82e4dc72-cc12-4ab5-8370-6270f9a3d45f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Lokale Anpassung der Elemente der Benutzeroberfläche{#localization-of-user-interface-elements}

Bestimmte Inhalte, die im Karussell-Viewer angezeigt werden, unterliegen der lokale Anpassung. Dazu gehören Navigationsschaltflächen für Dias.

Jeder Textinhalt im Viewer, der lokalisiert werden kann, wird durch den speziellen Viewer SDK-Bezeichner SYMBOL dargestellt. Jedes SYMBOL verfügt über einen Standardtextwert für ein englisches Gebietsschema ( `"en"`), das mit dem standardmäßigen Viewer bereitgestellt wird, und kann auch benutzerdefinierte Werte für so viele Gebietsschemas wie erforderlich enthalten.

Beim Beginn des Viewers wird das aktuelle Gebietsschema überprüft, um festzustellen, ob für jedes unterstützte SYMBOL für dieses Gebietsschema ein benutzerdefinierter Wert vorhanden ist. Ist dies der Fall, wird der benutzerdefinierte Wert verwendet. Andernfalls wird auf den Standardtext zurückgesetzt.

Benutzerdefinierte Daten zur lokale Anpassung können als JSON-Objekt der lokale Anpassung an den Viewer übergeben werden. Dieses Objekt enthält die Liste der unterstützten Gebietsschemata, SYMBOL-Textwerte für jedes Gebietsschema und das Standardgebietsschema.

Ein Beispiel für ein solches lokale Anpassung-Objekt ist Folgendes:

```
{ 
"en":{ 
"PanLeftButton.TOOLTIP":"Left", 
"PanRightButton.TOOLTIP":"Right" 
 }, 
 "fr":{ 
"PanLeftButton.TOOLTIP":"Gauchiste", 
"PanRightButton .TOOLTIP":"Droit" 
}, 
defaultLocale:"en" 
}
```

Im obigen Beispiel definiert das lokale Anpassung-Objekt zwei Gebietsschemas ( `"en"` und `"fr"`) und stellt lokale Anpassung für zwei Benutzeroberflächenelemente in jedem Gebietsschema bereit.

Der Webseitencode sollte das lokale Anpassung-Objekt als Feldwert des Konfigurationsobjekts an den Viewer-Konstruktor `localizedTexts` übergeben. Eine andere Option besteht darin, das lokale Anpassung-Objekt durch Aufrufen der `setLocalizedTexts(localizationInfo)` Methode zu übergeben.

Die folgenden SYMBOLs werden unterstützt:

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>SYMBOL </p> </th> 
   <th colname="col2" class="entry"> <p>QuickInfo für... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>Status der Schaltfläche zum Abspielen der Pause. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>Nicht ausgewählte Schaltfläche zum Abspielen der Pause. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CAROUSELVIEWER_TOOLTIP_GOTO </span> </p> </td> 
   <td colname="col2"> <p> QuickInfo und ARIA-Beschriftung für die Schaltflächen "Zurück"und "Weiter". </p> <p>Akzeptiert zwei Ersetzungstoken: <span class="codeph"> $CURRENT_FRAME$ </span> für den aktuellen Folienindex und <span class="codeph"> $TOTAL_FRAMES$ </span> für die Gesamtzahl der Folien. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL </span> </p> </td> 
   <td colname="col2"> <p> ARIA-Beschriftung für Viewer-Element der obersten Ebene. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CarouselView.ROLE_DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p> ARIA-Rollenbeschreibung für die Hauptkomponente Ansicht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CarouselView.USAGE_HINT </span> </p> </td> 
   <td colname="col2"> <p> ARIA-Verwendungshinweise für Tastaturbenutzer. </p> </td> 
  </tr> 
 </tbody> 
</table>

