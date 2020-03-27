---
description: Pfad des umgekehrten Ebenenclips. Gibt einen Ausschlussclip-Pfad für die aktuelle Ebene an. Alle Teile der Ebene, die innerhalb des durch clipXPath= definierten Bereichs liegen, werden transparent dargestellt.
seo-description: Pfad des umgekehrten Ebenenclips. Gibt einen Ausschlussclip-Pfad für die aktuelle Ebene an. Alle Teile der Ebene, die innerhalb des durch clipXPath= definierten Bereichs liegen, werden transparent dargestellt.
seo-title: clipXPath
solution: Experience Manager
title: clipXPath
topic: Scene7 Image Serving - Image Rendering API
uuid: a4062f3f-5dba-4514-acde-e1b7d608a2e9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# clipXPath{#clipxpath}

Pfad des umgekehrten Ebenenclips. Gibt einen Ausschlussclip-Pfad für die aktuelle Ebene an. Alle Teile der Ebene, die innerhalb des durch clipXPath= definierten Bereichs liegen, werden transparent dargestellt.

`clipXPath= *`pathDefinition`*`

`clipXPathE= *``*&#42;[, *`pathNamepathName`*]`

<table id="simpletable_27AFC3A694874CF8B673460820EFD90D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathDefinition</span></span> </p> </td> 
  <td class="stentry"> <p>Path data. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathName</span></span> </p> </td> 
  <td class="stentry"> <p>Name des Pfads, der in das Ebenenquellbild eingebettet ist (nur ASCII). </p></td> 
 </tr> 
</table>

Weitere Informationen, einschließlich einer Beschreibung von [pathName](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) und ` *`pathDefinition`*` , finden Sie unter ` *`clipPath=`*`.

## Eigenschaften {#section-acf7272ba93a4bbba818b8e6aa4dcea5}

Ebenenattribut. Gilt für die aktuelle Ebene oder für das Composite-Bild, falls `layer=comp`dies der Fall ist. Wird ignoriert, wenn `clipPath=` nicht angegeben. Von Effektebenen ignoriert.

## Standard {#section-d1986aa31af14767aeb1b4a57add67f4}

Keine.

## Verwandte Themen {#section-a60f6e37ebf14e458519fcc4d2cc911d}

[clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
