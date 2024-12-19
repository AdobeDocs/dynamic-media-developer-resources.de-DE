---
title: Größe
description: Ebenengröße. Legt die Größe oder maximale Ebenengröße für eine Ebene fest, bevor Rotation=, Perspektive= und Dehnen= auf die Ebene angewendet werden.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 55feeb32-b69d-4b95-80fb-c77f2612d255
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 1%

---

# Größe{#size}

Ebenengröße. Legt die Größe oder maximale Ebenengröße für eine Ebene fest, bevor Rotation=, Perspektive= und Dehnen= auf die Ebene angewendet werden.

` size= *`width`*, *`height`*`

` sizeN= *`widthN`*, *`heightN`*`

<table id="simpletable_FBE17D736F93485AA0053BF447B4CC9F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> Breite </span>, <span class="varname"> Höhe </span> </span> </p> </td> 
  <td class="stentry"> <p>Beschränkung der Ebenengröße in Pixel (int, int, 0 oder höher). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> widthN </span>, <span class="varname"> heightN </span> </span> </p> </td> 
  <td class="stentry"> <p>Die Ebenengrößenbeschränkung wurde relativ zur Größe der Ebene 0 normalisiert (real, real, 0.0…1.0). </p> </td> 
 </tr> 
</table>

Wenn für eine Bildebene angegeben, schränkt size= die Breite, Höhe oder beides der Bildebene ein. Das Bild wird so skaliert, dass es nicht größer als `size=` ist. Wenn eine normalisierte Größe angegeben wird, ist diese relativ zur Größe der Ebene 0. Wenn sowohl *`width`* als auch *`height`* angegeben sind, wird das Quellbild skaliert (nachdem `crop=` angewendet wurde), sodass keine der Dimensionen die angegebene Größe überschreitet. Das Seitenverhältnis des Quellrechtecks wird in allen Fällen beibehalten. *`width`* oder *`height`* können auf 0 gesetzt werden. In diesem Fall wird der Wert vom Server basierend auf dem Seitenverhältnis des Bildes berechnet.

Wenn für eine Textebene angegeben, gibt `size=` die Größe des Textfelds an. *`width`* ist erforderlich; *`height`* kann auf 0 gesetzt werden. In diesem Fall wird die Höhe des Textes als Layerhöhe verwendet. Standardmäßig fügen die Text-Layout-Engines Zeilenumbrüche ein, um sicherzustellen, dass Text immer horizontal in den verfügbaren Platz passt. Wenn *`height`* angegeben ist, werden Zeilen, die nicht in den verfügbaren Platz passen, abgeschnitten (`text=`) oder weggelassen (`textPs=`). `text=` unterstützt zusätzliche Anpassungsmodi. Weitere Informationen finden Sie in `textAttr=`.

Wenn für eine Volltonfarbschicht angegeben, definiert `size=` die genaue Ebenengröße. Beide Werte müssen angegeben werden (es sei denn, eine Maske wird bereitgestellt). Wenn `mask=` ebenfalls angegeben ist, wird die Größe des Maskenbilds so angepasst, `size=` sie in Bildebenen skaliert werden kann.

## Eigenschaften {#section-5f254b66fcba49bcb63f9c9ea40b230c}

Ebenenattribut. Gilt für Ebene 0, falls `layer=comp`. `sizeN=` ist für `layer=0` oder `layer=comp` nicht zulässig. `sizeN=` ist für `layer=0` und `layer=comp` nur in Katalogdatensätzen zulässig, die Wasserzeichenbilder definieren. In diesem Fall definiert `sizeN` die Skalierung des Wasserzeichenbildes relativ zu dem zusammengesetzten Bild, auf das das Wasserzeichen angewendet wird. Wenn `size=` angegeben ist, werden `res=` und `scale=` für diese Ebene ignoriert. Von Effektebenen ignoriert.

## Standard {#section-43d129deba6a441da66a1fdb63d1c85c}

`size=0,0` ist die Ebenengröße nicht beschränkt. Bei Bildebenen wird die Ebenengröße dann anhand der Ebenenbildgröße bestimmt, nachdem alle `crop=`, `scale=` oder `res=` Operationen angewendet wurden. Bei Textebenen wird die Größe der Ebene automatisch an den gerenderten Text angepasst, wenn `size=` nicht angegeben ist.

Für einfarbige Schichten ist entweder eine vollständig angegebene `size=`, ein `mask=` oder ein `clipPath=` erforderlich.

## Beispiel {#section-d1adaddd9e0b4ca881fd8e0a7541e5d9}

Siehe [Beispiel A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) unter [Vorlagen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Verwandte Themen {#section-63dfdf3750e249d2ab4c825ccd2e7181}

[scale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065) , [res=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md#reference-3d6fe416801148dea0f786f2b5169e55), [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d), [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d), [Textebenen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
