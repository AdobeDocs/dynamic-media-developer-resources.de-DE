---
title: Lokalisierung von Elementen der Benutzeroberfläche
description: Bestimmte Inhalte, die der Karussell-Viewer anzeigt, unterliegen der Lokalisierung. Dieser Inhalt enthält Folien-Navigationsschaltflächen.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 05f5abe0-1124-4114-864d-440699bcdc39
source-git-commit: 67e12fae514341137e4218ea950f34da0d9997f3
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 0%

---

# Lokalisierung von Elementen der Benutzeroberfläche{#localization-of-user-interface-elements}

Bestimmte Inhalte, die der Karussell-Viewer anzeigt, unterliegen der Lokalisierung. Dieser Inhalt enthält Folien-Navigationsschaltflächen.

Jeder Textinhalt, der im Viewer lokalisiert werden kann, wird durch die spezielle Viewer-SDK-Kennung namens SYMBOL dargestellt. Jedes SYMBOL verfügt über einen standardmäßigen Textwert für ein englisches Gebietsschema ( `"en"`), das mit dem standardmäßigen Viewer bereitgestellt wird, und kann auch benutzerdefinierte Werte für beliebig viele Gebietsschemata festlegen.

Beim Starten des Viewers wird das aktuelle Gebietsschema überprüft, um festzustellen, ob für jedes unterstützte SYMBOL für dieses Gebietsschema ein benutzerdefinierter Wert vorhanden ist. Ist dies der Fall, wird der benutzerdefinierte Wert verwendet, andernfalls wird der Standardtext verwendet.

Benutzerdefinierte Lokalisierungsdaten können als JSON-Objekt für die Lokalisierung an den Viewer übergeben werden. Dieses Objekt enthält die Liste der unterstützten Gebietsschemata, SYMBOL-Textwerte für jedes Gebietsschema und das Standardgebietsschema.

Ein Beispiel für ein solches Lokalisierungsobjekt ist Folgendes:

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

Im obigen Beispiel definiert das Localization-Objekt zwei Gebietsschemata (`"en"` und `"fr"`) und stellt die Lokalisierung für zwei Elemente der Benutzeroberfläche in jedem Gebietsschema bereit.

Der Web-Seiten-Code sollte das Lokalisierungsobjekt an den Viewer-Konstruktor als Wert `localizedTexts` Felds des Konfigurationsobjekts übergeben. Eine alternative Option besteht darin, das Lokalisierungsobjekt durch Aufruf `setLocalizedTexts(localizationInfo)` -Methode zu übergeben.

Die folgenden SYMBOLE werden unterstützt:

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>SYMBOL </p> </th> 
   <th colname="col2" class="entry"> <p>QuickInfo für… </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>Ausgewählter Status der Wiedergabe-Pause-Schaltfläche </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>Ausgewählter Status der Pause-Wiedergabeschaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CAROUSELVIEWER_TOOLTIP_GOTO </span> </p> </td> 
   <td colname="col2"> <p> QuickInfo und ARIA-Beschriftung für die Schaltflächen für die vorherige und nächste Folie. </p> <p>Akzeptiert zwei Ersatz-Token: <span class="codeph"> $CURRENT_FRAME$ </span> für den aktuellen Folienindex und <span class="codeph"> $TOTAL_FRAMES$ </span> für die Gesamtzahl der Folien. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">.LABEL-</span> </p> </td> 
   <td colname="col2"> <p> ARIA-Beschriftung für Viewer-Element der obersten Ebene. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CarouselView.ROLE_DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p> ARIA-Rollenbeschreibung für die Hauptansichtskomponente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CarouselView.USAGE_HINT </span> </p> </td> 
   <td colname="col2"> <p> ARIA-Nutzungshinweise für Tastaturbenutzer. </p> </td> 
  </tr> 
 </tbody> 
</table>
