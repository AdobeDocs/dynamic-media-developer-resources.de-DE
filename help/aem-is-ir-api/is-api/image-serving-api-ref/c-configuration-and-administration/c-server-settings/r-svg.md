---
description: Die Einstellungen in diesem Abschnitt müssen nur berücksichtigt werden, wenn das SVG-Rendering erforderlich ist.
seo-description: Die Einstellungen in diesem Abschnitt müssen nur berücksichtigt werden, wenn das SVG-Rendering erforderlich ist.
seo-title: SVG
solution: Experience Manager
title: SVG
topic: Scene7 Image Serving - Image Rendering API
uuid: 9e69b150-46ac-480f-96db-afadccc40fe4
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 1%

---


# SVG{#svg}

Die Einstellungen in diesem Abschnitt müssen nur berücksichtigt werden, wenn das SVG-Rendering erforderlich ist.

## SV::SvgHeapSize - SVG-Heap-Größe {#section-59ab17681daa4be8b5d794713e1a504e}

Die Java-Heap-Größe für den SVG-Renderer. Der Standardwert ist &quot;200m&quot;(200 MB).

## PS::svgProvider.rootPaths - SVG-Datenstammordner {#section-70fe575b0ad54e3b8b6d3a01ea8f1f44}

Der Speicherort der SVG-Quelldatendateien. Kann ein oder mehrere absolute Dateipfade oder Pfade relativ zu *[!DNL install_folder]* sein, durch Semikolons getrennt. Normalerweise auf denselben Wert wie `IS::RootPath`.

## PS::svgProvider.SVGFileSizeLimit - Maximale SVG-Dateigröße {#section-b9c81e3e104642ebbdd9f000843d3256}

Maximale Größe der SVG-Quelldatei in kBytes. Der Server gibt einen Fehler zurück, wenn versucht wird, eine SVG-Datei wiederzugeben, die größer als diese Grenze ist. Der Standardwert ist 1024 KB.

## IS::SvgMAxRenderRgnPixels - SVG-Bildgrößenbeschränkung {#section-5be1fd9639424d878a5ffd11736d3920}

Begrenzt die Größe der Bilder, die SVGRender produzieren kann. Ganzzahlwert größer als 0 in Millionen Pixeln. Ein Fehler wird zurückgegeben, wenn ein Rendervorgang die Größenbeschränkung überschreitet. Die Standardgrenze ist 4.

## PS::svgProvider.port - Platform Server-Listening-Anschluss {#section-f7e42a96c2dd4523b46f0557c239e659}

Der Anschluss, der für SvgRender verwendet wird, um Bilder vom Platform-Server abzurufen, die in SVG-Renderings eingebettet werden sollen.

Wichtig Damit die SVGRender-Komponente ordnungsgemäß funktioniert, muss diese Konfigurationsoption auf denselben Wert wie `TC::PsPort`.

## PS::svgProvider.fontRoot - Ordner mit SVG-Schriftartdateien {#section-a8d45b0d68504945b8780f5eac351b0d}

Gibt an, wo der SvgRender die Schriftartdateien findet, die für die Wiedergabe von SVG-Text benötigt werden; in der Regel einen der unter `IS::RootPaths`. Der Standardwert ist [!DNL *[!DNL install_folder]*/images].

## SVG::SVGRender.port, IS::SVGTcpPort - SVG Communications Port {#section-608687123aa644b7b58fe42385d71b79}

Konfiguriert den Anschluss, an dem der Image-Server und die SVGRender-Komponente kommunizieren.

>[!NOTE]
>
>Damit die SVGRender-Komponente ordnungsgemäß funktioniert, muss dieselbe Anschlussnummer für `SVG::SVGRender.port` und `IS::SVGTcpPort`angegeben werden.

