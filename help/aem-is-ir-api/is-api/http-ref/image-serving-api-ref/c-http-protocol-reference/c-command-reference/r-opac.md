---
title: opac
description: Passen Sie die Bilddeckkraft an. Ermöglicht die Verringerung der Vordergrunddeckkraft eines Bildes, Textes, einer Vollfarbe oder einer Effektebene.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 38e0e1dc-46c0-48a4-b676-f7e6d262392f
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 1%

---

# opac{#opac}

Passen Sie die Bilddeckkraft an. Ermöglicht die Verringerung der Vordergrunddeckkraft eines Bildes, Textes, einer Vollfarbe oder einer Effektebene.

`opac= *`Deckkraft`*[, *`fillOpacity`*]`

<table id="simpletable_DA4B5D86C496480886FADB284AD6047F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Deckkraft</span> </p> </td> 
  <td class="stentry"> <p>Primäre Deckkraft (0...100 int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> fillOpacity</span> </p></td> 
  <td class="stentry"> <p>Fülldeckkraft (0...100 int). </p></td> 
 </tr> 
</table>

Die Vordergrunddeckkraft einer Bildebene wird durch die Ebenenmaske oder den Alphakanal des Bildes bestimmt oder, wenn keines vorhanden ist, 100 %. Die Vordergrunddeckkraft einer Textebene beträgt 100 %, die einer durchgehenden Farbschicht wird durch `color=`.

`opac=` ändert nie die Deckkraft von Bereichen, die mit `color=` oder `bgColor=`, mit Ausnahme der Vordergrundbereiche von Vollfarben- und Effektschichten (festgelegt mit `color=`).

Wenn in einer Bild-, Text- oder einfarbigen Farbschicht angegeben, *`opacity`* wendet die gesamte Ebene einschließlich aller zugehörigen Effektebenen an, während *`fillOpacity`* gilt nur für den Inhalt der primären Ebene. Wenn in einer Effektebene angegeben, *`opacity`* wird auf die Effektebene angewendet, während *`fillOpacity`* wird ignoriert.

Die effektive Deckkraft für den Inhalt der Hauptschicht ist ( *`opacity`* &#42; *`fillOpacity`* 100). Die effektive Deckkraft der Effektschichten ist (main *`opacity`* &#42; Effekt *`opacity`* 100).

## Eigenschaften {#section-ac3f136ff1584a2eab87500b7164f7fa}

Ebenenattribut. Gilt für die aktuelle Ebene oder für das zusammengesetzte Bild, wenn `layer=comp`.

## Standard {#section-abba67ed028049048ae43405ea69b164}

`opac=100,100`, um die Deckkraft der Schicht nicht zu ändern.

## Beispiel {#section-9710810e96af40538652e8ae4aadd3be}

… `&layer=1&text=variable%20opacity&opac=90,70&effect=-1&opac=50&`…

Die Textdeckkraft in diesem Beispiel beträgt 90&#42;70/100 = 63 % und die Deckkraft der Effekteschicht 90 beträgt&#42;50/100 = 45 %.

## Verwandte Themen {#section-dbdad35ccd544590b4b11d31a9ab062e}

[color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) , [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab)
