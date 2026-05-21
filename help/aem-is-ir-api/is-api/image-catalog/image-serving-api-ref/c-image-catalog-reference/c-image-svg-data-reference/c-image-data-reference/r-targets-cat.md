---
description: Zoom-Zieldaten. Keine oder mehrere Zoom-Zieleigenschaften, die in Verbindung mit dem Zoom-Viewer-Client verwendet werden können.
solution: Experience Manager
title: Zielgruppen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b882ba01-a1ef-4179-95c7-964c2578aad1
TQID: 'https://experienceleague.adobe.com/kP22kltIPZqErqxNKpYp2eNkII-GdYQQeiVH3wEYOvM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: null
workflow-type: tm+mt
source-wordcount: 331
ht-degree: 1%

---

# Zielgruppen{#targets}

Zoom-Zieldaten. Keine oder mehrere Zoom-Zieleigenschaften, die in Verbindung mit dem Zoom-Viewer-Client verwendet werden können.

Der Server gibt den Inhalt dieses Felds als Antwort auf `req=targets` zurück, nachdem er die Datensatzabschlusstoken &#39; `??`&#39; ersetzt hat.

Jedem Zoom-Ziel können bis zu vier Eigenschaften zugeordnet werden:

` Target. *`num`*.frame= *`frame`*`

` Target. *`num`*.rect= *`left,top,width,height`*`

` Target. *`num`*.label= *`label`*`

` Target. *`num`*.userData= *`userData`*`

<table id="simpletable_4C20157A7A444DEB9959B335CAFBAEC8"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> num </span> </span> </p> </td> 
  <td class="stentry"> <p>Zoom-Zielnummer (int); Zoom-Ziele müssen sequenziell und fortlaufend nummeriert werden, beginnend mit 1. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> Frame </span> </span> </p> </td> 
  <td class="stentry"> <p>Optionale Frame-/Seitennummer für die Auswahl eines bestimmten Frames/einer bestimmten Seite eines Rotations- oder Broschürensets; Standardwert ist 0, wenn für Rotation und die Verwendung als Broschüren-Viewer nicht angegeben; vom Zoom-Viewer ignoriert. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> links, oben </span> </span> </p> </td> 
  <td class="stentry"> <p>Pixel-Versatz von oben links im Bild oben links neben dem Rechteck des Zoom-Ziels (int, int); muss 0 oder höher sein. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> Breite, Höhe </span> </span> </p> </td> 
  <td class="stentry"> <p>Pixelgröße des Rechtecks des Zoomziels (int, int); muss größer als 0 sein. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> Bezeichnung </span> </span> </p> </td> 
  <td class="stentry"> <p>Textdatenwert; kann als Textbeschriftung für einen Zoom-Ziel-Link verwendet werden. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> userData </span> </span> </p> </td> 
  <td class="stentry"> <p>Textdatenwert; kann verwendet werden, um zielgruppenspezifische Informationen an den Client zu übergeben, z. B. einen SKU-Wert oder eine Hotlink-URL. </p> </td> 
 </tr> 
</table>

Zielgruppe. *`num`*.rect ist für jedes Zoomziel erforderlich und muss ein Rechteck vollständig im Bild angeben. Alle anderen Eigenschaften sind optional.

*`label`* und *`userData`* sind an der Lokalisierung von Textzeichenfolgen beteiligt. Siehe [Lokalisierung von Textzeichenfolgen](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) in der *HTTP-Protokollreferenz* für Details.

Bei Anwendungen, die die Clients zum Anzeigen von Rotationen und Broschüren beinhalten, müssen die Zoom-Ziele im selben Katalogdatensatz definiert werden, der das Bildset definiert. Alle Zoom-Zieldefinitionen in den Katalogdatensätzen der Mitglieder des Bildsets werden vom Viewer ignoriert.

Die Dynamic Media-Viewer erwarten Zoom-Ziele in den Koordinaten des Bildes mit voller Auflösung, die bereits durch die Befehle von `catalog::Modifier` angepasst wurden.

## Eigenschaften {#section-b3f8eba4985f4b00bb935d592fe770f9}

[Eigenschaftsdaten](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md) Wert.

## Standard {#section-feab29f6575e482391086a57f547543c}

Keine.

## Verwandte Themen {#section-83dea73b1dbf4aa1b64b0aae2933e6e1}

[catalog::ImageSet](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md#reference-4764d347afd64afdaede9a74c7565256) , [catalog::](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834)Modifier[, req=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md), [Text-Zeichenfolgenlokalisierung](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
