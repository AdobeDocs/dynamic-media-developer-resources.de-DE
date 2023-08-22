---
title: scale
description: Bild skalieren. Skaliert ein Ebenenquellenbild nach Faktor im Verhältnis zum Bild mit voller Auflösung.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c2cd37de-f81e-4b08-9a3e-ff05a72c363c
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 4%

---

# scale{#scale}

Bild skalieren. Skaliert ein Ebenenquellenbild nach Faktor im Verhältnis zum Bild mit voller Auflösung.

`scale= *`Faktor`*`

<table id="simpletable_AC596A87494A4213A7D1C76612E8F2FD"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Faktor</span> </p> </td> 
  <td class="stentry"> <p>Skalierungsfaktor (real, größer als 0,0). </p></td> 
 </tr> 
</table>

Wenn keine Skalierung angewendet wird `scale=1`. *`factor`* kleiner als 1,0 Downskala und größer als 1,0 vergrößert das Quellbild.

## Eigenschaften {#section-3c7eb45527394fe79b1ddba6c1fcca09}

Quellbild-/Maskenattribut. Ignoriert , wenn `size=` wird auch für die aktuelle Ebene angegeben. Überschreibungen `res=`. Gilt für Ebene 0, wenn für `layer=comp`. Wird ignoriert, wenn die Ebene nicht mit einem Bild oder einer Maske verknüpft ist.

## Standard {#section-26e64904362342a5a62c5f6598f330c4}

Falls nicht angegeben, `res=` verwendet. Wenn `res=` nicht angegeben ist, wird das Bild ohne Skalierung verwendet.

## Verwandte Themen {#section-61a11f30d37341d58c10df759bfff951}

[res=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md#reference-3d6fe416801148dea0f786f2b5169e55) , [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)
