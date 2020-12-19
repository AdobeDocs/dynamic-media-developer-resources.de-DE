---
description: Auf Desktop-Systemen haben einige Benutzeroberflächenelemente wie Schaltflächen QuickInfos, die beim Bewegen der Maus angezeigt werden.
seo-description: Auf Desktop-Systemen haben einige Benutzeroberflächenelemente wie Schaltflächen QuickInfos, die beim Bewegen der Maus angezeigt werden.
seo-title: QuickInfos
solution: Experience Manager
title: QuickInfos
topic: Dynamic media
uuid: 2cbf8a22-5d0e-46e3-b6e3-29739439558b
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 5%

---


# QuickInfos{#tooltips}

Auf Desktop-Systemen haben einige Benutzeroberflächenelemente wie Schaltflächen QuickInfos, die beim Bewegen der Maus angezeigt werden.

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
   <td colname="col1"> <p> <span class="codeph"> border-radius  </span> </p> </td> 
   <td colname="col2"> <p> Rahmenradius im Hintergrund </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-color  </span> </p> </td> 
   <td colname="col2"> <p> Rahmenfarbe im Hintergrund </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> Hintergrundfarbe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Textfarbe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Textschriftart. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Schriftgröße des Textes. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Wenn QuickInfo-Stile von der Einbettungswebseite aus angepasst werden, müssen alle Eigenschaften die Regel `!IMPORTANT` enthalten. Dies ist nicht erforderlich, wenn QuickInfos in der CSS-Datei des Viewers angepasst werden.

Beispiel: So richten Sie QuickInfos ein, die einen grauen Rand mit einem Radius von 3 Pixel, einen schwarzen Hintergrund und einen weißen Text mit einer Größe von 11 Pixel haben:

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

