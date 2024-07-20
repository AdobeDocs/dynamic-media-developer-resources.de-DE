---
title: pscan
description: Progressiver JPEG-Scan. Progressives JPEG zeigt ein Bild so an, dass es zunächst ein unscharfes/minderwertiges Foto anzeigt.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1afd3a60-e0b6-47d1-b7e4-98a3145782a2
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 2%

---

# pscan{#pscan}

Progressiver JPEG-Scan. Progressives JPEG zeigt ein Bild so an, dass es zunächst ein unscharfes/minderwertiges Foto anzeigt. Wenn das Scannen fortgesetzt wird, wird es klarer, wenn die Bilddaten umfassender heruntergeladen werden. Mit diesem Parameter können Sie die Anzahl der Prüfungen festlegen, die zum Anzeigen des gesamten Bildes erforderlich sind (3, 4 oder 5).

`pscan=auto|3|4|5`

Die tatsächliche Geschwindigkeit jedes Scans hängt von der Übertragungsgeschwindigkeit des Systems des Benutzers und des Computers ab, der die Daten empfängt und dekomprimiert.

`Auto` verwendet die Scan-Einstellungen, die von der unabhängigen JPEG-Bibliothek berechnet werden und vom Farbmodell abhängen. Die Werte `3`, `4`, `5` entsprechen der Scan-Einstellung, die in Adobe Photoshop beim Speichern einer JPEG-Datei als PJPEG (progressives JPEG) gefunden wird.

Wenn `pscan` nicht gesetzt ist, wird standardmäßig `auto` verwendet.

## Eigenschaften {#section-e36aa3c63a974b969d9e4f43fe5a37ab}

Anforderungsattribut. Gilt unabhängig von der aktuellen Ebeneneinstellung. Wird ignoriert, wenn das Ausgabeformat kein progressives JPEG ist.

## Standard {#section-01948f6cd7a2415091004cd7526436c7}

`pscan=auto`

## Beispiel {#section-d51bc4d0e8a9473786f149cba9540506}

`http://localhost:8080/is/image/demo/bedroom.tif?wid=300&fmt=pjpeg&pscan=4`

## Verwandte Themen {#section-2105c6441d2b42edb15c7abc4e20d7fc}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
