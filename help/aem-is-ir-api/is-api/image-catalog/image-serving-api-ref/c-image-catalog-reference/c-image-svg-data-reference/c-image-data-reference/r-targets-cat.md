---
description: Zoom der Zieldaten. Keine oder mehrere Zoom-Zieleigenschaften, die zusammen mit dem Zoom-Viewer-Client verwendet werden können.
solution: Experience Manager
title: Ziele
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b882ba01-a1ef-4179-95c7-964c2578aad1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 1%

---

# Ziele{#targets}

Zoom der Zieldaten. Keine oder mehrere Zoom-Zieleigenschaften, die zusammen mit dem Zoom-Viewer-Client verwendet werden können.

Der Server gibt den Inhalt dieses Felds als Antwort auf `req=targets` zurück, nachdem er die &#39;`??`&#39;-Record-Terminator-Token ersetzt hat.

Jedem Zoomziel können bis zu vier Eigenschaften zugeordnet werden:

` Target. *`num`*.frame= *`frame`*`

` Target. *`num`*.rect= *`left,top,width,height`*`

` Target. *`num`*.label= *`label`*`

` Target. *`num`*.userData= *`userData`*`

<table id="simpletable_4C20157A7A444DEB9959B335CAFBAEC8"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> num </span> </span> </p> </td> 
  <td class="stentry"> <p>Zoom-Zielnummer (int); Zoomziele müssen sequenziell und nacheinander nummeriert werden, beginnend bei 1. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> frame </span> </span> </p> </td> 
  <td class="stentry"> <p>Optionale Frame-/Seitennummer für die Zielgruppenbestimmung eines bestimmten Rahmens/einer bestimmten Seite eines Rotationssets oder eines Broschürensets; Standardwert ist 0, wenn nicht für die Verwendung des Rotationsset- und Broschüren-Viewers angegeben; wird vom Zoom-Viewer ignoriert. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> links, oben </span> </span> </p> </td> 
  <td class="stentry"> <p>Pixel-Versatz von oben links im Bild oben links im Zoom-Zielrechteck (int, int); muss 0 oder höher sein. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> Breite, Höhe </span> </span> </p> </td> 
  <td class="stentry"> <p>Die Pixelgröße des Zoom-Zielrechtecks (int, int) muss größer als 0 sein. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> label </span> </span> </p> </td> 
  <td class="stentry"> <p>Textdatenwert; kann als Textbeschriftung für einen Zoomziel-Link verwendet werden. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> userData </span> </span> </p> </td> 
  <td class="stentry"> <p>Textdatenwert; kann verwendet werden, um zielgruppenspezifische Informationen an den Client zu übergeben, z. B. einen SKU-Wert oder eine Hotlink-URL. </p> </td> 
 </tr> 
</table>

Target. *`num`*.rect ist für jedes Zoomziel erforderlich und muss ein Rechteck im Bild vollständig angeben. Alle anderen Eigenschaften sind optional.

*`label`* und *`userData`* nehmen an der Lokalisierung von Textzeichenfolgen teil. Weitere Informationen finden Sie unter [Lokalisierung von Textzeichenfolgen](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) in der *HTTP-Protokollreferenz*.

Bei Anwendungen, bei denen die Viewer-Clients für Rotation und Broschüre verwendet werden, müssen die Zoomziele in demselben Katalogdatensatz definiert werden, der das Bildset definiert. Alle Zoom-Zieldefinitionen in den Katalogdatensätzen der Mitglieder des Bildsets werden vom Viewer ignoriert.

Die Dynamic Media-Viewer erwarten Zoomziele in den Koordinaten des Vollbildbilds, das bereits durch die Befehle von `catalog::Modifier` angepasst wurde.

## Eigenschaften {#section-b3f8eba4985f4b00bb935d592fe770f9}

[Eigenschaftsdaten](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md) .

## Standard {#section-feab29f6575e482391086a57f547543c}

Keine.

## Verwandte Themen {#section-83dea73b1dbf4aa1b64b0aae2933e6e1}

[catalog::ImageSet](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md#reference-4764d347afd64afdaede9a74c7565256) , [catalog::Modifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834), [req=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md), [Text String Localization](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
