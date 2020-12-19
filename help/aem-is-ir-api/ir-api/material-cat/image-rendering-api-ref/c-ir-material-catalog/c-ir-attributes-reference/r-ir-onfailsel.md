---
description: Behandlung von Auswahlfehlern auswählen Gibt die Aktion an, die ausgeführt werden soll, wenn der Befehl sel= fehlschlägt, weil die angegebene Pixelposition nicht im Maskenbereich eines auswählbaren Objekts liegt.
seo-description: Behandlung von Auswahlfehlern auswählen Gibt die Aktion an, die ausgeführt werden soll, wenn der Befehl sel= fehlschlägt, weil die angegebene Pixelposition nicht im Maskenbereich eines auswählbaren Objekts liegt.
seo-title: OnFailSel
solution: Experience Manager
title: OnFailSel
topic: Scene7 Image Serving - Image Rendering API
uuid: 073b6651-970c-460c-b044-e3ef37cc677a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 10%

---


# OnFailSel{#onfailsel}

Behandlung von Auswahlfehlern auswählen Gibt die Aktion an, die ausgeführt werden soll, wenn der Befehl sel= fehlschlägt, weil die angegebene Pixelposition nicht im Maskenbereich eines auswählbaren Objekts liegt.

## Eigenschaften {#section-cec491e6c5c744f9bfafaaa9d8774f83}

Enum.

<table id="simpletable_1CFD2BC6F9BC4D2AB372EAF115B7F2FC"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>Von <span class="codeph"> default::OnFailSel </span> übernehmen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>Bisherige Auswahl beibehalten. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>die Auswahl aufheben; Versuche, ein Material anzuwenden oder Objekte ein-/auszublenden, werden ignoriert. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>Fehler zurückgeben. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p> </td> 
  <td class="stentry"> <p>Wählen Sie die Standardgruppe aus (die erste Gruppe in der Vignettenhierarchie, die renderbare Objekte enthält). </p> </td> 
 </tr> 
</table>

## Standard {#section-c25f458f9f8f4236963a95779529e664}

Vererbt von `default::OnFailSel`, wenn nicht definiert.

## Verwandte Themen {#section-f8b15dd64c674c5484d190dd9e3016af}

[sel=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sel.md#reference-01322c58d414481385c29fcdd27a090b) ,  [attribute::OnFailObj](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailobj.md#reference-4c6ba90418e84da5831f8573bbbf2c8d)
