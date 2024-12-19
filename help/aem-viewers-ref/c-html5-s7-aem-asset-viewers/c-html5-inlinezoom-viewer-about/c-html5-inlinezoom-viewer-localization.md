---
title: Lokalisierung von Elementen der Benutzeroberfläche
description: Bestimmte Inhalte, die der Flyout-Viewer anzeigt, unterliegen der Lokalisierung. Dieser Inhalt enthält QuickInfos zu Benutzeroberflächenelementen und Informationsmeldungen, die beim Laden in der Flyout-Zoomansicht angezeigt werden.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 49795aa1-07c7-4f2e-bfd9-51d6581898ed
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 0%

---

# Lokalisierung von Elementen der Benutzeroberfläche{#localization-of-user-interface-elements}

Bestimmte Inhalte, die der Flyout-Viewer anzeigt, unterliegen der Lokalisierung. Dieser Inhalt enthält QuickInfos zu Benutzeroberflächenelementen und Informationsmeldungen, die beim Laden in der Flyout-Zoomansicht angezeigt werden.

Jeder Textinhalt, der im Viewer lokalisiert werden kann, wird durch die spezielle Viewer-SDK-Kennung namens SYMBOL dargestellt. Jedes SYMBOL verfügt über einen standardmäßigen Textwert für ein englisches Gebietsschema ( `"en"`), das mit dem standardmäßigen Viewer bereitgestellt wird, und kann auch benutzerdefinierte Werte für beliebig viele Gebietsschemata festlegen.

Beim Starten des Viewers wird das aktuelle Gebietsschema überprüft, um festzustellen, ob für jedes unterstützte SYMBOL für dieses Gebietsschema ein benutzerdefinierter Wert vorhanden ist. Ist dies der Fall, wird der benutzerdefinierte Wert verwendet, andernfalls wird der Standardtext verwendet.

Benutzerdefinierte Lokalisierungsdaten können als JSON-Objekt für die Lokalisierung an den Viewer übergeben werden. Dieses Objekt enthält die Liste der unterstützten Gebietsschemata, SYMBOL-Textwerte für jedes Gebietsschema und das Standardgebietsschema.

Ein Beispiel für ein solches Lokalisierungsobjekt ist Folgendes:

```
{ 
"en":{ 
"FlyoutZoomView.TIP_BUBBLE_OVER":"Mouse over to zoom", 
"FlyoutZoomView.TIP_BUBBLE_TAP":"Tap and hold to zoom" 
 }, 
 "fr":{ 
"FlyoutZoomView.TIP_BUBBLE_OVER":"Passez la souris sur pour zoomer", 
"FlyoutZoomView.TIP_BUBBLE_TAP":"Appuyez et maintenez pour agrandir" 
}, 
defaultLocale:"en" 
}
```

Im obigen Beispiel definiert das Localization-Objekt zwei Gebietsschemata (`"en"` und `"fr"`) und stellt die Lokalisierung für zwei Elemente der Benutzeroberfläche in jedem Gebietsschema bereit.

Der Web-Seiten-Code sollte dieses Lokalisierungsobjekt an den Viewer-Konstruktor als Wert des `localizedTexts` des Konfigurationsobjekts übergeben. Eine alternative Option besteht darin, das Localization-Objekt durch Aufruf der `setLocalizedTexts(localizationInfo)`-Methode zu übergeben.

Die folgenden SYMBOLE werden unterstützt:

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>SYMBOL </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">.LABEL-</span> </p> </td> 
   <td colname="col2"> <p>ARIA-Beschriftung für Viewer-Element der obersten Ebene. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.ROLE_DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>ARIA-Rollenbeschreibung für die Hauptansichtskomponente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.USAGE_HINT-</span> </p> </td> 
   <td colname="col2"> <p>ARIA-Nutzungshinweise für Tastaturbenutzer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.TIPP_BUBBLE_OVER </span> </p> </td> 
   <td colname="col2"> <p>Informationsmeldung für Desktop-Systeme. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.TIPP_BUBBLE_TAP </span> </p> </td> 
   <td colname="col2"> <p>Informationsmeldung für Touch-Geräte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollLeftButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>QuickInfo für den Bildlauf mit der linken Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollRightButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>QuickInfo für den Bildlauf mit der rechten Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollUpButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>QuickInfo für die Schaltfläche Nach oben scrollen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollDownButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>QuickInfo für Scroll-Down-Schaltfläche. </p> </td> 
  </tr> 
 </tbody> 
</table>
