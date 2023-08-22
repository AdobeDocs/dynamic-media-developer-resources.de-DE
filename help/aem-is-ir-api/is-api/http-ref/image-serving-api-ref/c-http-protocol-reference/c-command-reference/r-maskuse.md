---
title: maskUse
description: Verwendung der Bildmaske. Gibt an, wie die Maske oder der Alphakanal des Bildes für Vorgänge im Bild verwendet wird (z. B. colorize=). Wenn in einer Effektebene angegeben, kann der Effekt auf den Hintergrundbereich der übergeordneten Ebene oder auf das gesamte Rechteck der übergeordneten Ebene angewendet werden.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e99101a1-1747-454c-b0c0-3af3335c0497
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 2%

---

# maskUse{#maskuse}

Verwendung der Bildmaske. Gibt an, wie die Maske oder der Alphakanal des Bildes für Vorgänge im Bild verwendet wird (z. B. colorize=). Wenn in einer Effektebene angegeben, kann der Effekt auf den Hintergrundbereich der übergeordneten Ebene oder auf das gesamte Rechteck der übergeordneten Ebene angewendet werden.

`maskUse=norm|invert|off`

Die folgende Tabelle zeigt die Auswirkungen von `maskUse=` je nach Verfügbarkeit und Typ der Maske (Alphakanal), die mit dem Ebenenbild verknüpft ist.

<table id="table_B765F6A765F548948531AF26DA0B4360"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Wert</b> </th> 
   <th class="entry"> <b> Keine Maske</b> </th> 
   <th class="entry"> <b> Nicht zugeordnetes Alpha (oder separates Maskenbild)</b> </th> 
   <th class="entry"> <b> Assoziiertes Alpha (vormultipliziert)</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> aus </span> </p> </td> 
   <td> <p> Rechteck für undurchsichtige Bilder </p> </td> 
   <td> <p> Rechteck für undurchsichtige Bilder </p> </td> 
   <td> <p> Vordergrundbereich des Bildes über einem Rechteck, gefüllt mit schwarz </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> norm </span> </p> </td> 
   <td> <p> Rechteck für undurchsichtige Bilder </p> </td> 
   <td> <p> Vordergrundbereich des Bildes </p> </td> 
   <td> <p> Vordergrundbereich des Bildes oder der Ebene </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> invert </span> </p> </td> 
   <td> <p> Ausgeblendete Ebene </p> </td> 
   <td> <p> Hintergrundbereich des Bildes </p> </td> 
   <td> <p> Hintergrundbereich des Bildes oder der Ebene mit schwarzem Vollbild </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-f36ad1af348e45aeb3eb336544df30b0}

Bild- oder Ebenenattribut. Gilt für Ebene 0, wenn `layer=comp`. Wenn in einer Effektebene angegeben, ändert der Befehl die von der übergeordneten Ebene übernommene Maske.

Das Verhalten `maskUse=` ist nicht definiert und wird nicht unterstützt, wenn sie mit Text oder einfarbigen Ebenen angegeben wird, wenn keine Bildmaske anwendbar ist (angegeben mit `mask=` oder `catalog::Mask`).

## Standard {#section-982dd8174641437786dcb3729ace6428}

`maskUse=norm`

## Beispiel {#section-daa371e9be5547368ff6772342acba0a}

Den Hintergrundbereich eines Bildes färben; der BildVordergrund wird durch ein eigenes Maskenbild definiert. Dies wird erreicht, indem der farbige Bildhintergrund auf der Oberseite platziert wird, wenn das unveränderte Bild:

`http://server/myRootId/myImageId?layer=1&src=myImageId&mask=myImgMask&maskUse=invert&colorize=0x306090`

## Verwandte Themen {#section-f239d8f4ce70434f8d30e482ed60ee5e}

[color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) , [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)
