---
description: Deckkraft. Gibt die Materialdeckkraft an.
solution: Experience Manager
title: opac
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 3%

---


# opac{#opac}

Deckkraft. Gibt die Materialdeckkraft an.

` opac= *`val`*`

<table id="simpletable_6AB8CD75F526469FBC9FEAE049792EF2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val  </span> </p> </td> 
  <td class="stentry"> <p>Materialdeckkraft (in Prozent); 0...100 </p> </td> 
 </tr> 
</table>

Die folgenden Material-/Objektkombinationen unterstützen variable Deckkraft:

* Einfarbige und wiederholbare Texturen, die auf texturierbare überlappende Objekte angewendet werden.
* Fensterbedeckende Materialien, die auf Fensterbedeckungsobjekte angewendet werden.
* Auf texturierbare Objekte oder Wandobjekte angewendete Dekore.

Wenn das Material ein Bild mit einem Alpha-Kanal enthält, kann `opac=` verwendet werden, um das Bild transparenter, aber nicht undurchsichtiger zu machen.

## Eigenschaften {#section-352f7b82ede54159b6afb90ae4b559ec}

Materialattribut. Wird ignoriert, wenn die aktuelle Objektauswahl oder das Material keine Deckkraft unterstützt.

## Standard {#section-bd45105b1e614f96ad5d521e3ef65736}

`opac=100`, für vollständig undurchsichtiges Material (wenn das Bild keinen Alpha-Kanal enthält).
