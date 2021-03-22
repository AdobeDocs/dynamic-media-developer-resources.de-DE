---
description: Die Ansicht "Main"besteht aus dem Rotationsbild, wenn es sich bei dem aktuellen Asset um ein Rotationsset handelt.
seo-description: Die Ansicht "Main"besteht aus dem Rotationsbild, wenn es sich bei dem aktuellen Asset um ein Rotationsset handelt.
seo-title: Ansicht
solution: Experience Manager
title: Ansicht
uuid: f1edbcc4-966a-4ec6-8ba9-a76f3ae51733
feature: Dynamic Media Classic,Viewer,SDK/API,Mix-Mediensets
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---


# Rotationsset-Ansicht{#spin-view}

Die Ansicht &quot;Main&quot;besteht aus dem Rotationsbild, wenn es sich bei dem aktuellen Asset um ein Rotationsset handelt.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften des Haupt-Viewer-Bereichs**

Das Erscheinungsbild des Anzeigebereichs wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7mixedmediaviewer .s7spinview
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
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> Hintergrundfarbe im Hexadezimalformat der Rotationsfarbe. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel - um die Ansicht transparent zu machen.

```
.s7mixedmediaviewer .s7spinview { 
 background-color: transparent; 
}
```

