---
title: Seitenansicht
description: Die Hauptansicht besteht aus dem Katalogbild. Sie kann gewischt werden, um zu einer anderen Seite zu gelangen, oder gezoomt werden.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: d98babad-96c7-419a-abf2-3b6657d550eb
source-git-commit: 67e12fae514341137e4218ea950f34da0d9997f3
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 1%

---

# Seitenansicht{#page-view}

Die Hauptansicht besteht aus dem Katalogbild. Sie kann gewischt werden, um zu einer anderen Seite zu gelangen, oder gezoomt werden.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften des Haupt-Viewer-Bereichs**

Das Erscheinungsbild des Anzeigebereichs wird mit dem folgenden CSS-Klassenselektor gesteuert:

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
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Hintergrundfarbe der Hauptansicht im Hexadezimalformat. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Cursor-</span> </p> </td> 
   <td colname="col2"> <p>Cursor, der über der Hauptansicht angezeigt wird. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel - um die Hauptansicht transparent zu gestalten.

```
.s7ecatalogsearchviewer .s7pageview { 
 background-color: transparent; 
}
```

Auf Desktop-Systemen unterstützt die Komponente den `cursortype`-Attributselektor , der auf `.s7pageview` Klasse angewendet werden kann und den Cursortyp basierend auf dem Komponentenstatus und der Benutzeraktion steuert. Die folgenden `cursortype` werden unterstützt:

<table id="table_45B83F6CCDE84C36B0E087CA9144BFE6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Wert </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Wird angezeigt, wenn das Bild aufgrund einer geringen Bildauflösung, Komponenteneinstellungen oder beidem nicht zoombar ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Zoom-</span> </p> </td> 
   <td colname="col2"> <p>Wird angezeigt, wenn das Bild vergrößert werden kann. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Wird angezeigt, wenn sich das Bild im maximalen Zoombereich befindet und auf den Ausgangszustand zurückgesetzt werden kann. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Drag </span> </p> </td> 
   <td colname="col2"> <p>Wird angezeigt, wenn Benutzende das Bild schwenken, das vergrößert ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Wird angezeigt, wenn Benutzende durch horizontales Wischen oder Klicken ein Bild austauschen. </p> </td> 
  </tr> 
 </tbody> 
</table>

Der Seitenteiler, der die linken und rechten Seiten der Katalogausbreitung visuell trennt, wird mit dem folgenden CSS-Klassenselektor gesteuert:

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
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p> Die Breite des Seitenteilers. Legen Sie auf <span class="codeph"> 0 </span> px fest, um die Trennlinie vollständig auszublenden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundbild-</span> </p> </td> 
   <td colname="col2"> <p>Das Bild, das Sie als Seitenteiler verwenden möchten. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Für einen Seitenteiler mit einer Breite von 40 Pixeln mit halbtransparentem Bild.

```
.s7ecatalogsearchviewer .s7pageview .s7pagedivider { 
 width:40px; 
 background-image:url(images/sdk/divider.png); 
}
```

>[!NOTE]
>
>Wenn der Modifikator `frametransition` auf `turn` oder `auto` (auf Desktop-Systemen) festgelegt ist, wird das Erscheinungsbild des Seitenteils mit dem Modifikator `pageturnstyle` gesteuert und die `.s7pagedivider` CSS-Klasse wird ignoriert.

Es ist möglich, die Anzeige der benutzerdefinierten Mauszeiger über dem Haupt-Viewer-Bereich zu konfigurieren. Diese Funktion wird mit den zusätzlichen Attributauswahlen gesteuert, die auf `.s7ecatalogsearchviewer .s7pageview` CSS-Klasse angewendet werden:

<table id="table_908164DECF9347A19A9696A23BBDB1A2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-Eigenschaft </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Normalerweise wird für nicht zoombare Bilder ein Pfeil angezeigt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Zoom-</span> </p> </td> 
   <td colname="col2"> <p> Zeigt an, wann ein Bild vergrößert werden kann. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Zeigt an, wann ein Bild im maximalen Zoom ist und zurückgesetzt werden kann. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Drag </span> </p> </td> 
   <td colname="col2"> <p>Zeigt an, wann der Benutzer einen Ziehvorgang für ein vergrößertes Bild durchführt </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Zeigt an, wann der Benutzer den Bildaustausch mit der Foliengeste durchführt </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Für jeden Komponententyp stehen unterschiedliche Mauszeiger zur Verfügung.

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
