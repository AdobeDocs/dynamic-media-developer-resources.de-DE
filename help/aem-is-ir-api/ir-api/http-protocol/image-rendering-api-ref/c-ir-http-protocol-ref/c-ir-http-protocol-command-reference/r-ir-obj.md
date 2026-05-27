---
title: obj
description: Objekt nach Namen auswählen. Wählt die angegebene Vignettengruppe nach Namen aus und startet eine neue SMS.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 17387203-f7a7-4876-a15b-2084894f981d
TQID: 'https://experienceleague.adobe.com/te9iyNajxDfgvHqqThbVUc7tBItxfMtxhOMl2eCLOsk'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 141
ht-degree: 3%

---

# obj{#obj}

Objekt nach Namen auswählen. Wählt die angegebene Vignettengruppe nach Namen aus und startet eine neue SMS.

` obj= *`name`*`

<table id="simpletable_6E0DA6CBCDCF4CDDAFA5A4C38E0D5FC5"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> Name </span> </span> </p> </td> 
  <td class="stentry"> <p>Gruppenname oder Pfad/Name. </p> </td> 
 </tr> 
</table>

Untergruppen oder einzelne Objekte können mithilfe eines vollqualifizierten Gruppenpfads ausgewählt werden (d. h. durch Angabe des Namens der Zielgruppe oder des Objekts mit vorangestellter Angabe aller übergeordneten Gruppen, getrennt durch / (Schrägstriche).

Wenn keine Gruppe/kein Objekt mit dem angegebenen Namen gefunden wird, wird die in `attribute::OnObjFail` angegebene Aktion ausgeführt.

## Eigenschaften {#section-9463b36e8ff74c81a70c7c2b58927430}

Auswahlbefehl; MS-Trennzeichen. Die Objektauswahl bleibt so lange bestehen, bis ein anderes Objekt ausgewählt wird, entweder mit `obj=` oder `sel=`.

Bei Gruppen-/Objektpfaden und Namen wird nicht zwischen Groß- und Kleinschreibung unterschieden.

## Standard {#section-0c322850512c4896bb551856a549440e}

Die erste Gruppe in der Vignette, die renderbare Objekte enthält, wird automatisch ausgewählt, wenn eine neue Vignette geöffnet wird.

## Verwandte Themen {#section-d9d2c92ef48548f48b9781e2a8a5fb5a}

[sel=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sel.md#reference-01322c58d414481385c29fcdd27a090b), [attribute::OnFailObj](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailobj.md#reference-4c6ba90418e84da5831f8573bbbf2c8d)
