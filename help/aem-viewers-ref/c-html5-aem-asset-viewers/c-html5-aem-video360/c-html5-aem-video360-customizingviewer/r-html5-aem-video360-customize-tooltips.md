---
title: Tooltips
description: Auf Desktop-Systemen verfügen einige Elemente der Benutzeroberfläche, wie Schaltflächen, über QuickInfos, die beim Bewegen des Mauszeigers angezeigt werden.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 051bfbed-103e-4fcf-9f01-93f03730397a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 0%

---

# Tooltips{#tooltips}

Auf Desktop-Systemen verfügen einige Elemente der Benutzeroberfläche, wie Schaltflächen, über QuickInfos, die beim Bewegen des Mauszeigers angezeigt werden.

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
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Textschriftgröße. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Falls QuickInfo-Stile von der eingebetteten Webseite aus angepasst werden, müssen alle Eigenschaften die Regel `!IMPORTANT` enthalten. Diese Regel ist nicht erforderlich, wenn QuickInfos in der CSS-Datei des Viewers angepasst werden.

Beispiel - So richten Sie QuickInfos ein, die einen grauen Rahmen mit einem Radius von drei Pixel, schwarzem Hintergrund und weißem Text in Arial® haben, und zwar 11 Pixel:

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
