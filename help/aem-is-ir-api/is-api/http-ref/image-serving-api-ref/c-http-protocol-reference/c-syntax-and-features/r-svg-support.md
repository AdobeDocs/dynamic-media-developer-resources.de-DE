---
description: Image Serving unterstützt SVG-Dateien (Scalable Vector Graphics) als Quelldaten. Die Kompatibilität mit SVG 1.1 ist erforderlich.
seo-description: Image Serving unterstützt SVG-Dateien (Scalable Vector Graphics) als Quelldaten. Die Kompatibilität mit SVG 1.1 ist erforderlich.
seo-title: SVG-Unterstützung
solution: Experience Manager
title: SVG-Unterstützung
topic: Scene7 Image Serving - Image Rendering API
uuid: 30d7b37d-fdef-4518-a4b3-4baee56fa634
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '522'
ht-degree: 0%

---


# SVG-Unterstützung{#svg-support}

Image Serving unterstützt SVG-Dateien (Scalable Vector Graphics) als Quelldaten. Die Kompatibilität mit SVG 1.1 ist erforderlich.

Image Serving erkennt nur statische SVG-Inhalte. Animationen, Skripten und andere interaktive Inhalte werden nicht unterstützt.

SVG kann überall dort angegeben werden, wo Bilddateien zulässig sind (URL-Pfad, `src=` und `mask=`). Nachdem der Inhalt der SVG-Datei gerastert wurde, wird er wie ein Bild behandelt.

Ähnlich wie bei Bildern können SVG-Dateien als Bildkatalogeinträge oder als relative Dateipfade angegeben werden.

## Substitutionsvariablen {#section-83b149f13f244193901df39b204c975b}

` $ *[!DNL var]*$` Ersatzvariablen können in die SVG-Datei in die  `<text>` Elemente der Wertzeichenfolgen und jedes Elementattribut aufgenommen werden.

Wichtige Variablen im Bereich Abfrage von eingebetteten Image Serving-Anforderungen werden nicht direkt ersetzt. Stattdessen werden alle verfügbaren Variablendefinitionen an die Anforderung angehängt, sodass Image Serving Variablen beim Analysieren der Anforderung ersetzen kann.

Weitere Informationen finden Sie unter [Ersatzvariablen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a).

## Bildverweise {#section-a7680f9e6aca4b1a83560637cc9fac66}

Bilder können mit dem `<image>`-Element in SVG eingefügt werden. Bilder, auf die vom `xlink::href`-Attribut des `<image>`-Elements verwiesen wird, müssen gültige Image Serving-Anforderungen sein. Ausländische URLs sind nicht zulässig.

Geben Sie entweder eine vollständige Image Serving-Anforderung an, beginnend mit `http://`, oder eine relative URL, beginnend mit `/is/image`. Wenn ein vollständiger HTTP-Pfad angegeben ist, wird der Domänenname aus dem Pfad entfernt, um in das relative Format zu konvertieren. Die Verwendung eines vollständigen HTTP-Pfads kann von Vorteil sein, da die Datei mit einem SVG-Renderer eines Drittanbieters in der Vorschau angezeigt werden kann.

>[!NOTE]
>
>Die Unterstützung für das Rendern von Bildern in dieser Version von Image Serving ist eingeschränkt. Verweisende Bilder aus SVG sollten nur in Situationen verwendet werden, in denen herkömmliche Bildservierungs- und Vorlagerungsmechanismen nicht ausreichen, um das gewünschte Ergebnis zu erzielen. Unter keinen Umständen sollte SVG zum Generieren von Mehrbild-Composites verwendet werden.

>[!NOTE]
>
>Die Größe von in SVG eingebetteten Bildern wird derzeit nicht automatisch angepasst. Stellen Sie sicher, dass alle href die erforderlichen Image Serving-Befehle enthalten, um die gewünschte Bildgröße (z. `wid=`). Wenn die Bildgröße nicht explizit festgelegt ist, wird `attribute::DefaultPix` angewendet.

## Farbmanagement {#section-ea76e2bc4e1842638aa97a2d470c8a68}

Es wird angenommen, dass alle Farbwerte, die in SVG-Dateien eingebettet und über Substitutionsvariablen an SVG-Vorlagen übergeben werden, im Farbraum `sRgb` vorhanden sind.

Beim Einbetten von Bildern in das SVG wird keine Farbkonvertierung durchgeführt. Um die Farbtreue sicherzustellen, müssen Sie für alle eingebetteten Bildanforderungen `icc=sRgb` angeben.

Nach der Rasterung nimmt das SVG-Bild wie jedes andere Bild am Farbmanagement teil.

## Beispiel {#section-036cdd45abd449849ee00a8f21788c28}

Die folgende SVG-Vorlage zeigt die Bildverweise und die Verwendung von Variablen.

`<?xml version="1.0" standalone="no"?> <!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 20010904//EN" "http://www.w3.org/TR/2001/REC-SVG-20010904/DTD/svg10.dtd"> <svg width="500" height="500"> <image x="50" y="50" width="400" height="400" xlink:href="/is/image?src=$img$&wid=300&hei=400"/> <text x="150" y="400" style="font-size:$pts$; fill:$color$"> Title: $txt$ </text> </svg>`

Diese SVG-Vorlage kann wie folgt verwendet werden:

`http://server/is/image/mySvgTemplate.svg?$txt=Svg%20Template%20Test&$img=myImage.tif&$color=red&$pts=40&qlt=95`

## Einschränkungen {#section-daa5eccd07204aaf993be41e87822d54}

SVG-Dateien müssen eigenständig sein und dürfen keine sekundären Dateien oder Ressourcen referenzieren, mit Ausnahme externer Bilder, auf die mit Image Serving- oder Image Rendering-Anforderungen verwiesen wird (siehe oben).

Nur statischer Inhalt wird gerendert. Animation, interaktive Funktionen wie Schaltflächen usw. vorhanden sein, jedoch möglicherweise nicht erwartungsgemäß gerendert werden.

ICC-Profil-basierte Farbspezifikationen werden derzeit nicht unterstützt.

`<script>` -Elemente vorhanden sein, werden jedoch immer ignoriert.

## Verwandte Themen {#section-901dd1775fd24154a766dcfbe5032b67}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) ,  [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e),  [SVG 1.1-Spezifikation](http://www.w3.org/TR/SVG11/)
