---
description: Image Serving unterstützt skalierbare Vector Graphics (SVG)-Dateien als Quelldaten. Die Konformität mit SVG 1.1 ist erforderlich.
solution: Experience Manager
title: SVG-Unterstützung
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 60e40195-710f-4f03-b152-52eaa10c5b21
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '507'
ht-degree: 0%

---

# SVG-Unterstützung{#svg-support}

Image Serving unterstützt skalierbare Vector Graphics (SVG)-Dateien als Quelldaten. Die Konformität mit SVG 1.1 ist erforderlich.

Image Serving erkennt nur statische SVG-Inhalte. Animationen, Skripten und andere interaktive Inhalte werden nicht unterstützt.

SVG kann überall dort angegeben werden, wo Bilddateien zulässig sind (URL-Pfad, `src=`, und `mask=`). Nachdem der Inhalt der SVG-Datei gerastert wurde, wird er wie ein Bild behandelt.

Ähnlich wie bei Bildern können SVG-Dateien als Bildkatalogeinträge oder als relative Dateipfade angegeben werden.

## Ersatzvariablen {#section-83b149f13f244193901df39b204c975b}

` $ *[!DNL var]*$` Ersatzvariablen können in der SVG-Datei in den Wertzeichenfolgen enthalten sein. `<text>` Elemente und jedes Elementattribut.

Wichtige Variablen im Abfrageteil eingebetteter Image-Serving-Anforderungen werden nicht direkt ersetzt. Stattdessen werden alle verfügbaren Variablendefinitionen an die Anfrage angehängt, wodurch das Image Serving Variablen beim Analysieren der Anforderung ersetzen kann.

Siehe [Ersatzvariablen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a) für weitere Informationen.

## Bildverweise {#section-a7680f9e6aca4b1a83560637cc9fac66}

Bilder können mit der `<image>` -Element. Bilder, auf die von der `xlink::href` -Attribut `<image>` -Element müssen gültige Bildbereitstellungsanfragen sein. Ausländische URLs sind nicht zulässig.

Geben Sie entweder eine vollständige Image Serving-Anforderung an, beginnend mit `http://`oder eine relative URL, beginnend mit `/is/image`. Wenn ein vollständiger HTTP-Pfad angegeben ist, wird der Domänenname aus dem Pfad entfernt, um in das relative Format zu konvertieren. Die Verwendung eines vollständigen HTTP-Pfads kann von Vorteil sein, da es die Vorschau der Datei mit einem SVG-Renderer eines Drittanbieters ermöglicht.

>[!NOTE]
>
>Die Unterstützung für das Rendern von Bildern in dieser Version von Image Serving ist eingeschränkt. Verweise auf Bilder aus SVG sollten nur in Fällen verwendet werden, in denen die herkömmlichen Bildbereitstellungs-Ebenen und Vorlagenmechanismen nicht ausreichen, um das gewünschte Ergebnis zu erzielen. Unter keinen Umständen sollte SVG zum Generieren von Mehrbild-Composites verwendet werden.

>[!NOTE]
>
>Die Größe von in SVG eingebetteten Bildern wird derzeit nicht automatisch geändert. Stellen Sie sicher, dass alle href die erforderlichen Image Serving-Befehle enthalten, um die gewünschte Bildgröße festzulegen (z. B. `wid=`). Wenn die Bildgröße nicht explizit festgelegt ist, `attribute::DefaultPix` angewendet wird.

## Farbmanagement {#section-ea76e2bc4e1842638aa97a2d470c8a68}

Es wird angenommen, dass alle Farbwerte, die in SVG-Dateien eingebettet und über Ersatzvariablen an SVG-Vorlagen übergeben werden, im `sRgb` Farbraum.

Wenn Bilder in die SVG eingebettet werden, erfolgt keine Farbkonvertierung. Um die Farbtreue sicherzustellen, geben Sie `icc=sRgb` für alle eingebetteten Bildanforderungen.

Nach der Rasterung nimmt das SVG-Bild wie jedes andere Bild am Farbmanagement teil.

## Beispiel {#section-036cdd45abd449849ee00a8f21788c28}

Die folgende SVG-Vorlage zeigt die Bildreferenzen und die Verwendung von Variablen.

`<?xml version="1.0" standalone="no"?> <!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 20010904//EN" "http://www.w3.org/TR/2001/REC-SVG-20010904/DTD/svg10.dtd"> <svg width="500" height="500"> <image x="50" y="50" width="400" height="400" xlink:href="/is/image?src=$img$&wid=300&hei=400"/> <text x="150" y="400" style="font-size:$pts$; fill:$color$"> Title: $txt$ </text> </svg>`

Diese SVG-Vorlage kann wie folgt verwendet werden:

`http://server/is/image/mySvgTemplate.svg?$txt=Svg%20Template%20Test&$img=myImage.tif&$color=red&$pts=40&qlt=95`

## Einschränkungen {#section-daa5eccd07204aaf993be41e87822d54}

SVG-Dateien müssen eigenständig sein und dürfen keine sekundären Dateien oder Ressourcen referenzieren, mit Ausnahme externer Bilder, die mit Image Serving- oder Image Rendering-Anforderungen referenziert werden (siehe oben).

Nur statische Inhalte werden gerendert. Animation, interaktive Funktionen wie Schaltflächen usw. vorhanden sein, möglicherweise aber nicht wie erwartet gerendert werden.

ICC-profilbasierte Farbspezifikationen werden derzeit nicht unterstützt.

`<script>` -Elemente vorhanden sein, werden jedoch immer ignoriert.

## Verwandte Themen {#section-901dd1775fd24154a766dcfbe5032b67}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) , [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [SVG 1.1 Spezifikation](https://www.w3.org/TR/SVG11/)
