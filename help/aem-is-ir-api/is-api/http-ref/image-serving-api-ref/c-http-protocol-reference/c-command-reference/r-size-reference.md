---
title: Größe
description: 'Ebenengröße. Gibt die Größe oder die maximale Ebenengröße für eine Ebene an, bevor auf die Ebene Folgendes angewendet wird: rotate=, visibility=, and expand=.'
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 55feeb32-b69d-4b95-80fb-c77f2612d255
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 1%

---

# Größe{#size}

Ebenengröße. Gibt die Größe oder die maximale Ebenengröße für eine Ebene an, bevor auf die Ebene Folgendes angewendet wird: rotate=, visibility=, and expand=.

` size= *`width`*, *`height`*`

` sizeN= *`widthN`*, *`heightN`*`

<table id="simpletable_FBE17D736F93485AA0053BF447B4CC9F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> width </span>, <span class="varname"> height </span> </span> </p> </td> 
  <td class="stentry"> <p>Begrenzung der Ebenengröße in Pixel (int, int, 0 oder höher). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> widthN </span>, <span class="varname"> heightN </span> </span> </p> </td> 
  <td class="stentry"> <p>Ebenengrößenbegrenzung normalisiert sich relativ zur Ebenengröße 0 (real, real, 0.0...1.0). </p> </td> 
 </tr> 
</table>

Wenn für eine Bildebene angegeben, beschränkt size= die Breite oder Höhe des Ebenenbilds oder beides. Das Bild wird so skaliert, dass es nicht größer ist als `size=`. Wenn eine normalisierte Größe angegeben wird, ist sie relativ zur Größe der Ebene 0. Wenn *`width`* und *`height`* festgelegt sind, wird das Quellbild skaliert (nach `crop=` angewendet wird), sodass keine der Dimensionen die angegebene Größe überschreitet. Das Seitenverhältnis des Quellrechtecks wird in allen Fällen beibehalten. Entweder *`width`* oder *`height`* kann auf 0 gesetzt werden. In diesem Fall wird der Wert vom Server basierend auf dem Seitenverhältnis des Bildes berechnet.

Wenn für eine Textebene angegeben, `size=` gibt die Größe des Textfelds an. *`width`* erforderlich ist; *`height`* kann auf 0 gesetzt werden. In diesem Fall wird die Höhe des ausgelegten Textes als Ebenenhöhe verwendet. Standardmäßig fügen die Textlayout-Engines Zeilenumbrüche ein, um sicherzustellen, dass der Text immer horizontal in den verfügbaren Bereich passt. Wenn *`height`* angegeben ist, werden Zeilen, die nicht in den verfügbaren Bereich passen, abgeschnitten ( `text=`) oder ausgelassen ( `textPs=`). `text=` unterstützt zusätzliche Anpassungsmodi; siehe `textAttr=` für Details.

Wenn für eine Farbschicht angegeben, `size=` definiert die genaue Ebenengröße. Beide Werte müssen angegeben werden (es sei denn, eine Maske wird bereitgestellt). Wenn `mask=` wird auch die Größe des Maskenbilds festgelegt. `size=` Bilder werden auf die gleiche Weise in Bildebenen skaliert.

## Eigenschaften {#section-5f254b66fcba49bcb63f9c9ea40b230c}

Ebenenattribut. Gilt für Ebene 0, wenn `layer=comp`. `sizeN=` ist nicht zulässig für `layer=0` oder `layer=comp`. `sizeN=` ist zulässig für `layer=0` und `layer=comp` nur in Katalogdatensätzen, die Wasserzeichenbilder definieren. In diesem Fall `sizeN` definiert die Skalierung des Wasserzeichenbilds relativ zum zusammengesetzten Bild, auf das das Wasserzeichen angewendet wird. Wenn `size=` festgelegt ist, `res=` und `scale=` werden für diese Ebene ignoriert. Wird von Effektebenen ignoriert.

## Standard {#section-43d129deba6a441da66a1fdb63d1c85c}

`size=0,0`festgelegt ist, ist die Ebenengröße nicht beschränkt. Bei Bildebenen wird die Ebenengröße dann basierend auf der Ebenenbildgröße nach einer beliebigen `crop=`, `scale=`oder `res=` -Vorgänge angewendet wurden. Bei Textebenen, wenn `size=` nicht angegeben ist, wird die Ebene automatisch an den gerenderten Text angepasst.

Solide Farbschichten erfordern entweder eine vollständig spezifizierte `size=`, a `mask=`oder `clipPath=`.

## Beispiel {#section-d1adaddd9e0b4ca881fd8e0a7541e5d9}

Siehe [Beispiel A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) in [Vorlagen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Verwandte Themen {#section-63dfdf3750e249d2ab4c825ccd2e7181}

[scale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065) , [res=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md#reference-3d6fe416801148dea0f786f2b5169e55), [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d), [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d), [Textebenen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
