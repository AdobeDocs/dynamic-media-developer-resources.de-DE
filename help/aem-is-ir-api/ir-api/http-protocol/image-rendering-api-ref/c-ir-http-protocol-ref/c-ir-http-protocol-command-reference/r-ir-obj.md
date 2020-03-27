---
description: Wählen Sie das Objekt anhand des Namens aus. Wählt die angegebene Vignettengruppe anhand des Namens aus und Beginn ein neues MSS.
seo-description: Wählen Sie das Objekt anhand des Namens aus. Wählt die angegebene Vignettengruppe anhand des Namens aus und Beginn ein neues MSS.
seo-title: obj
solution: Experience Manager
title: obj
topic: Scene7 Image Serving - Image Rendering API
uuid: 2fede992-6759-45bd-b2f1-36e2c791d536
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# obj{#obj}

Wählen Sie das Objekt anhand des Namens aus. Wählt die angegebene Vignettengruppe anhand des Namens aus und Beginn ein neues MSS.

` obj= *`name`*`

<table id="simpletable_6E0DA6CBCDCF4CDDAFA5A4C38E0D5FC5"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> Name </span></span> </p> </td> 
  <td class="stentry"> <p>Gruppenname oder Pfad/Name. </p> </td> 
 </tr> 
</table>

Untergruppen oder einzelne Objekte können mithilfe eines vollständig qualifizierten Gruppenpfads ausgewählt werden (d. h. durch Angabe des Namens der Zielpopulation oder des Objekts, dem alle übergeordneten Gruppen vorangestellt sind, getrennt durch / (Schrägstriche).

Wenn keine Gruppe/kein Objekt mit dem angegebenen Namen gefunden wird, wird die in angegebene Aktion `attribute::OnObjFail` ausgeführt.

## Eigenschaften {#section-9463b36e8ff74c81a70c7c2b58927430}

Auswahlbefehl; MSS-Trennzeichen. Die Objektauswahl bleibt bestehen, bis ein anderes Objekt ausgewählt ist, entweder mit `obj=` oder `sel=`.

Bei Gruppen-/Objektpfaden und -namen wird nicht zwischen Groß- und Kleinschreibung unterschieden.

## Standard {#section-0c322850512c4896bb551856a549440e}

Die erste Gruppe in der Vignette mit renderbaren Objekten wird automatisch ausgewählt, wenn eine neue Vignette geöffnet wird.

## Verwandte Themen {#section-d9d2c92ef48548f48b9781e2a8a5fb5a}

[sel=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sel.md#reference-01322c58d414481385c29fcdd27a090b), [attribute::OnFailObj](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailobj.md#reference-4c6ba90418e84da5831f8573bbbf2c8d)
