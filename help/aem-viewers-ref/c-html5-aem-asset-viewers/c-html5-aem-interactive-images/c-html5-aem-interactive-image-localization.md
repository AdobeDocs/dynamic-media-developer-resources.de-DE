---
title: Lokalisierung der Elemente der Benutzeroberfläche
description: Bestimmte Inhalte, die der interaktive Bild-Viewer anzeigt, können lokalisiert werden. Dieser Inhalt enthält QuickInfos zu Elementen der Benutzeroberfläche und eine Informationsmeldung, die vom Flyout-Zoom-Ansicht beim Laden angezeigt wird.
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 19749c74-5c31-4dcf-ab07-0e7f10176a86
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 0%

---

# Lokalisierung der Elemente der Benutzeroberfläche{#localization-of-user-interface-elements}

Bestimmte Inhalte, die der interaktive Bild-Viewer anzeigt, können lokalisiert werden. Dieser Inhalt enthält QuickInfos zu Elementen der Benutzeroberfläche und eine Informationsmeldung, die vom Flyout-Zoom-Ansicht beim Laden angezeigt wird.

Jeder Textinhalt im Viewer, der lokalisiert werden kann, wird durch die spezielle Viewer-SDK-Kennung SYMBOL dargestellt. Jede SYMBOL verfügt über einen standardmäßig zugeordneten Textwert für ein englisches Gebietsschema ( `"en"`) mit dem vordefinierten Viewer bereitgestellt werden und benutzerdefinierte Werte für beliebig viele Gebietsschemas festgelegt sein können.

Beim Starten des Viewers wird das aktuelle Gebietsschema überprüft, um festzustellen, ob für jedes unterstützte SYMBOL für dieses Gebietsschema ein benutzerdefinierter Wert vorhanden ist. Ist dies der Fall, wird der benutzerdefinierte Wert verwendet. Andernfalls wird der vordefinierte Standardtext verwendet.

Benutzerdefinierte Lokalisierungsdaten können als lokalisiertes JSON-Objekt an den Viewer übergeben werden. Dieses Objekt enthält die Liste der unterstützten Gebietsschemas, die SYMBOL-Textwerte für jedes Gebietsschema und das Standardgebietsschema.

Ein Beispiel für ein solches Lokalisierungsobjekt ist:

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

Im obigen Beispiel definiert das Lokalisierungsobjekt zwei Gebietsschemata ( `"en"` und `"fr"`) und bietet Lokalisierung für zwei Elemente der Benutzeroberfläche in jedem Gebietsschema.

Der Webseitencode sollte das Lokalisierungsobjekt als Wert von `localizedTexts` -Feld des Konfigurationsobjekts. Eine alternative Option besteht darin, das Lokalisierungsobjekt durch Aufruf von `setLocalizedTexts(localizationInfo)` -Methode.

Die folgenden SYMBOLs werden unterstützt:

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>SYMBOL </p> </th> 
   <th colname="col2" class="entry"> <p>QuickInfo für ... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL </span> </p> </td> 
   <td colname="col2"> <p>ARIA-Beschriftung für Viewer-Element der obersten Ebene. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.ROLE_DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>ARIA-Rollenbeschreibung für die Hauptansichtskomponente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.USAGE_HINT </span> </p> </td> 
   <td colname="col2"> <p>ARIA-Verwendungshinweise für Tastaturbenutzer. </p> </td> 
  </tr> 
 </tbody> 
</table>
