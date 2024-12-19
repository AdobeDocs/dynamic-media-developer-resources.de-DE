---
title: Untergruppe
description: Unterauswahl. Ermöglicht das Aufbringen verschiedener Materialien auf verschiedene Bereiche des ausgewählten Objekts oder der Gruppe und das Entfernen zuvor angewendeter Materialien.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c9968fbb-c38b-4180-81be-19992fa8f347
source-git-commit: 67e12fae514341137e4218ea950f34da0d9997f3
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 6%

---

# Untergruppe{#sub}

Unterauswahl. Ermöglicht das Aufbringen verschiedener Materialien auf verschiedene Bereiche des ausgewählten Objekts oder der Gruppe und das Entfernen zuvor angewendeter Materialien.

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
  <td class="stentry"> <p>Wählen Sie den oberen Wandrahmenbereich aus. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p> </td> 
  <td class="stentry"> <p>Wählen Sie den Randbereich der mittleren Wand aus. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>5 </p> </td> 
  <td class="stentry"> <p>Wählen Sie den unteren Wandrahmenbereich aus. </p> </td> 
 </tr> 
</table>

Wird derzeit nur für Wandobjekte unterstützt. Beendet eine vorherige MS und startet eine neue MS für das Material, das auf die angegebene Unterauswahl angewendet werden soll.

Ein für die obere oder untere Wand festgelegtes Material gilt für die gesamte Wand, es sei denn, es wurde auch ein anderes Material für die andere Hälfte der Wand festgelegt.

## Eigenschaften {#section-b202139d6d0847cc8d520a154104ab9d}

Auswahlbefehl; MS-Trennzeichen.

## Standard {#section-5b45a167a17c451596e4c59b7d53c368}

`sub=0`

## Verwandte Themen {#section-1a993ee24f144d4fb8baef0cc431b53b}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a)
