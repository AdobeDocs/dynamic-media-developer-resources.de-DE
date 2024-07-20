---
title: SVG
description: Die Einstellungen in diesem Abschnitt müssen nur berücksichtigt werden, wenn ein SVG-Rendering erforderlich ist.
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

Die Einstellungen in diesem Abschnitt müssen nur berücksichtigt werden, wenn ein SVG-Rendering erforderlich ist.

## SV::SvgHeapSize - SVG Heap Size {#section-59ab17681daa4be8b5d794713e1a504e}

Die Java-Heap-Größe für den SVG Renderer. Die Standardeinstellung ist &quot;200m&quot; (200 MB).

## PS::svgProvider.rootPaths - SVG Data Root Folders {#section-70fe575b0ad54e3b8b6d3a01ea8f1f44}

Der Speicherort der SVG-Quelldatendateien. Es kann sich um einen oder mehrere absolute Dateipfade oder Pfade handeln, die relativ zu *[!DNL install_folder]* sind und durch Semikolons getrennt sind. Wird normalerweise auf denselben Wert wie `IS::RootPath` gesetzt.

## PS::svgProvider.SVGFileSizeLimit - Maximale SVG-Dateigröße {#section-b9c81e3e104642ebbdd9f000843d3256}

Maximale SVG-Quelldateigröße in kBytes. Der Server gibt einen Fehler zurück, wenn versucht wird, eine SVG-Datei zu rendern, die diese Grenze überschreitet. Der Standardwert ist 1024 KB.

## IS::SvgMAxRenderRgnPixels - SVG Output Image Size Limit {#section-5be1fd9639424d878a5ffd11736d3920}

Dadurch wird die Größe der Bilder begrenzt, die SVGRender erstellen kann. Ganzzahlwert größer als 0 in Millionen von Pixeln. Wenn ein Rendervorgang die Größenbeschränkung überschreiten würde, wird ein Fehler zurückgegeben. Der Standardwert ist 4.

## PS::svgProvider.port - [!DNL Platform Server] Listening Port {#section-f7e42a96c2dd4523b46f0557c239e659}

Der für SvgRender verwendete Port zum Abrufen von Bildern aus dem [!DNL Platform Server], die in SVG-Renderings eingebettet werden sollen.

Wichtig Für die ordnungsgemäße Funktionsweise der SVGRender-Komponente muss diese Konfigurationsoption auf denselben Wert wie `TC::PsPort` gesetzt werden.

## PS::svgProvider.fontRoot - SVG Font Files Folder {#section-a8d45b0d68504945b8780f5eac351b0d}

Gibt an, wo der SvgRender die Schriftartendateien findet, die zum Rendern von SVG-Text erforderlich sind; normalerweise einer der in `IS::RootPaths` angegebenen Pfade. Der Standardwert ist [!DNL *[!DNL install_folder]*/images].

## SVG::SVGRender.port, IS::SVGTcpPort - SVG Communications Port {#section-608687123aa644b7b58fe42385d71b79}

Konfiguriert den Port, an dem der Image-Server und die SVGRender-Komponente kommunizieren.

>[!NOTE]
>
>Damit die SVGRender-Komponente ordnungsgemäß funktioniert, muss dieselbe Portnummer für `SVG::SVGRender.port` und `IS::SVGTcpPort` angegeben werden.
