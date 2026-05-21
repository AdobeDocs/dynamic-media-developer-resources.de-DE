---
title: textFlowXPath
description: Textfluss-Ausschlussbereich. Gibt mindestens eine vom Textfluss auszuschließende Region an.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2430ab43-c032-4c2f-93c3-225e8116f100
TQID: 'https://experienceleague.adobe.com/hNtdD3lH2laX-X-1PXoeAZegB0Ly9c7-bn7gdinQxwg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 76
ht-degree: 5%

---

# textFlowXPath{#textflowxpath}

Textfluss-Ausschlussbereich. Gibt mindestens eine vom Textfluss auszuschließende Region an.

`textFlowXPath= *`pathDefinition`*`

<table id="simpletable_7E0EA48AEBB5426CBE948FCA18882C66"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> pathDefinition</span> </p> </td> 
  <td class="stentry"> <p>Pfaddaten. </p></td> 
 </tr> 
</table>

Siehe [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) für weitere Informationen, einschließlich einer Beschreibung der *`pathDefinition`*. Wenn keine Pfaddefinition angegeben ist, wird `textFlowXPath=` ignoriert.

## Eigenschaften {#section-cd1ebb151d4a405fbfc508d46522d686}

Attribut der Textebene (nur `textPs=`). Von anderen Ebenen ignoriert oder ohne `textFlowPath=` angegeben. Gilt für `layer=0`, wenn für `layer=comp` angegeben.

## Standard {#section-9405cda904684d829ed12a9e40a4dc46}

Keine.

## Verwandte Themen {#section-855228e744c7437a921d5db5b24bcd95}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) , [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d), [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef)
