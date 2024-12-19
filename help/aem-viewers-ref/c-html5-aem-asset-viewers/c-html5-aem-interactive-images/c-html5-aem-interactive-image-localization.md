---
title: Lokalisierung von Elementen der Benutzeroberfläche
description: Bestimmte Inhalte, die der interaktive Bild-Viewer anzeigt, unterliegen der Lokalisierung. Dieser Inhalt enthält QuickInfos zu Benutzeroberflächenelementen und eine Informationsmeldung, die beim Laden von der Flyout-Zoomansicht angezeigt wird.
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 19749c74-5c31-4dcf-ab07-0e7f10176a86
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# Lokalisierung von Elementen der Benutzeroberfläche{#localization-of-user-interface-elements}

Bestimmte Inhalte, die der interaktive Bild-Viewer anzeigt, unterliegen der Lokalisierung. Dieser Inhalt enthält QuickInfos zu Benutzeroberflächenelementen und eine Informationsmeldung, die beim Laden von der Flyout-Zoomansicht angezeigt wird.

Jeder Textinhalt, der im Viewer lokalisiert werden kann, wird durch die spezielle Viewer-SDK-Kennung namens SYMBOL dargestellt. Jedes SYMBOL verfügt über einen standardmäßigen Textwert für ein englisches Gebietsschema ( `"en"`), das mit dem standardmäßigen Viewer bereitgestellt wird, und kann benutzerdefinierte Werte für so viele Gebietsschemata wie erforderlich festlegen.

Beim Starten des Viewers wird das aktuelle Gebietsschema überprüft, um festzustellen, ob für jedes unterstützte SYMBOL für dieses Gebietsschema ein benutzerdefinierter Wert vorhanden ist. Ist dies der Fall, wird der benutzerdefinierte Wert verwendet, andernfalls wird der Standardtext verwendet.

Benutzerdefinierte Lokalisierungsdaten können als JSON-Objekt für die Lokalisierung an den Viewer übergeben werden. Dieses Objekt enthält die Liste der unterstützten Gebietsschemata, SYMBOL-Textwerte für jedes Gebietsschema und das Standardgebietsschema.

Ein Beispiel für ein solches Lokalisierungsobjekt ist Folgendes:

```
{ 
"en":{ 
"Container.LABEL":"Interactive Image Viewer" 
 }, 
 "fr":{ 
"Container.LABEL":"Visionneuse d'images interactive" 
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
 </tbody> 
</table>
