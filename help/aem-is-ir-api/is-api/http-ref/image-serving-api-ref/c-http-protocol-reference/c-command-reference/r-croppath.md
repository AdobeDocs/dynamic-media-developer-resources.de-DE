---
description: Hiermit können Sie auf den Begrenzungsrahmen eines eingebetteten benannten Pfads zuschneiden. Diese Beschneidung ändert wiederum die Größe des Bildes.
solution: Experience Manager
title: cutPathE
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 2%

---


# cutPathE{#croppathe}

Hiermit können Sie auf den Begrenzungsrahmen eines eingebetteten benannten Pfads zuschneiden. Diese Beschneidung ändert wiederum die Größe des Bildes.

`cropPathE= *``*&#42;[, *`pathNamepathName`*]`

<table id="table_598304852E844456AB3AC9FF1F178B71"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> pathName</span></span> </p> </td> 
   <td colname="col2"> <p>Name des Pfads, der in das Ebenenquellbild eingebettet ist (nur ASCII). </p> <p> <span class="codeph"><span class="varname"> </span></span> pathNames ist der Name eines Pfads, der im Quellbild der Ebene eingebettet ist. Der Pfad wird nach Bedarf automatisch transformiert, um die relative Ausrichtung am Bildinhalt beizubehalten. Wenn mehr als ein <span class="codeph"><span class="varname"> pathName</span></span> angegeben ist, schneidet der Server nacheinander auf den Begrenzungsrahmen jedes Pfads ab. Alle <span class="codeph"><span class="varname"> pathName</span></span>, die nicht im Quellbild gefunden wurden, werden ignoriert. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-acf7272ba93a4bbba818b8e6aa4dcea5}

Ebenenattribut. Gilt für die aktuelle Ebene oder für das Composite-Bild, wenn `layer=comp`. Von Effektebenen ignoriert.

`cropPathE=` wird ignoriert, wenn im Quellbild der Ebene kein Pfad mit dem angegebenen Namen gefunden wird oder wenn die Ebenenquelle kein Bild ist.

## Standard {#section-d1986aa31af14767aeb1b4a57add67f4}

Ohne, wenn die Ebene nicht weiter beschnitten werden soll.

## Verwandte Themen {#section-a60f6e37ebf14e458519fcc4d2cc911d}

[beschneiden](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab),  [clipPathE](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
