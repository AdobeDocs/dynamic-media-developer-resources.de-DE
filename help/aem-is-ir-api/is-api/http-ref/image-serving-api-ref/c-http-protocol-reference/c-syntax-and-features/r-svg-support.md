---
description: Image Serving unterstützt SVG-Dateien (Scalable Vector Graphics) als Quelldaten. Die Konformität mit SVG 1.1 ist erforderlich.
solution: Experience Manager
title: SVG-Support
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 60e40195-710f-4f03-b152-52eaa10c5b21
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 0%

---

# SVG-Support{#svg-support}

Image Serving unterstützt SVG-Dateien (Scalable Vector Graphics) als Quelldaten. Die Konformität mit SVG 1.1 ist erforderlich.

Die Bildbereitstellung erkennt nur statische SVG-Inhalte. Animationen, Skripterstellung und andere interaktive Inhalte werden nicht unterstützt.

SVG kann überall dort angegeben werden, wo Bilddateien zulässig sind (URL-Pfad, `src=` und `mask=`). Nachdem der Inhalt der SVG-Datei gerastert wurde, wird er wie ein Bild gehandhabt.

Ähnlich wie Bilder können SVG-Dateien als Bildkatalogeinträge oder als relative Dateipfade angegeben werden.

## Substitutionsvariablen {#section-83b149f13f244193901df39b204c975b}

` $ *[!DNL var]*$` Ersatzvariablen können in der SVG-Datei in den Wert-Zeichenfolgen `<text>` -Elementen und beliebigen Elementattributen enthalten sein.

Wichtige Variablen im Abfrageteil von eingebetteten Bildbereitstellungsanfragen werden nicht direkt ersetzt. Stattdessen werden alle verfügbaren Variablendefinitionen an die Anfrage angehängt, sodass Image Serving beim Analysieren der Anfrage Variablen ersetzen kann.

Siehe [Substitutionsvariablen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a) für weitere Informationen.

## Bildreferenzen {#section-a7680f9e6aca4b1a83560637cc9fac66}

Bilder können mithilfe des `<image>` in SVG eingefügt werden. Bilder, auf die vom `xlink::href`-Attribut des `<image>`-Elements verwiesen wird, müssen gültige Bildbereitstellungsanfragen sein. Fremde URLs sind nicht zulässig.

Geben Sie entweder eine vollständige Image-Serving-Anfrage ab `http://` oder eine relative URL ab `/is/image` an. Wenn ein vollständiger HTTP-Pfad angegeben ist, wird der Domain-Name aus dem Pfad entfernt, um in das relative Format zu konvertieren. Die Verwendung eines vollständigen HTTP-Pfads kann von Vorteil sein, da er die Vorschau der Datei mit einem SVG-Renderer eines Drittanbieters ermöglicht.

>[!NOTE]
>
>Die Unterstützung für das Rendern von Bildern in dieser Version von Image Serving ist begrenzt. Referenzieren von Bildern aus SVG sollte nur in Situationen verwendet werden, in denen die herkömmlichen Bildbereitstellungs-Ebenen und Vorlagenmechanismen nicht ausreichend sind, um das gewünschte Ergebnis zu erzielen. Unter keinen Umständen sollte SVG verwendet werden, um Verbunde mit mehreren Bildern zu erzeugen.

>[!NOTE]
>
>Die Größe von in SVG eingebetteten Bildern wird derzeit nicht automatisch geändert. Stellen Sie sicher, dass alle Bildbereitstellungsbefehle die erforderlichen Image-Serving-Befehle enthalten, um die gewünschte Bildgröße festzulegen (z. B. `wid=`). Wenn die Bildgröße nicht explizit festgelegt ist, wird `attribute::DefaultPix` angewendet.

## Farbmanagement {#section-ea76e2bc4e1842638aa97a2d470c8a68}

Alle Farbwerte, die in SVG-Dateien eingebettet und über Substitutionsvariablen an SVG-Vorlagen übergeben werden, werden als im `sRgb` Farbraum vorhanden angenommen.

Beim Einbetten von Bildern in SVG wird keine Farbkonvertierung durchgeführt. Um die Farbtreue sicherzustellen, müssen Sie `icc=sRgb` für alle eingebetteten Bildanforderungen angeben.

Nach der Rasterung ist das SVG-Bild wie jedes andere Bild am Farbmanagement beteiligt.

## Beispiel {#section-036cdd45abd449849ee00a8f21788c28}

Die folgende SVG-Vorlage veranschaulicht Bildverweise und die Verwendung von Variablen.

`<?xml version="1.0" standalone="no"?> <!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 20010904//EN" "http://www.w3.org/TR/2001/REC-SVG-20010904/DTD/svg10.dtd"> <svg width="500" height="500"> <image x="50" y="50" width="400" height="400" xlink:href="/is/image?src=$img$&wid=300&hei=400"/> <text x="150" y="400" style="font-size:$pts$; fill:$color$"> Title: $txt$ </text> </svg>`

Diese SVG-Vorlage kann wie folgt verwendet werden:

`http://server/is/image/mySvgTemplate.svg?$txt=Svg%20Template%20Test&$img=myImage.tif&$color=red&$pts=40&qlt=95`

## Einschränkungen {#section-daa5eccd07204aaf993be41e87822d54}

SVG-Dateien müssen eigenständig sein und dürfen keine sekundären Dateien oder Ressourcen referenzieren, mit Ausnahme von externen Bildern, auf die mit Bildbereitstellungs- oder Bildbereitstellungsanfragen verwiesen wird (siehe oben).

Es werden nur statische Inhalte gerendert. Animation, interaktive Funktionen wie Schaltflächen usw. Kann vorhanden sein, kann aber nicht wie erwartet gerendert werden.

ICC-profilbasierte Farbspezifikationen werden derzeit nicht unterstützt.

`<script>` Elemente können vorhanden sein, werden jedoch immer ignoriert.

## Verwandte Themen {#section-901dd1775fd24154a766dcfbe5032b67}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) , [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [Spezifikation für SVG 1.1](https://www.w3.org/TR/SVG11/)
