---
description: Umgekehrter Ebenenbeschneidungspfad. Gibt einen Ausschlussklammern-Pfad für die aktuelle Ebene an. Alle Teile der Ebene, die innerhalb des durch clipXPath= definierten Bereichs liegen, werden transparent dargestellt.
solution: Experience Manager
title: clipXPath
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7d7e92f5-856f-4d62-a5d3-4726d7b43792
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 5%

---

# clipXPath{#clipxpath}

Umgekehrter Ebenenbeschneidungspfad. Gibt einen Ausschlussklammern-Pfad für die aktuelle Ebene an. Alle Teile der Ebene, die innerhalb des durch clipXPath= definierten Bereichs liegen, werden transparent dargestellt.

`clipXPath= *`pathDefinition`*`

`clipXPathE= *``*&#42;[, *`pathNamepathName`*]`

<table id="simpletable_27AFC3A694874CF8B673460820EFD90D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathDefinition</span> </span> </p> </td> 
  <td class="stentry"> <p>Path data. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathName</span> </span> </p> </td> 
  <td class="stentry"> <p>Name des Pfades, der in das Ebenenquellbild eingebettet ist (nur ASCII). </p></td> 
 </tr> 
</table>

Weitere Informationen, einschließlich einer Beschreibung von `*`pathName`*` und `*`pathDefinition`*`, finden Sie unter [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) .

## Eigenschaften {#section-acf7272ba93a4bbba818b8e6aa4dcea5}

Ebenenattribut. Gilt für die aktuelle Ebene oder für das zusammengesetzte Bild, wenn `layer=comp` Wird ignoriert, wenn `clipPath=` nicht angegeben ist. Wird von Effektebenen ignoriert.

## Standard {#section-d1986aa31af14767aeb1b4a57add67f4}

Keine.

## Verwandte Themen {#section-a60f6e37ebf14e458519fcc4d2cc911d}

[clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
