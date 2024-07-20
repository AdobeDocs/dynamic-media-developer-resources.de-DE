---
title: Seitenansicht
description: Die Hauptansicht besteht aus dem Katalogbild. Es kann wischt werden, um zu einer anderen Seite zu gelangen oder zu zoomen.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: d98babad-96c7-419a-abf2-3b6657d550eb
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 1%

---

# Seitenansicht{#page-view}

Die Hauptansicht besteht aus dem Katalogbild. Es kann wischt werden, um zu einer anderen Seite zu gelangen oder zu zoomen.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften des Haupt-Viewer-Bereichs**

Das Erscheinungsbild des Anzeigebereichs wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7pageview
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
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Hintergrundfarbe der Hauptansicht im hexadezimalen Format. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Cursor </span> </p> </td> 
   <td colname="col2"> <p>Cursor, der über der Hauptansicht angezeigt wird. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel - um die Hauptansicht transparent zu machen.

```
.s7ecatalogsearchviewer .s7pageview { 
 background-color: transparent; 
}
```

Auf Desktop-Systemen unterstützt die Komponente die Attributauswahl `cursortype` , die auf die Klasse `.s7pageview` angewendet werden kann, und steuert den Typ des Cursors basierend auf dem Komponentenstatus und der Benutzeraktion. Die folgenden `cursortype` -Werte werden unterstützt:

<table id="table_45B83F6CCDE84C36B0E087CA9144BFE6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Wert </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> default </span> </p> </td> 
   <td colname="col2"> <p>Wird angezeigt, wenn das Bild aufgrund einer geringen Bildauflösung, Komponenteneinstellungen oder beidem nicht vergrößert werden kann. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomin </span> </p> </td> 
   <td colname="col2"> <p>Wird angezeigt, wenn das Bild vergrößert werden kann. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> reset </span> </p> </td> 
   <td colname="col2"> <p>Wird angezeigt, wenn sich das Bild auf dem maximalen Zoomfaktor befindet und auf den anfänglichen Status zurückgesetzt werden kann. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ziehen </span> </p> </td> 
   <td colname="col2"> <p>Wird angezeigt, wenn der Benutzer das Bild schaltet, das gezoomt ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Folie </span> </p> </td> 
   <td colname="col2"> <p>Wird angezeigt, wenn der Benutzer einen Bildtausch durch horizontales Wischen oder Klick durchführt. </p> </td> 
  </tr> 
 </tbody> 
</table>

Der Seitenaufteiler, der die linke und rechte Seite des Katalogaufschlags visuell trennt, wird mit der folgenden CSS-Klassenauswahl gesteuert:

`.s7ecatalogsearchviewer .s7pageview .s7pagedivider`

<table id="table_77EBC9A77BF14CF4974F8F43C709A207"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-Eigenschaft </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Die Breite des Seiten-Dividers. Setzen Sie sie auf <span class="codeph"> 0 </span> px , um die Trennlinie vollständig auszublenden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Das Bild, das Sie als Seitenaufteilung verwenden möchten. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Um einen Seitenaufleger mit einer Breite von 40 Pixel mit einem halbtransparenten Bild zu haben.

```
.s7ecatalogsearchviewer .s7pageview .s7pagedivider { 
 width:40px; 
 background-image:url(images/sdk/divider.png); 
}
```

>[!NOTE]
>
>Wenn der Modifikator `frametransition` auf `turn` oder `auto` (auf Desktop-Systemen) gesetzt ist, wird das Erscheinungsbild des Seitenunterteilers mit dem Modifikator `pageturnstyle` gesteuert und die CSS-Klasse `.s7pagedivider` wird ignoriert.

Es ist möglich, die Anzeige der benutzerdefinierten Mauszeiger über dem Hauptanzeige-Bereich zu konfigurieren. Diese Fähigkeit wird durch zusätzliche Attributselektoren gesteuert, die auf die CSS-Klasse `.s7ecatalogsearchviewer .s7pageview` angewendet werden:

<table id="table_908164DECF9347A19A9696A23BBDB1A2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-Eigenschaft </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> default </span> </p> </td> 
   <td colname="col2"> <p> Normalerweise wird ein Pfeil für ein Bild angezeigt, das nicht vergrößert werden kann. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomin </span> </p> </td> 
   <td colname="col2"> <p> Zeigt an, wann ein Bild vergrößert werden kann. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> reset </span> </p> </td> 
   <td colname="col2"> <p>Zeigt an, wann ein Bild maximal zoomt und zurückgesetzt werden kann. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ziehen </span> </p> </td> 
   <td colname="col2"> <p>Zeigt an, wann der Benutzer beim Zoomen des Bildes den Ziehvorgang durchführt </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Folie </span> </p> </td> 
   <td colname="col2"> <p>Zeigt an, wann der Benutzer einen Bildtausch mithilfe einer Foliengeste durchführt </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Für jeden Komponententyp gibt es unterschiedliche Mauszeiger.

```
.s7ecatalogsearchviewer .s7pageview[cursortype="default"] { 
cursor:auto; 
} 
.s7ecatalogsearchviewer .s7pageview[cursortype="zoomin"] { 
cursor:url(images/zoomin_cursor.cur), auto; 
} 
.s7ecatalogsearchviewer .s7pageview[cursortype="reset"] { 
cursor:url(images/zoomout_cursor.cur), auto; 
} 
.s7ecatalogsearchviewer .s7pageview [cursortype="slide"] { 
cursor:url(images/slide_cursor.cur), auto; 
} 
.s7ecatalogsearchviewer .s7pageview[cursortype="drag"] { 
cursor:url(images/drag_cursor.cur), auto; 
}
```
