---
description: Verwendung der Bildmaske. Gibt an, wie der Kanal "Maske"oder "Alpha"für Bildoperationen verwendet wird (z. B. "colorize="). Wenn in einer Effektebene angegeben, kann der Effekt auf den Hintergrundbereich der übergeordneten Ebene oder auf das gesamte Rechteck der übergeordneten Ebene angewendet werden.
seo-description: Verwendung der Bildmaske. Gibt an, wie der Kanal "Maske"oder "Alpha"für Bildoperationen verwendet wird (z. B. "colorize="). Wenn in einer Effektebene angegeben, kann der Effekt auf den Hintergrundbereich der übergeordneten Ebene oder auf das gesamte Rechteck der übergeordneten Ebene angewendet werden.
seo-title: maskUse
solution: Experience Manager
title: maskUse
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 2c70da87-f869-495a-be50-226a4516e002
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 2%

---


# maskUse{#maskuse}

Verwendung der Bildmaske. Gibt an, wie der Kanal &quot;Maske&quot;oder &quot;Alpha&quot;für Bildoperationen verwendet wird (z. B. &quot;colorize=&quot;). Wenn in einer Effektebene angegeben, kann der Effekt auf den Hintergrundbereich der übergeordneten Ebene oder auf das gesamte Rechteck der übergeordneten Ebene angewendet werden.

`maskUse=norm|invert|off`

Die folgende Tabelle zeigt den Effekt von `maskUse=` in Abhängigkeit von Verfügbarkeit und Typ der Maske (Alpha-Kanal), die mit dem Ebenenbild verknüpft ist.

<table id="table_B765F6A765F548948531AF26DA0B4360"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Wert</b> </th> 
   <th class="entry"> <b> Keine Maske</b> </th> 
   <th class="entry"> <b> Nicht verknüpftes Alpha (oder separates Maskenbild)</b> </th> 
   <th class="entry"> <b> Assoziierte (vormultiplizierte) Alpha</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> aus </span> </p> </td> 
   <td> <p> Rechteck eines undurchsichtigen Bilds </p> </td> 
   <td> <p> Rechteck eines undurchsichtigen Bilds </p> </td> 
   <td> <p> Vordergrundbereich des Bildes über Rechteck, gefüllt mit schwarzem </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> norm  </span> </p> </td> 
   <td> <p> Rechteck eines undurchsichtigen Bilds </p> </td> 
   <td> <p> Vordergrundbereich des Bildes </p> </td> 
   <td> <p> Vordergrundbereich des Bilds oder der Ebene </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> invert  </span> </p> </td> 
   <td> <p> Ausgeblendete Ebene </p> </td> 
   <td> <p> Hintergrundbereich des Bildes </p> </td> 
   <td> <p> Hintergrundbereich des Bilds oder der Ebene mit schwarzem Hintergrund </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-f36ad1af348e45aeb3eb336544df30b0}

Bild- oder Ebenenattribut. Gilt für Ebene 0, wenn `layer=comp`. Wenn in einer Effektebene angegeben, ändert der Befehl die Maske, die von der übergeordneten Ebene übernommen wurde.

Das Verhalten von `maskUse=` ist nicht definiert und wird nicht unterstützt, wenn es mit Text- oder Vollfarbebenen angegeben wird, wenn keine Bildmaske angewendet wird (angegeben mit `mask=` oder `catalog::Mask`).

## Standard {#section-982dd8174641437786dcb3729ace6428}

`maskUse=norm`

## Beispiel {#section-daa371e9be5547368ff6772342acba0a}

den Hintergrundbereich eines Bilds färben; Der Vordergrund des Bilds wird durch ein separates Maskenbild definiert. Dies wird erreicht, indem der farbige Bildhintergrund auf der Oberseite angeordnet wird, wenn das nicht geänderte Bild:

`http://server/myRootId/myImageId?layer=1&src=myImageId&mask=myImgMask&maskUse=invert&colorize=0x306090`

## Verwandte Themen {#section-f239d8f4ce70434f8d30e482ed60ee5e}

[color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) ,  [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)
