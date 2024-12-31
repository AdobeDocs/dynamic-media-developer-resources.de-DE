---
title: Maskenverwendung
description: Verwendung der Bildmaske. Gibt an, wie die Maske oder der Alphakanal des Bildes für Vorgänge auf dem Bild verwendet wird (z. B. colorize=). Wenn in einer Effektebene festgelegt, kann der Effekt auf den Hintergrundbereich der übergeordneten Ebene oder auf das gesamte übergeordnete Ebenenrechteck angewendet werden.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e99101a1-1747-454c-b0c0-3af3335c0497
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 1%

---

# Maskenverwendung{#maskuse}

Verwendung der Bildmaske. Gibt an, wie die Maske oder der Alphakanal des Bildes für Vorgänge auf dem Bild verwendet wird (z. B. colorize=). Wenn in einer Effektebene festgelegt, kann der Effekt auf den Hintergrundbereich der übergeordneten Ebene oder auf das gesamte übergeordnete Ebenenrechteck angewendet werden.

`maskUse=norm|invert|off`

Die folgende Tabelle zeigt die Wirkung von `maskUse=` in Abhängigkeit von Verfügbarkeit und Typ der Maske (Alphakanal), die mit dem Ebenenbild verknüpft ist.

<table id="table_B765F6A765F548948531AF26DA0B4360"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Wert</b> </th> 
   <th class="entry"> <b> keine Maske</b> </th> 
   <th class="entry"> <b> Nicht verknüpfte Alpha (oder separates Maskenbild)</b> </th> 
   <th class="entry"> <b> zugeordnete (vormultiplizierte) Alpha</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> von </span> </p> </td> 
   <td> <p> Undurchsichtiges Bildrechteck </p> </td> 
   <td> <p> Undurchsichtiges Bildrechteck </p> </td> 
   <td> <p> Vordergrundbereich des Bildes über einem Rechteck, das mit durchgehendem Schwarz gefüllt ist </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">-</span> </p> </td> 
   <td> <p> Undurchsichtiges Bildrechteck </p> </td> 
   <td> <p> Vordergrundbildbereich </p> </td> 
   <td> <p> Vordergrundbereich eines Bildes oder einer Ebene </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> invertieren </span> </p> </td> 
   <td> <p> Ausgeblendete Ebene </p> </td> 
   <td> <p> Hintergrundbild </p> </td> 
   <td> <p> Hintergrundbereich eines Bildes oder einer Ebene mit Volltonschwarz gefüllt </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-f36ad1af348e45aeb3eb336544df30b0}

Bild- oder Ebenenattribut. Gilt für Ebene 0, falls `layer=comp`. Wenn in einer Effektebene angegeben, ändert der Befehl die Maske, die von der übergeordneten Ebene übernommen wird.

Das Verhalten von `maskUse=` ist nicht definiert und wird nicht unterstützt, wenn es mit Text- oder Vollfarbschichten angegeben wird und keine Bildmaske anwendbar ist (angegeben mit `mask=` oder `catalog::Mask`).

## Standard {#section-982dd8174641437786dcb3729ace6428}

`maskUse=norm`

## Beispiel {#section-daa371e9be5547368ff6772342acba0a}

Den Hintergrundbereich eines Bildes einfärben; der Bildvordergrund wird durch ein separates Maskenbild definiert. Dies wird erreicht, indem der farbige Bildhintergrund über das unveränderte Bild geschichtet wird:

`http://server/myRootId/myImageId?layer=1&src=myImageId&mask=myImgMask&maskUse=invert&colorize=0x306090`

## Verwandte Themen {#section-f239d8f4ce70434f8d30e482ed60ee5e}

[color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) , [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)
