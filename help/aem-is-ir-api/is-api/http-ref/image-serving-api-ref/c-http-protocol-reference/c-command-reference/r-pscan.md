---
description: Progressiver JPEG-Scan. Progressives JPEG zeigt ein Bild so an, dass es zunächst ein verschwommenes/minderwertiges Foto in seiner Gesamtheit anzeigt. Wenn das Scannen fortgesetzt wird, wird es klarer, wenn die Daten des Bildes umfassender heruntergeladen werden. Mit diesem Parameter können Sie festlegen, wie viele Scans (3, 4 oder 5) erforderlich sind, damit das gesamte Bild angezeigt wird.
seo-description: Progressiver JPEG-Scan. Progressives JPEG zeigt ein Bild so an, dass es zunächst ein verschwommenes/minderwertiges Foto in seiner Gesamtheit anzeigt. Wenn das Scannen fortgesetzt wird, wird es klarer, wenn die Daten des Bildes umfassender heruntergeladen werden. Mit diesem Parameter können Sie festlegen, wie viele Scans (3, 4 oder 5) erforderlich sind, damit das gesamte Bild angezeigt wird.
seo-title: pscan
solution: Experience Manager
title: pscan
topic: Dynamic Media Image Serving - Image Rendering API
uuid: c8e1d7a9-679c-437f-aa53-67aca3f40b30
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 1%

---


# pscan{#pscan}

Progressiver JPEG-Scan. Progressives JPEG zeigt ein Bild so an, dass es zunächst ein verschwommenes/minderwertiges Foto in seiner Gesamtheit anzeigt. Wenn das Scannen fortgesetzt wird, wird es klarer, wenn die Daten des Bildes umfassender heruntergeladen werden. Mit diesem Parameter können Sie festlegen, wie viele Scans (3, 4 oder 5) erforderlich sind, damit das gesamte Bild angezeigt wird.

`pscan=auto|3|4|5`

Die tatsächliche Geschwindigkeit jedes Scans hängt von der Übertragungsgeschwindigkeit des Systems des Benutzers und des Computers ab, der die Daten empfängt und dekomprimiert.

`Auto` verwendet die Scan-Einstellungen, die von der unabhängigen JPEG-Bibliothek berechnet werden und vom Farbmodell abhängen. Die Werte von `3`, `4`, `5` entsprechen der Scan-Einstellung, die in Adobe Photoshop gefunden wird, wenn Sie eine JPEG-Datei als PJPEG (Progressives JPEG) speichern.

Wenn `pscan` nicht eingestellt ist, wird standardmäßig `auto` verwendet.

## Eigenschaften {#section-e36aa3c63a974b969d9e4f43fe5a37ab}

Anforderungsattribut. Gilt unabhängig von der aktuellen Ebeneneinstellung. Wird ignoriert, wenn das Ausgabeformat kein progressives JPEG-Format ist.

## Standard {#section-01948f6cd7a2415091004cd7526436c7}

`pscan=auto`

## Beispiel {#section-d51bc4d0e8a9473786f149cba9540506}

`http://localhost:8080/is/image/demo/bedroom.tif?wid=300&fmt=pjpeg&pscan=4`

## Verwandte Themen {#section-2105c6441d2b42edb15c7abc4e20d7fc}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
