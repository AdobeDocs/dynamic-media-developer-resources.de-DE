---
description: Ebenengröße. Gibt die Größe oder maximale Ebenengröße für eine Ebene an, bevor "rotate=", "perspective="und "extended="auf die Ebene angewendet werden.
seo-description: Ebenengröße. Gibt die Größe oder maximale Ebenengröße für eine Ebene an, bevor "rotate=", "perspective="und "extended="auf die Ebene angewendet werden.
seo-title: Größe
solution: Experience Manager
title: Größe
topic: Scene7 Image Serving - Image Rendering API
uuid: c9c13062-7974-4dd9-aff4-f9502bcf442e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 1%

---


# Größe{#size}

Ebenengröße. Gibt die Größe oder maximale Ebenengröße für eine Ebene an, bevor &quot;rotate=&quot;, &quot;perspective=&quot;und &quot;extended=&quot;auf die Ebene angewendet werden.

` size= *``*, *`widthheight`*`

` sizeN= *``*, *`widthNheightN`*`

<table id="simpletable_FBE17D736F93485AA0053BF447B4CC9F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> width  </span>,  <span class="varname"> height  </span> </span> </p> </td> 
  <td class="stentry"> <p>Begrenzung der Ebenengröße in Pixel (int, int, 0 oder höher). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> widthN  </span>,  <span class="varname"> heightN  </span> </span> </p> </td> 
  <td class="stentry"> <p>Ebenengrößenbeschränkung normalisiert relativ zur Ebene 0 (real, real, 0.0...1.0). </p> </td> 
 </tr> 
</table>

Wenn für eine Bildebene &quot;size=&quot;angegeben ist, wird die Breite oder Höhe des Ebenenbilds bzw. beides eingeschränkt. Das Bild wird so skaliert, dass es nicht größer ist als `size=`. Wenn eine normalisierte Größe angegeben wird, ist sie relativ zur Größe der Ebene 0. Wenn sowohl *`width`* als auch *`height`* angegeben sind, wird das Quellbild skaliert (nachdem `crop=` angewendet wurde), sodass keine der beiden Dimensionen die angegebene Größe überschreitet. Das Seitenverhältnis des Quellrechtecks wird in allen Fällen beibehalten. *`width`* oder *`height`* kann auf 0 eingestellt werden. in diesem Fall wird der Wert vom Server basierend auf dem Seitenverhältnis des Bildes berechnet.

Wenn für eine Textebene angegeben, gibt `size=` die Größe des Textfelds an. *`width`* erforderlich ist;  *`height`* kann auf 0 gesetzt werden. In diesem Fall wird die Höhe des Layouttextes als Ebenenhöhe verwendet. Standardmäßig fügen die Textlayout-Engines Zeilenumbrüche ein, um sicherzustellen, dass der Text immer horizontal in den verfügbaren Platz passt. Wenn *`height`* angegeben ist, werden Zeilen, die nicht in den verfügbaren Raum passen, abgeschnitten ( `text=`) oder ausgelassen ( `textPs=`). `text=` unterstützt zusätzliche Formate für die Anpassung; Weitere Informationen finden Sie  `textAttr=` unter .

Wenn für eine Farbflächenebene angegeben, definiert `size=` die exakte Ebenengröße. Beide Werte müssen angegeben werden (es sei denn, eine Maske wird bereitgestellt). Wenn `mask=` ebenfalls angegeben ist, wird die Größe des Maskenbilds auf `size=` genau so angepasst, wie Bilder in Bildebenen skaliert werden.

## Eigenschaften {#section-5f254b66fcba49bcb63f9c9ea40b230c}

Ebenenattribut. Gilt für Ebene 0, wenn `layer=comp`. `sizeN=` ist nicht zulässig für  `layer=0` oder  `layer=comp`. `sizeN=` ist für  `layer=0` und  `layer=comp` nur in Katalogdatensätzen zulässig, die Wasserzeichenbilder definieren. In diesem Fall definiert `sizeN` die Skalierung des Wasserzeichenbilds relativ zum Composite-Bild, auf das das Wasserzeichen angewendet wird. Wenn `size=` angegeben ist, werden `res=` und `scale=` für diese Ebene ignoriert. Von Effektebenen ignoriert.

## Standard {#section-43d129deba6a441da66a1fdb63d1c85c}

`size=0,0`festgelegt ist, ist die Ebenengröße nicht eingeschränkt. Bei Bildebenen wird die Ebenengröße dann basierend auf der Bildgröße der Ebene bestimmt, nachdem beliebige Vorgänge wie `crop=`, `scale=` oder `res=` angewendet wurden. Wenn für Textebenen `size=` nicht angegeben ist, wird die Ebene automatisch an den gerenderten Text angepasst.

Einfarbige Ebenen erfordern entweder ein vollständig angegebenes `size=`, ein `mask=` oder ein `clipPath=`.

## Beispiel {#section-d1adaddd9e0b4ca881fd8e0a7541e5d9}

Siehe [Beispiel A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) in [Vorlagen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Verwandte Themen {#section-63dfdf3750e249d2ab4c825ccd2e7181}

[scale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065) ,  [res=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md#reference-3d6fe416801148dea0f786f2b5169e55),  [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d),  [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e),  [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d),  [Textebenen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
