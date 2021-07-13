---
description: Wählen Sie das Objekt anhand des Namens aus. Wählt die angegebene Vignettengruppe nach Namen aus und startet einen neuen MSS.
solution: Experience Manager
title: obj
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 17387203-f7a7-4876-a15b-2084894f981d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 4%

---

# obj{#obj}

Wählen Sie das Objekt anhand des Namens aus. Wählt die angegebene Vignettengruppe nach Namen aus und startet einen neuen MSS.

` obj= *`name`*`

<table id="simpletable_6E0DA6CBCDCF4CDDAFA5A4C38E0D5FC5"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> name  </span> </span> </p> </td> 
  <td class="stentry"> <p>Gruppenname oder Pfad/Name. </p> </td> 
 </tr> 
</table>

Untergruppen oder einzelne Objekte können über einen vollständig qualifizierten Gruppenpfad ausgewählt werden (d. h. durch Angabe des Namens der Zielgruppe oder des Objekts, dem alle übergeordneten Gruppen vorangestellt sind, getrennt durch / (Schrägstriche).

Wenn keine Gruppe/kein Objekt mit dem angegebenen Namen gefunden wird, wird die in `attribute::OnObjFail` angegebene Aktion ausgeführt.

## Eigenschaften {#section-9463b36e8ff74c81a70c7c2b58927430}

Auswahlbefehl; MSS-Trennzeichen. Die Objektauswahl ist so lange persistent, bis ein anderes Objekt ausgewählt ist, entweder mit `obj=` oder `sel=`.

Bei Gruppen-/Objektpfaden und -namen wird nicht zwischen Groß- und Kleinschreibung unterschieden.

## Standard {#section-0c322850512c4896bb551856a549440e}

Die erste Gruppe in der Vignette mit renderbaren Objekten wird automatisch ausgewählt, wenn eine neue Vignette geöffnet wird.

## Verwandte Themen {#section-d9d2c92ef48548f48b9781e2a8a5fb5a}

[sel=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sel.md#reference-01322c58d414481385c29fcdd27a090b),  [attribute::OnFailObj](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailobj.md#reference-4c6ba90418e84da5831f8573bbbf2c8d)
