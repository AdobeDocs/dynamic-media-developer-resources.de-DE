---
description: Daten zur Zoom-Zielgruppe. Keine oder mehr Zoom-Zielgruppe-Eigenschaften, die zusammen mit dem Zoom-Viewer-Client verwendet werden können.
seo-description: Daten zur Zoom-Zielgruppe. Keine oder mehr Zoom-Zielgruppe-Eigenschaften, die zusammen mit dem Zoom-Viewer-Client verwendet werden können.
seo-title: Ziele
solution: Experience Manager
title: Ziele
topic: Scene7 Image Serving - Image Rendering API
uuid: ca02483a-9aa0-4b54-b6f0-4fd10d8b2b4c
translation-type: tm+mt
source-git-commit: b4331c6f033903ec64f168da0b739927c6066710

---


# Ziele{#targets}

Daten zur Zoom-Zielgruppe. Keine oder mehr Zoom-Zielgruppe-Eigenschaften, die zusammen mit dem Zoom-Viewer-Client verwendet werden können.

Der Server gibt den Inhalt dieses Felds als Antwort auf `req=targets`das Ersetzen der Token für die `??`Datensatzsperre zurück.

Mit jeder Zoom-Zielgruppe können bis zu vier Eigenschaften verknüpft werden:

` Target. *``*.frame= *`numerframe`*`

` Target. *``*.rect= *`Numleft, top, width, height`*`

` Target. *``*.label= *`numlabel`*`

` Target. *``*.userData= *`numuserData`*`

<table id="simpletable_4C20157A7A444DEB9959B335CAFBAEC8"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> num </span></span> </p> </td> 
  <td class="stentry"> <p>Zoom-Zielgruppe (int); Zoom-Zielgruppen müssen fortlaufend nummeriert werden, beginnend mit 1. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> Rahmen </span></span> </p> </td> 
  <td class="stentry"> <p>Optionaler Rahmen/Seitennummer für das Targeting eines bestimmten Rahmens/einer bestimmten Seite eines Rotationssets oder eines Prospektsatzes; ist standardmäßig auf 0 gesetzt, wenn für die Verwendung des Rotationsset- und Prospektanzeigers keine Angabe gemacht wurde; vom Zoom-Viewer ignoriert. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> links, oben </span></span> </p> </td> 
  <td class="stentry"> <p>Pixel-Versatz von oben links im Bild nach links oben im Rechteck für die Zoom-Zielgruppe (int, int); muss 0 oder größer sein. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> Breite, Höhe </span></span> </p> </td> 
  <td class="stentry"> <p>Pixelgröße des Rechtecks für die Zoom-Zielgruppe (int, int); muss größer als 0 sein. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> label </span></span> </p> </td> 
  <td class="stentry"> <p>Textdatenwert; kann als Textbeschriftung für einen Link zur Zoom-Zielgruppe verwendet werden. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> userData </span></span> </p> </td> 
  <td class="stentry"> <p>Textdatenwert; kann verwendet werden, um Zielgruppe-spezifische Informationen an den Client weiterzugeben, z. B. einen SKU-Wert oder eine Hotlink-URL. </p> </td> 
 </tr> 
</table>

Ziel. *`num`*.rect ist für jede Zoom-Zielgruppe erforderlich und muss ein Rechteck vollständig im Bild angeben. Alle anderen Eigenschaften sind optional.

*`label`* und *`userData`* nehmen Sie an der lokale Anpassung der Textzeichenfolge teil. Weitere Informationen finden Sie in der [Textzeichenfolgen-Lokale Anpassung](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) in der *HTTP-Protokollreferenz* .

Bei Anwendungen, die die Rotationsset- und Prospekt-Viewer-Clients einbeziehen, müssen die Zoom-Zielgruppen in demselben Katalogdatensatz definiert werden, der den Bildsatz definiert. Alle Zoomdefinitionen in den Katalogdatensätzen der Bildsätze werden vom Viewer ignoriert.

Die Scene7-Viewer erwarten Zoom-Zielgruppen in den Koordinaten des Bildes mit voller Auflösung, die bereits durch die Befehle von `catalog::Modifier`festgelegt wurden.

## Eigenschaften {#section-b3f8eba4985f4b00bb935d592fe770f9}

[Eigenschaftsdatenwert](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md) .

## Standard {#section-feab29f6575e482391086a57f547543c}

Keine.

## Verwandte Themen {#section-83dea73b1dbf4aa1b64b0aae2933e6e1}

[catalog::ImageSet](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md#reference-4764d347afd64afdaede9a74c7565256) , [catalog::Modifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834), [req=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md), [Textzeichenfolgen-Lokale Anpassung](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
