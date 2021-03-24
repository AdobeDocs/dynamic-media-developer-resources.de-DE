---
description: Bestimmte Inhalte, die im interaktiven Bild-Viewer angezeigt werden, unterliegen der lokale Anpassung. Dazu gehören QuickInfos zu Elementen in der Benutzeroberfläche und eine Informationsmeldung, die von der Flyout-Zoom-Ansicht beim Laden angezeigt wird.
title: lokale Anpassung der Elemente der Benutzeroberfläche
feature: Dynamic Media Classic, Viewer, SDK/API, Interaktive Bilder
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 0%

---


# lokale Anpassung der Elemente der Benutzeroberfläche{#localization-of-user-interface-elements}

Bestimmte Inhalte, die im interaktiven Bild-Viewer angezeigt werden, unterliegen der lokale Anpassung. Dazu gehören QuickInfos zu Elementen in der Benutzeroberfläche und eine Informationsmeldung, die von der Flyout-Zoom-Ansicht beim Laden angezeigt wird.

Jeder Textinhalt im Viewer, der lokalisiert werden kann, wird durch den speziellen Viewer SDK-Bezeichner SYMBOL dargestellt. Jedes SYMBOL verfügt über einen Standardtextwert für ein englisches Gebietsschema ( `"en"`), das mit dem standardmäßigen Viewer bereitgestellt wird, und kann auch benutzerdefinierte Werte für so viele Gebietsschemas wie erforderlich enthalten.

Beim Beginn des Viewers wird das aktuelle Gebietsschema überprüft, um festzustellen, ob für jedes unterstützte SYMBOL für dieses Gebietsschema ein benutzerdefinierter Wert vorhanden ist. Ist dies der Fall, wird der benutzerdefinierte Wert verwendet. Andernfalls wird auf den Standardtext zurückgesetzt.

Benutzerdefinierte Daten zur lokale Anpassung können als JSON-Objekt der lokale Anpassung an den Viewer übergeben werden. Dieses Objekt enthält die Liste der unterstützten Gebietsschemata, SYMBOL-Textwerte für jedes Gebietsschema und das Standardgebietsschema.

Ein Beispiel für ein solches lokale Anpassung-Objekt ist Folgendes:

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

Im obigen Beispiel definiert das lokale Anpassung-Objekt zwei Gebietsschemas ( `"en"` und `"fr"`) und stellt lokale Anpassung für zwei Benutzeroberflächenelemente in jedem Gebietsschema bereit.

Der Webseitencode sollte das lokale Anpassung-Objekt an den Viewer-Konstruktor als Wert des Felds `localizedTexts` des Konfigurationsobjekts übergeben. Eine andere Option besteht darin, das Objekt &quot;lokale Anpassung&quot;durch Aufruf der Methode `setLocalizedTexts(localizationInfo)` weiterzugeben.

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
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL  </span> </p> </td> 
   <td colname="col2"> <p>ARIA-Beschriftung für Viewer-Element der obersten Ebene. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.ROLE_DESCRIPTION  </span> </p> </td> 
   <td colname="col2"> <p>ARIA-Rollenbeschreibung für die Hauptkomponente Ansicht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.USAGE_HINT  </span> </p> </td> 
   <td colname="col2"> <p>ARIA-Verwendungshinweise für Tastaturbenutzer. </p> </td> 
  </tr> 
 </tbody> 
</table>

