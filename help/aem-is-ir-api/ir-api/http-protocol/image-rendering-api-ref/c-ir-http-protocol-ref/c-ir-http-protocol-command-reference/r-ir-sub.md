---
description: Unterauswahl. Ermöglicht das Anwenden unterschiedlicher Materialien auf verschiedene Bereiche des ausgewählten Objekts oder der ausgewählten Gruppe sowie das Entfernen zuvor angewendeter Materialien.
seo-description: Unterauswahl. Ermöglicht das Anwenden unterschiedlicher Materialien auf verschiedene Bereiche des ausgewählten Objekts oder der ausgewählten Gruppe sowie das Entfernen zuvor angewendeter Materialien.
seo-title: sub
solution: Experience Manager
title: sub
topic: Scene7 Image Serving - Image Rendering API
uuid: cb9f4dc5-9d89-483a-ae72-b9076b27c57e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 6%

---


# sub{#sub}

Unterauswahl. Ermöglicht das Anwenden unterschiedlicher Materialien auf verschiedene Bereiche des ausgewählten Objekts oder der ausgewählten Gruppe sowie das Entfernen zuvor angewendeter Materialien.

`sub=0|1|2|3|4|5`

<table id="simpletable_F6BF91BD2C4B47BF8A28032E392D37F0"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>Wählen Sie die gesamte Wand aus. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>Wählen Sie die obere Hälfte der Wand aus. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>Wählen Sie die untere Hälfte der Wand aus. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>Wählen Sie den oberen Rand aus. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p> </td> 
  <td class="stentry"> <p>Wählen Sie den mittleren Wandbegrenzungsbereich aus. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>5 </p> </td> 
  <td class="stentry"> <p>Wählen Sie den Randbereich der unteren Wand aus. </p> </td> 
 </tr> 
</table>

Derzeit nur für Wandobjekte unterstützt. Hiermit wird ein vorhergehendes MSS beendet und ein neuer MSS-Dienst für das Material, das auf die angegebene Unterauswahl angewendet werden soll, Beginn.

Ein für die obere oder untere Wand definiertes Material wird auf die gesamte Wand angewendet, es sei denn, es wurde auch ein anderes Material für die andere Hälfte der Wand angegeben.

## Eigenschaften {#section-b202139d6d0847cc8d520a154104ab9d}

Auswahlbefehl; MSS-Trennzeichen.

## Standard {#section-5b45a167a17c451596e4c59b7d53c368}

`sub=0`

## Verwandte Themen {#section-1a993ee24f144d4fb8baef0cc431b53b}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a)
