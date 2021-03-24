---
description: Anwenden von Flags Gibt weitere Renderoptionen an.
solution: Experience Manager
title: kennzeichnen
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '78'
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
