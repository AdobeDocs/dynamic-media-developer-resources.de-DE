---
title: QuickInfos
description: Auf Desktop-Systemen verfügen einige Elemente der Benutzeroberfläche wie Schaltflächen über QuickInfos, die beim Bewegen des Mauszeigers angezeigt werden.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: b4604528-93f6-440c-b676-7b4c89fff6c8
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---

# QuickInfos{#tooltips}

Auf Desktop-Systemen verfügen einige Elemente der Benutzeroberfläche wie Schaltflächen über QuickInfos, die beim Bewegen des Mauszeigers angezeigt werden.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften des Haupt-Viewer-Bereichs**

Das Erscheinungsbild von QuickInfos wird mit dem folgenden CSS-Klassenselektor gesteuert:

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
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Rahmenradius im Hintergrund </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Hintergrundfarbe des Rahmens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Hintergrundfarbe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Textfarbe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Name der Textschriftart. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Textschriftgröße. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Wenn QuickInfo-Stile innerhalb der einbettenden Web-Seite angepasst werden, müssen alle Eigenschaften `!IMPORTANT` Regel enthalten. Dieser Schritt ist nicht erforderlich, wenn QuickInfos in der CSS-Datei des Viewers angepasst werden.

Beispiel - Zum Einrichten von QuickInfos mit einem grauen Rahmen mit einem 3-Pixel-Eckenradius, schwarzem Hintergrund und weißem Text in Arial®, 11 Pixel Größe:

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
