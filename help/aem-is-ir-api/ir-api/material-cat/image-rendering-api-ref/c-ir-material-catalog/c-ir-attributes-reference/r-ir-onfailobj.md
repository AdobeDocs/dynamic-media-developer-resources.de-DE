---
title: OnFailObj
description: Fehlerbehandlung bei der Objektauswahl. Gibt die Aktion an, die ausgeführt werden soll, wenn der Befehl obj= fehlschlägt, da der angegebene Pfad in der Vignettenobjekthierarchie nicht abgeglichen werden kann.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0ed04daf-1797-4c12-ae6d-a9a008de9d1d
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 7%

---

# OnFailObj{#onfailobj}

Fehlerbehandlung bei der Objektauswahl. Gibt die Aktion an, die ausgeführt werden soll, wenn der Befehl obj= fehlschlägt, da der angegebene Pfad in der Vignettenobjekthierarchie nicht abgeglichen werden kann.

## Eigenschaften {#section-2c779d9c133a443d9f0aed9fde7b703c}

Aufzählung.

<table id="simpletable_538B76AB784D4DEE9B8021A6BDCE06AB"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>Von <span class="codeph"> standardmäßigen </span>::OnFailObj erben. </p> </td> 
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

## Standard {#section-a5a95a2b4a204a4eae350e5b544d1513}

Von `default::OnFailObj` geerbt, wenn nicht definiert.

## Verwandte Themen {#section-806dc2c5973c41f683af085b3315043c}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a) , [attribute::OnFailSel](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailsel.md#reference-f95e4a4a3c02412b87a2b0acca8a5513)
