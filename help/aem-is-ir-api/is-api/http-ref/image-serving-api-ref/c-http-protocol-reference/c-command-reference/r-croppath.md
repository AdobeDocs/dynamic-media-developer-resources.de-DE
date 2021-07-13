---
description: Ermöglicht das Zuschneiden auf den Begrenzungsrahmen eines eingebetteten benannten Pfads. Dieser Zuschnitt ändert wiederum die Größe des Bildes.
solution: Experience Manager
title: cropPathE
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 78e9f994-d638-49a7-ac42-3146e47210e3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 2%

---

# cropPathE{#croppathe}

Ermöglicht das Zuschneiden auf den Begrenzungsrahmen eines eingebetteten benannten Pfads. Dieser Zuschnitt ändert wiederum die Größe des Bildes.

`cropPathE= *``*&#42;[, *`pathNamepathName`*]`

<table id="table_598304852E844456AB3AC9FF1F178B71"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> pathName</span></span> </p> </td> 
   <td colname="col2"> <p>Name des Pfades, der in das Ebenenquellbild eingebettet ist (nur ASCII). </p> <p> <span class="codeph"><span class="varname"> </span></span> pathNames ist der Name eines Pfades, der in das Ebenenquellbild eingebettet ist. Der Pfad wird bei Bedarf automatisch umgewandelt, um die relative Ausrichtung am Bildinhalt zu gewährleisten. Wenn mehr als ein <span class="codeph"><span class="varname"> pathName</span></span> angegeben ist, schneidet der Server nacheinander auf den Begrenzungsrahmen jedes Pfads zu. Jeder <span class="codeph"><span class="varname"> pathName</span></span>, der nicht im Quellbild gefunden wird, wird ignoriert. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-acf7272ba93a4bbba818b8e6aa4dcea5}

Ebenenattribut. Gilt für die aktuelle Ebene oder für das zusammengesetzte Bild, wenn `layer=comp` Wird von Effektebenen ignoriert.

`cropPathE=` wird ignoriert, wenn kein Pfad mit dem angegebenen Namen im Ebenenquellenbild gefunden wird oder wenn die Ebenenquelle kein Bild ist.

## Standard {#section-d1986aa31af14767aeb1b4a57add67f4}

Keine, kein zusätzliches Zuschneiden der Ebene.

## Verwandte Themen {#section-a60f6e37ebf14e458519fcc4d2cc911d}

[crop](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab),  [clipPathE](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
