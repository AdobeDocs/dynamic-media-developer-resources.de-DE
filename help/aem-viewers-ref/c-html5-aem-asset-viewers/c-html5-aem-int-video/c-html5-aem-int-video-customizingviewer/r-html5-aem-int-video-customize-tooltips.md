---
description: Auf Desktop-Systemen verfügen einige Elemente der Benutzeroberfläche, wie Schaltflächen, über QuickInfos, die beim Bewegen der Maus angezeigt werden.
seo-description: Auf Desktop-Systemen verfügen einige Elemente der Benutzeroberfläche, wie Schaltflächen, über QuickInfos, die beim Bewegen der Maus angezeigt werden.
seo-title: QuickInfos
solution: Experience Manager
title: QuickInfos
topic: Dynamic media
uuid: 763cdda7-4938-4884-8040-7e4017e6a0d8
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Tooltips{#tooltips}

Auf Desktop-Systemen verfügen einige Elemente der Benutzeroberfläche, wie Schaltflächen, über QuickInfos, die beim Bewegen der Maus angezeigt werden.

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
   <td colname="col2"> <p> Rahmenfarbe im Hintergrund </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Textschriftart. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Schriftgröße des Textes. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Wenn QuickInfo-Stile von der Einbettungswebseite aus angepasst werden, müssen alle Eigenschaften die `!IMPORTANT` Regel enthalten. Dies ist nicht erforderlich, wenn QuickInfos in der CSS-Datei des Viewers angepasst werden.

## Beispiel {#section-59e009fd05b14019936aba04d7ca779d}

So richten Sie QuickInfos mit einem grauen Rand mit einem Radius von drei Pixeln, einem schwarzen Hintergrund und einem weißen Text in Arial ein (11 Pixel):

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

