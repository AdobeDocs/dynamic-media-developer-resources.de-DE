---
description: Anwenden von Flags Gibt weitere Renderoptionen an.
seo-description: Anwenden von Flags Gibt weitere Renderoptionen an.
seo-title: kennzeichnen
solution: Experience Manager
title: kennzeichnen
uuid: 43ed24fe-461e-4973-aa44-8fba66668e6f
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 5%

---


# kennzeichnen{#flags}

Anwenden von Flags Gibt weitere Renderoptionen an.

`flags= *`val`*`

<table id="simpletable_00B21BD9E47E4D2FB0042CB507431916"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Kennzeichnungswert. </p></td> 
 </tr> 
</table>

Wird derzeit nur für Möbelstücke verwendet.

`flags=0` (Standard) Rendert Oberschränke mit durchgehenden Türen.

`flags=1` Rendert Oberschränke mit Glastüren (wenn die Vignette mit Glastüren verfasst wurde).

## Eigenschaften {#section-a2b00d7bb15e449ea85178acb92d8285}

Materialattribut. Wird ignoriert, wenn nicht ein Schrankmaterial, oder wenn die Zielgruppe Schrank Objekt nicht erlaubt Glastüren.

## Standard {#section-4c134b02a1da4ffb9841233f98f6e97c}

`flags=0` für keine Glastüren.
