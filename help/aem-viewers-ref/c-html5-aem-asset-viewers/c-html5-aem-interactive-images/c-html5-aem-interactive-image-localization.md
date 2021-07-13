---
description: Bestimmte Inhalte, die der interaktive Bild-Viewer anzeigt, können lokalisiert werden. Dazu gehören QuickInfos für Benutzeroberflächenelemente und eine Informationsmeldung, die vom Flyout-Zoom-Ansicht beim Laden angezeigt wird.
title: Lokalisierung der Elemente der Benutzeroberfläche
feature: Dynamic Media Classic,Viewer,SDK/API,Interaktive Bilder
role: Developer,User
exl-id: 19749c74-5c31-4dcf-ab07-0e7f10176a86
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 0%

---

# Lokalisierung der Elemente der Benutzeroberfläche{#localization-of-user-interface-elements}

Bestimmte Inhalte, die der interaktive Bild-Viewer anzeigt, können lokalisiert werden. Dazu gehören QuickInfos für Benutzeroberflächenelemente und eine Informationsmeldung, die vom Flyout-Zoom-Ansicht beim Laden angezeigt wird.

Jeder Textinhalt im Viewer, der lokalisiert werden kann, wird durch die spezielle Viewer-SDK-Kennung SYMBOL dargestellt. Jedes SYMBOL verfügt über einen standardmäßigen zugeordneten Textwert für ein englisches Gebietsschema ( `"en"`), das mit dem vordefinierten Viewer bereitgestellt wird. Außerdem können benutzerdefinierte Werte für beliebig viele Gebietsschemata festgelegt werden.

Beim Starten des Viewers wird das aktuelle Gebietsschema überprüft, um festzustellen, ob für jedes unterstützte SYMBOL für dieses Gebietsschema ein benutzerdefinierter Wert vorhanden ist. Ist dies der Fall, wird der benutzerdefinierte Wert verwendet. andernfalls wird auf den vordefinierten Standardtext zurückgegriffen.

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

Im obigen Beispiel definiert das Lokalisierungsobjekt zwei Gebietsschemata ( `"en"` und `"fr"`) und stellt die Lokalisierung für zwei Benutzeroberflächenelemente in jedem Gebietsschema bereit.

Der Webseitencode sollte das Lokalisierungsobjekt als Wert des Felds `localizedTexts` des Konfigurationsobjekts an den Viewer-Konstruktor übergeben. Eine alternative Option besteht darin, das Lokalisierungsobjekt durch Aufruf der Methode `setLocalizedTexts(localizationInfo)` weiterzugeben.

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
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL  </span> </p> </td> 
   <td colname="col2"> <p>ARIA-Beschriftung für Viewer-Element der obersten Ebene. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.ROLE_DESCRIPTION  </span> </p> </td> 
   <td colname="col2"> <p>ARIA-Rollenbeschreibung für die Hauptansichtskomponente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.USAGE_HINT  </span> </p> </td> 
   <td colname="col2"> <p>ARIA-Verwendungshinweise für Tastaturbenutzer. </p> </td> 
  </tr> 
 </tbody> 
</table>
