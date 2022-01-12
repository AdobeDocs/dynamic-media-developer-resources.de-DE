---
title: QuickInfos
description: Auf Desktop-Systemen verfügen einige Elemente der Benutzeroberfläche wie Schaltflächen über QuickInfos, die beim Bewegen der Maus angezeigt werden.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: bcbdd047-428b-48f8-9bd9-600f36f2e0b7
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 6%

---

# QuickInfos{#tooltips}

Auf Desktop-Systemen verfügen einige Elemente der Benutzeroberfläche wie Schaltflächen über QuickInfos, die beim Bewegen der Maus angezeigt werden.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften des Haupt-Viewer-Bereichs**

Das Erscheinungsbild von QuickInfos wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7tooltip
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-Eigenschaft </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p> Rahmenradius im Hintergrund </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-color </span> </p> </td> 
   <td colname="col2"> <p> Hintergrundrahmenfarbe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Hintergrundfarbe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Textfarbe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Schriftfamilie </span> </p> </td> 
   <td colname="col2"> <p>Textschriftart. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Schriftgröße </span> </p> </td> 
   <td colname="col2"> <p>Textschriftgröße. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Falls QuickInfo-Stile von der eingebetteten Web-Seite aus angepasst werden, müssen alle Eigenschaften enthalten `!IMPORTANT` Regel. Es ist jedoch nicht erforderlich, QuickInfos in der CSS-Datei des Viewers anzupassen.

Beispiel: Zum Einrichten von QuickInfos mit einem grauen Rahmen mit einem Radius von 3 Pixel, schwarzem Hintergrund und weißem Text, der mit Arial® geschrieben wurde, mit einer Größe von 11 Pixel:

```
.s7tooltip { 
 border-radius: 3px 3px 3px 3px; 
 border-color: #999999; 
 background-color: #000000; 
 color: #FFFFFF; 
 font-family: Arial, Helvetica, sans-serif; 
 font-size: 11px; 
}
```
