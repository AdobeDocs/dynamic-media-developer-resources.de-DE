---
title: OPAC
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

# OPAC{#opac}

Deckkraft. Gibt die Materialdeckkraft an.

` opac= *`val`*`

<table id="simpletable_6AB8CD75F526469FBC9FEAE049792EF2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> Val </span> </p> </td> 
  <td class="stentry"> <p>Materialdeckkraft (Prozent); 0…100 </p> </td> 
 </tr> 
</table>

Die folgenden Material/Objekt-Kombinationen unterstützen eine variable Deckkraft:

* Volltonfarbe und wiederholbare Texturen, die auf textuelle Überlappungsobjekte angewendet werden.
* Fensterabdeckungsmaterialien, die auf Fensterabdeckungsrahmenobjekte angewendet werden.
* Abziehbilder, die auf Texturobjekte oder Wandobjekte angewendet werden.

Wenn das Material ein Bild mit einem Alphakanal enthält, können `opac=` verwendet werden, um das Bild transparenter, aber nicht deckender zu machen.

## Eigenschaften {#section-352f7b82ede54159b6afb90ae4b559ec}

Materialattribut. Wird ignoriert, wenn die aktuelle Objektauswahl oder das Material keine Deckkraft unterstützen.

## Standard {#section-bd45105b1e614f96ad5d521e3ef65736}

`opac=100` für ein vollständig opakes Material (wenn das Bild keinen Alphakanal enthält).
