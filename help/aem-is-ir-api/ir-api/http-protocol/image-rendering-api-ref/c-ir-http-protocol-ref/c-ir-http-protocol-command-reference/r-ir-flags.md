---
title: kennzeichnen
description: Anwenden von Flags. Gibt zusätzliche Render-Optionen an.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d0c3f65e-2dec-4c35-8df4-8d111e81f3f0
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 4%

---

# kennzeichnen {#flags}

Anwenden von Flags. Gibt zusätzliche Render-Optionen an.

`flags= *`val`*`

<table id="simpletable_00B21BD9E47E4D2FB0042CB507431916"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Val</span> </p> </td> 
  <td class="stentry"> <p>Markierungswert. </p></td> 
 </tr> 
</table>

Wird derzeit nur für Schrankmaterialien verwendet.

`flags=0` (Standard) Rendert obere Schränke mit geschlossenen Türen.

`flags=1` Rendert Oberschränke mit Glastüren (wenn die Vignette mit Glastüren erstellt wurde).

## Eigenschaften {#section-a2b00d7bb15e449ea85178acb92d8285}

Materialattribut. Ignoriert, wenn kein Schrankmaterial vorhanden ist oder wenn das Zielobjekt keine Glastüren zulässt.

## Standard {#section-4c134b02a1da4ffb9841233f98f6e97c}

`flags=0` Für keine Glastüren.
