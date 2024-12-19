---
title: OnFailSel
description: Handhabung von Auswahlfehlern. Gibt die Aktion an, die ausgeführt werden soll, wenn der Befehl sel= fehlschlägt, weil sich die angegebene Pixelposition nicht im Maskenbereich eines auswählbaren Objekts befindet.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d5485569-def8-4e16-9f0e-7dd30d38439d
source-git-commit: 67e12fae514341137e4218ea950f34da0d9997f3
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 6%

---

# OnFailSel{#onfailsel}

Handhabung von Auswahlfehlern. Gibt die Aktion an, die ausgeführt werden soll, wenn der `sel=`-Befehl fehlschlägt, weil sich die angegebene Pixelposition nicht im Maskenbereich eines auswählbaren Objekts befindet.

## Eigenschaften {#section-cec491e6c5c744f9bfafaaa9d8774f83}

Aufzählung.

<table id="simpletable_1CFD2BC6F9BC4D2AB372EAF115B7F2FC"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>Von <span class="codeph"> standardmäßigen </span>::OnFailSel erben. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>Vorherige Auswahl beibehalten. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>Markierung aufheben; alle Versuche, ein Material anzuwenden oder Objekte ein-/auszublenden, werden ignoriert. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>Gibt einen Fehler zurück. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p> </td> 
  <td class="stentry"> <p>Wählen Sie die Standardgruppe aus (die erste Gruppe in der Vignettenhierarchie, die renderbare Objekte enthält). </p> </td> 
 </tr> 
</table>

## Standard {#section-c25f458f9f8f4236963a95779529e664}

Von `default::OnFailSel` geerbt, wenn nicht definiert.

## Verwandte Themen {#section-f8b15dd64c674c5484d190dd9e3016af}

[sel=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sel.md#reference-01322c58d414481385c29fcdd27a090b) , [attribute::OnFailObj](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailobj.md#reference-4c6ba90418e84da5831f8573bbbf2c8d)
