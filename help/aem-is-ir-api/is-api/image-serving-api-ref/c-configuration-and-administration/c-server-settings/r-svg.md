---
title: SVG
description: Die Einstellungen in diesem Abschnitt dürfen nur berücksichtigt werden, wenn SVG-Rendering erforderlich ist.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 2863cc86-1f79-4db3-bd6f-a42839ef3439
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 2%

---

# SVG{#svg}

Die Einstellungen in diesem Abschnitt dürfen nur berücksichtigt werden, wenn SVG-Rendering erforderlich ist.

## SV::SvgHeapSize - SVG-Heap-Größe {#section-59ab17681daa4be8b5d794713e1a504e}

Die Java Heap-Größe für den SVG Renderer. Die Standardeinstellung ist „200m“ (200 MB).

## PS::svgProvider.rootPaths - SVG-Datenstammordner {#section-70fe575b0ad54e3b8b6d3a01ea8f1f44}

Der Speicherort der SVG-Quelldatendateien. Es kann sich um einen oder mehrere absolute Dateipfade oder Pfade relativ zu *[!DNL install_folder]* handeln, die durch Semikolons getrennt sind. Normalerweise auf denselben Wert wie `IS::RootPath` festgelegt.

## PS::svgProvider.SVGFileSizeLimit - Maximale Dateigröße für SVG {#section-b9c81e3e104642ebbdd9f000843d3256}

Maximale Größe der SVG-Quelldatei in kByte. Der Server gibt einen Fehler zurück, wenn versucht wird, eine SVG-Datei zu rendern, die größer als diese Beschränkung ist. Der Standardwert ist 1024 KB.

## IS::SvgMAxRenderRgnPixels - Größenbeschränkung des SVG-Ausgabebilds {#section-5be1fd9639424d878a5ffd11736d3920}

Dadurch wird die Größe der Bilder begrenzt, die SVGRender erzeugen kann. Ganzzahliger Wert größer als 0 in Millionen von Pixeln. Ein Fehler wird zurückgegeben, wenn ein Render-Vorgang die Größenbeschränkung überschreiten würde. Der Standardwert ist 4.

## PS::svgProvider.port - [!DNL Platform Server] Listening-Port {#section-f7e42a96c2dd4523b46f0557c239e659}

Der Port, der für SvgRender zum Abrufen von Bildern aus der [!DNL Platform Server] verwendet wird, die in SVG-Renderings eingebettet werden sollen.

Wichtig Für eine ordnungsgemäße Funktion der SVGRender-Komponente muss diese Konfigurationsoption auf denselben Wert wie `TC::PsPort` gesetzt werden.

## PS::svgProvider.fontRoot - Ordner mit SVG-Schriftarten {#section-a8d45b0d68504945b8780f5eac351b0d}

Gibt an, wo SvgRender die Schriftdateien findet, die zum Rendern von SVG-Text benötigt werden; normalerweise einer der in `IS::RootPaths` angegebenen Pfade. Der Standardwert ist [!DNL *[!DNL install_folder]*/images].

## SVG::SVGRender.port, IS::SVGTcpPort - SVG Communications Port {#section-608687123aa644b7b58fe42385d71b79}

Konfiguriert den Port, über den der Bild-Server und die SVGRender-Komponente kommunizieren.

>[!NOTE]
>
>Damit die SVGRender-Komponente ordnungsgemäß funktioniert, muss für `SVG::SVGRender.port` und `IS::SVGTcpPort` dieselbe Portnummer angegeben werden.
