---
description: Die Hauptversion besteht aus dem Katalogbild. Es kann wischen, um zu einer anderen Seite zu gelangen, oder gezoomt.
seo-description: Die Hauptversion besteht aus dem Katalogbild. Es kann wischen, um zu einer anderen Seite zu gelangen, oder gezoomt.
seo-title: Ansicht der Seite
solution: Experience Manager
title: Ansicht der Seite
topic: Dynamic media
uuid: 5e247f56-f0da-487b-8e03-587b9d36aa39
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 2%

---


# Ansicht der Seite{#page-view}

Die Hauptversion besteht aus dem Katalogbild. Es kann wischen, um zu einer anderen Seite zu gelangen, oder gezoomt.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften des Haupt-Viewer-Bereichs**

Das Erscheinungsbild des Anzeigebereichs wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogviewer .s7pageview
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
   <td colname="col2"> <p> Hintergrundfarbe der Haupt-Ansicht im Hexadezimalformat. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cursor  </span> </p> </td> 
   <td colname="col2"> <p>Cursor, der über der Haupt-Ansicht angezeigt wird. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel - um die Ansicht transparent zu machen.

```
.s7ecatalogviewer .s7pageview { 
 background-color: transparent; 
}
```

Auf Desktop-Systemen unterstützt die Komponente die Attributauswahl `cursortype`, die auf die Klasse `.s7pageview` angewendet werden kann, und steuert den Cursortyp basierend auf Komponentenstatus und Benutzeraktion. Die folgenden `cursortype`-Werte werden unterstützt:

<table id="table_45B83F6CCDE84C36B0E087CA9144BFE6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Wert </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Standard </span> </p> </td> 
   <td colname="col2"> <p>Wird angezeigt, wenn das Bild aufgrund einer geringen Bildauflösung, Komponenteneinstellungen oder beidem nicht gezoombar ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomin  </span> </p> </td> 
   <td colname="col2"> <p>Wird angezeigt, wenn das Bild vergrößert werden kann. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zurücksetzen </span> </p> </td> 
   <td colname="col2"> <p>Wird angezeigt, wenn das Bild den maximalen Zoomgrad erreicht hat und auf den Ausgangszustand zurückgesetzt werden kann. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ziehen </span> </p> </td> 
   <td colname="col2"> <p>Wird angezeigt, wenn der Benutzer das Bild verschiebt, das gezoomt ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Folie  </span> </p> </td> 
   <td colname="col2"> <p>Wird angezeigt, wenn der Benutzer einen Bildtausch durch horizontales Blättern oder Klick durchführt. </p> </td> 
  </tr> 
 </tbody> 
</table>

Der Seitentrenner, der die linke und rechte Seite des Katalogstreublattes visuell trennt, wird mit der folgenden CSS-Klassenauswahl gesteuert:

`.s7ecatalogviewer .s7pageview .s7pagedivider`

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
   <td colname="col2"> <p> Die Breite des Seitenunterteilers. Auf <span class="codeph"> 0 </span> px setzen, um die Trennlinie vollständig auszublenden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>Das Bild, das Sie als Seitenunterteilung verwenden möchten. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Es wird ein Seitenteiler mit einer Breite von 40 Pixeln und ein halbtransparentes Bild verwendet.

```
.s7ecatalogviewer .s7pageview .s7pagedivider { 
 width:40px; 
 background-image:url(images/sdk/divider.png); 
}
```

>[!NOTE]
>
>Wenn der Modifikator `frametransition` auf `turn` oder `auto` (auf Desktop-Systemen) eingestellt ist, wird das Erscheinungsbild des Seitenteilers mit dem Modifikator `pageturnstyle` gesteuert und die CSS-Klasse `.s7pagedivider` wird ignoriert.

Es ist möglich, die Anzeige der benutzerdefinierten Mauszeiger über dem Hauptviewer-Bereich zu konfigurieren. Dies wird mithilfe der zusätzlichen Attributselektoren gesteuert, die auf die CSS-Klasse `.s7ecatalogviewer .s7pageview` angewendet werden:

<table id="table_908164DECF9347A19A9696A23BBDB1A2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-Eigenschaft </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Standard </span> </p> </td> 
   <td colname="col2"> <p> Normalerweise wird ein Pfeil für ein Bild angezeigt, das nicht vergrößert werden kann. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomin  </span> </p> </td> 
   <td colname="col2"> <p> Zeigt an, wann ein Bild vergrößert werden kann. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zurücksetzen </span> </p> </td> 
   <td colname="col2"> <p>Zeigt an, wann ein Bild maximal gezoomt wird und zurückgesetzt werden kann. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ziehen </span> </p> </td> 
   <td colname="col2"> <p>Zeigt an, wenn der Benutzer beim Zoomen des Bildes den Vorgang "Ziehen"durchführt </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Folie  </span> </p> </td> 
   <td colname="col2"> <p>Zeigt an, wann der Benutzer den Bildaustausch mithilfe der Foliengeste durchführt </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Sie haben unterschiedliche Mauszeiger für jeden Typ des Komponentenstatus.

```
.s7ecatalogviewer .s7pageview[cursortype="default"] { 
cursor:auto; 
} 
.s7ecatalogviewer .s7pageview[cursortype="zoomin"] { 
cursor:url(images/zoomin_cursor.cur), auto; 
} 
.s7ecatalogviewer .s7pageview[cursortype="reset"] { 
cursor:url(images/zoomout_cursor.cur), auto; 
} 
.s7ecatalogviewer .s7pageview [cursortype="slide"] { 
cursor:url(images/slide_cursor.cur), auto; 
} 
.s7ecatalogviewer .s7pageview[cursortype="drag"] { 
cursor:url(images/drag_cursor.cur), auto; 
}
```

