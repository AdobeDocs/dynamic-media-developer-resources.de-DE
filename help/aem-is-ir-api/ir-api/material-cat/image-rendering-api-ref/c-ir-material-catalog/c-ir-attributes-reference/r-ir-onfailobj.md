---
description: Umgang mit Fehlern bei der Objektauswahl. Gibt die Aktion an, die ausgeführt werden soll, wenn der Befehl obj= fehlschlägt, da der angegebene Pfad in der Vignettenobjekthierarchie nicht übereinstimmt.
solution: Experience Manager
title: OnFailObj
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0ed04daf-1797-4c12-ae6d-a9a008de9d1d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 13%

---

# OnFailObj{#onfailobj}

Umgang mit Fehlern bei der Objektauswahl. Gibt die Aktion an, die ausgeführt werden soll, wenn der Befehl obj= fehlschlägt, da der angegebene Pfad in der Vignettenobjekthierarchie nicht übereinstimmt.

## Eigenschaften {#section-2c779d9c133a443d9f0aed9fde7b703c}

Enum.

<table id="simpletable_538B76AB784D4DEE9B8021A6BDCE06AB"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>Vererben Sie von <span class="codeph"> default::OnFailObj </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>Bisherige Auswahl beibehalten. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>Auswahl aufheben; Alle Versuche, ein Material anzuwenden oder Objekte ein-/auszublenden, werden ignoriert. </p> </td> 
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

## Standard {#section-a5a95a2b4a204a4eae350e5b544d1513}

Vererbt von `default::OnFailObj` , falls nicht definiert.

## Verwandte Themen {#section-806dc2c5973c41f683af085b3315043c}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a) ,  [attribute::OnFailSel](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailsel.md#reference-f95e4a4a3c02412b87a2b0acca8a5513)
