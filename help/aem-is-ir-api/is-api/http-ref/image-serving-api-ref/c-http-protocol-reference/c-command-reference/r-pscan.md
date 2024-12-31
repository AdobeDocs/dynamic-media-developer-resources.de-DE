---
title: pscan
description: Progressiver JPEG-Scan. Progressive JPEG zeigt ein Bild so an, dass zunächst ein unscharfes Bild mit niedriger Bildqualität vollständig angezeigt wird.
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

Progressiver JPEG-Scan. Progressive JPEG zeigt ein Bild so an, dass zunächst ein unscharfes Bild mit niedriger Bildqualität vollständig angezeigt wird. Mit dem Fortfahren des Scannens wird es klarer, da die Bilddaten umfassender heruntergeladen werden. Mit diesem Parameter können Sie festlegen, wie viele Scans erforderlich sind (3, 4 oder 5), damit das gesamte Bild angezeigt wird.

`pscan=auto|3|4|5`

Die tatsächliche Geschwindigkeit jedes Scans hängt von der Übertragungsgeschwindigkeit des Systems des Benutzers und des Computers ab, der die Daten empfängt und dekomprimiert.

`Auto` verwendet die Scaneinstellungen, die von der unabhängigen JPEG-Bibliothek berechnet werden und vom Farbmodell abhängen. Die Werte `3`, `4` `5` der Scan-Einstellung in Adobe Photoshop entsprechen, wenn Sie eine JPEG-Datei als PJPEG (Progressive JPEG) speichern.

Wenn `pscan` nicht festgelegt ist, wird standardmäßig `auto` verwendet.

## Eigenschaften {#section-e36aa3c63a974b969d9e4f43fe5a37ab}

Anforderungsattribut. Wird unabhängig von der aktuellen Ebeneneinstellung angewendet. Wird ignoriert, wenn das Ausgabeformat kein progressives JPEG ist.

## Standard {#section-01948f6cd7a2415091004cd7526436c7}

`pscan=auto`

## Beispiel {#section-d51bc4d0e8a9473786f149cba9540506}

`http://localhost:8080/is/image/demo/bedroom.tif?wid=300&fmt=pjpeg&pscan=4`

## Verwandte Themen {#section-2105c6441d2b42edb15c7abc4e20d7fc}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
