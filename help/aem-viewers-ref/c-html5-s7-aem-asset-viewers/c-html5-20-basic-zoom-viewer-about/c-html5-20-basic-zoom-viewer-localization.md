---
title: Lokalisierung der Elemente der Benutzeroberfläche
description: Bestimmte Inhalte, die der einfache Zoom-Viewer anzeigt, können lokalisiert werden, einschließlich Zoom-Schaltflächen und einer Vollbildschaltfläche.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 8c399b64-e278-41bc-a9eb-692812979fea
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 0%

---

# Lokalisierung der Elemente der Benutzeroberfläche{#localization-of-user-interface-elements}

Bestimmte Inhalte, die der einfache Zoom-Viewer anzeigt, können lokalisiert werden, einschließlich Zoom-Schaltflächen und einer Vollbildschaltfläche.

Jeder Textinhalt im Viewer, der lokalisiert werden kann, wird durch eine spezielle Viewer-SDK-ID namens SYMBOL dargestellt. Jedes SYMBOL verfügt über einen standardmäßig zugewiesenen Textwert für das englische Gebietsschema ( `"en"`), das mit dem vordefinierten Viewer bereitgestellt wird, und kann auch benutzerdefinierte Werte für beliebig viele Gebietsschemas enthalten.

Beim Starten des Viewers wird das aktuelle Gebietsschema überprüft, um festzustellen, ob für jede unterstützte SYMBOL im Gebietsschema ein benutzerdefinierter Wert vorhanden ist. Ist dies der Fall, wird der benutzerdefinierte Wert verwendet. Andernfalls wird der vordefinierte Standardtext verwendet.

Benutzerdefinierte Lokalisierungsdaten können als lokalisiertes JSON-Objekt an den Viewer übergeben werden. Ein solches Objekt enthält die Liste der unterstützten Gebietsschemas, die SYMBOL-Textwerte für jedes Gebietsschema und das Standardgebietsschema.

Ein Beispiel für ein solches Lokalisierungsobjekt:

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

Im obigen Beispiel definiert das Lokalisierungsobjekt zwei Gebietsschemas ( `"en"` und `"fr"`) und stellt die Lokalisierung von zwei Benutzeroberflächenelementen in jedem Gebietsschema bereit.

Der Webseitencode sollte dieses Lokalisierungsobjekt als Wert des Felds `localizedTexts` des Konfigurationsobjekts an den Viewer-Konstruktor übergeben. Eine alternative Option besteht darin, das Lokalisierungsobjekt durch Aufruf der Methode `setLocalizedTexts(localizationInfo)` weiterzugeben.

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
   <td colname="col1"> <p> <span class="codeph"> container.LABEL </span> </p> </td> 
   <td colname="col2"> <p>ARIA-Beschriftung für das Viewer-Element der obersten Ebene. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.ROLE_DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>ARIA-Rollenbeschreibung für die Hauptansichtskomponente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.USAGE_HINT </span> </p> </td> 
   <td colname="col2"> <p>ARIA-Verwendungshinweise für Tastaturbenutzer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CloseButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche "Schließen". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomInButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche "Vergrößern" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomOutButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche "Verkleinern" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomResetButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche zum Zurücksetzen des Zooms </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche im Vollbildmodus im Normalzustand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>Schaltfläche im Vollbildmodus. </p> </td> 
  </tr> 
 </tbody> 
</table>
