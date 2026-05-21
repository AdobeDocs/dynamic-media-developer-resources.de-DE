---
title: Skala
description: Bild skalieren. Skaliert ein Ebenenquellbild relativ zum Bild mit voller Auflösung nach Faktor.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c2cd37de-f81e-4b08-9a3e-ff05a72c363c
TQID: 'https://experienceleague.adobe.com/qC-yBofpV9CNTTjb8Ll1EYV6Q1YA0BUsLLEHadfLAu8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 113
ht-degree: 2%

---

# Skala{#scale}

Bild skalieren. Skaliert ein Ebenenquellbild relativ zum Bild mit voller Auflösung nach Faktor.

`scale= *`Faktor`*`

<table id="simpletable_AC596A87494A4213A7D1C76612E8F2FD"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Faktor</span> </p> </td> 
  <td class="stentry"> <p>Skalierungsfaktor (real, größer als 0,0). </p></td> 
 </tr> 
</table>

Bei der `scale=1` wird keine Skalierung vorgenommen. *`factor`* kleiner als 1,0 wird das Quellbild herunterskaliert und größer als 1,0 vergrößert.

## Eigenschaften {#section-3c7eb45527394fe79b1ddba6c1fcca09}

Source-Bild-/Maskenattribut. Wird ignoriert, wenn `size=` auch für die aktuelle Ebene angegeben ist. Überschreibt `res=`. Gilt für Ebene 0, wenn für `layer=comp` angegeben. Wird ignoriert, wenn die Ebene keinem Bild oder keiner Maske zugeordnet ist.

## Standard {#section-26e64904362342a5a62c5f6598f330c4}

Wenn nichts angegeben ist, wird `res=` verwendet. Wenn `res=` nicht angegeben ist, wird das Bild ohne Skalierung verwendet.

## Verwandte Themen {#section-61a11f30d37341d58c10df759bfff951}

[res=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md#reference-3d6fe416801148dea0f786f2b5169e55) , [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)
