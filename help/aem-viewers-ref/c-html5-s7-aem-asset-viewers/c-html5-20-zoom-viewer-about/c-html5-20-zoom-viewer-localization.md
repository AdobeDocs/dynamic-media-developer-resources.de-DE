---
title: Lokalisierung von Elementen der Benutzeroberfläche
description: Bestimmte Inhalte, die der Video-Viewer anzeigt, unterliegen der Lokalisierung, einschließlich Zoom-Schaltflächen und einer Vollbildschaltfläche.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: c386a09c-21ce-4105-b416-e6ae50219af0
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 0%

---

# Lokalisierung von Elementen der Benutzeroberfläche{#localization-of-user-interface-elements}

Bestimmte Inhalte, die der Video-Viewer anzeigt, unterliegen der Lokalisierung, einschließlich Zoom-Schaltflächen und einer Vollbildschaltfläche.

Jeder Textinhalt im Viewer, der lokalisiert werden kann, wird durch eine spezielle Viewer-SDK-Kennung namens SYMBOL dargestellt. Jedes SYMBOL verfügt über einen standardmäßigen Textwert für das englische Gebietsschema ( `"en"`), der mit dem standardmäßigen Viewer bereitgestellt wird. Darüber hinaus können benutzerdefinierte Werte für beliebig viele Gebietsschemata festgelegt werden.

Beim Starten des Viewers wird das aktuelle Gebietsschema überprüft, um festzustellen, ob für jedes unterstützte SYMBOL für das Gebietsschema ein benutzerdefinierter Wert vorhanden ist. Ist dies der Fall, wird der benutzerdefinierte Wert verwendet, andernfalls wird der Standardtext verwendet.

Benutzerdefinierte Lokalisierungsdaten können als JSON-Objekt für die Lokalisierung an den Viewer übergeben werden. Dieses Objekt enthält die Liste der unterstützten Gebietsschemata, SYMBOL-Textwerte für jedes Gebietsschema und das Standardgebietsschema.

Ein Beispiel für ein solches Lokalisierungsobjekt ist Folgendes:

```
{ 
"en":{ 
"CloseButton.TOOLTIP":"Close", 
"ZoomInButton.TOOLTIP":"Zoom In" 
 }, 
 "fr":{ 
"CloseButton.TOOLTIP":"Fermer", 
"ZoomInButton.TOOLTIP":"Agrandir" 
}, 
defaultLocale:"en" 
}
```

Im obigen Beispiel definiert das Localization-Objekt zwei Gebietsschemata (`"en"` und `"fr"`) und stellt die Lokalisierung für zwei Elemente der Benutzeroberfläche in jedem Gebietsschema bereit.

Der Web-Seiten-Code sollte dieses Lokalisierungsobjekt an den Viewer-Konstruktor als Wert `localizedTexts` Felds des Konfigurationsobjekts übergeben. Eine alternative Option besteht darin, das Localization-Objekt durch Aufruf der `setLocalizedTexts(localizationInfo)`-Methode zu übergeben.

Die folgenden SYMBOLE werden unterstützt:

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>SYMBOL </p> </th> 
   <th colname="col2" class="entry"> <p>QuickInfo für die… </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">.LABEL-</span> </p> </td> 
   <td colname="col2"> <p>ARIA-Beschriftung für Viewer-Element der obersten Ebene. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.ROLE_DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>ARIA-Rollenbeschreibung für die Hauptansichtskomponente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.USAGE_HINT </span> </p> </td> 
   <td colname="col2"> <p>ARIA-Nutzungshinweise für Tastaturbenutzer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> closeButton.TOOLTIP-</span> </p> </td> 
   <td colname="col2"> <p>Schließen-Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomInButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche „Vergrößern“. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomOutButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche „Verkleinern“. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomResetButton.TOOLTIP-</span> </p> </td> 
   <td colname="col2"> <p>Zurücksetzen-Schaltfläche für Zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> fullScreenButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>Vollbildschaltfläche im normalen Zustand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> fullScreenButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>Vollbildschaltfläche im Vollbildmodus. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollLeftButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Nach links scrollen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollRightButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Nach rechts scrollen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollUpButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Scroll up button. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollDownButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Scroll down button. </p> </td> 
  </tr> 
 </tbody> 
</table>
