---
title: OPAC
description: Deckkraft. Gibt die Materialdeckkraft an.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7acd50b2-5c0c-492e-b5a8-105dc027ebcc
TQID: 'https://experienceleague.adobe.com/j4Y-Lk-BL8VybOYqbP256D81w8FFbQqdS0q8z6Y5l1c'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 106
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
