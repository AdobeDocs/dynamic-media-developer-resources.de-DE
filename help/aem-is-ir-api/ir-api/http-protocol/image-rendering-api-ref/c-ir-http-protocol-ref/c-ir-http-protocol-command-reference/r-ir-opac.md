---
title: opac
description: Deckkraft. Gibt die Materialdeckkraft an.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7acd50b2-5c0c-492e-b5a8-105dc027ebcc
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 0%

---

# opac{#opac}

Deckkraft. Gibt die Materialdeckkraft an.

` opac= *`val`*`

<table id="simpletable_6AB8CD75F526469FBC9FEAE049792EF2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>Materialdeckkraft (in Prozent); 0...100 </p> </td> 
 </tr> 
</table>

Die folgenden Material-/Objektkombinationen unterstützen die variable Deckkraft:

* Durchgehende Farbe und wiederholbare Texturen, die auf Texturüberlappungsobjekte angewendet werden.
* Fensterabdeckende Materialien, die auf Fensterscheiben angewendet werden, die Rahmenobjekte bedecken.
* Auf Textobjekte oder Wandobjekte angewendete Deklarationen.

Wenn das Material ein Bild mit einem Alphakanal enthält, kann `opac=` verwendet werden, um das Bild transparenter, aber nicht undurchsichtiger zu machen.

## Eigenschaften {#section-352f7b82ede54159b6afb90ae4b559ec}

Materialattribut. Wird ignoriert, wenn die aktuelle Objektauswahl oder das Material die Deckkraft nicht unterstützt.

## Standard {#section-bd45105b1e614f96ad5d521e3ef65736}

`opac=100` für ein vollständig opak Material (wenn das Bild keinen Alphakanal enthält).
