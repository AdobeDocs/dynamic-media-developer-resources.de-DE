---
title: Beispiele für RTF-Kodierung
description: Die folgenden Beispiele zeigen ein Beispiel für Textbefehle und deren Auswirkungen auf den Text.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54c35aa7-aa8b-49af-a9ea-4bc704e4eebd
source-git-commit: 9254f7eefe66fcdadef2c7d9efeef11756e3eb59
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 2%

---

# Beispiele für RTF-Kodierung{#rtf-encoding-examples}

Die folgenden Beispiele zeigen ein Beispiel für Textbefehle und deren Auswirkungen auf den Text.

`http://server?fmt=png&size=300,50&bgc=f0f0f0&text=\fs16eight,%20\fs32sixteen,%20\fs60thirty,%20\fs100fifty`

![RTF-Kodierungsbeispiel für ein Bild](assets/rtf01.png)

`http://server?fmt=png&size=300,50&bgc=f0f0f0&text=\fs48normal,%20\b1Bold\b0,%20\i1italic\i0`

![RTF-Kodierungsbeispiel zwei Bilder](assets/rtf02.png)

`http://server?fmt=png&size=300,50&bgc=f0f0f0&text={\fonttbl{\f0\fcharset0%20Arial;}{\f1\fcharset0%20Courier%20New;}{\f2\fcharset0%20Palatino%20Linotype;}}\f0\fs50%20Arial,%20\f1%20Courier,%20\f2%20Palatino`

![RTF-Kodierungsbeispiel: drei Bilder](assets/rtf03.png)

`http://server?fmt=png&size=300,50&bgc=f0f0f0&text={\colortbl%20;\red255\green0\blue0;\red0\green128\blue0;\red0\green0\blue255;}\fs48\cf1red,%20\cf2green,%20\cf3blue`

![RTF-Kodierungsbeispiel vier Bilder](assets/rtf04.png)

`http://server?fmt=png&size=300,50&bgc=f0f0f0&text=top-left&layer=1&sizen=1,1&text=\vertalc\qc%20center&layer=2&sizen=1,1&text=\vertalb\qr%20bottom -right`

![RTF-Kodierungsbeispiel fünf Bilder](assets/rtf05.png)

`http://server?fmt=png&size=300,50&bgc=f0f0f0&text=\fs36normal{\super%20superscript}normal{\sub%20subscript}`

![RTF-Kodierungsbeispiel: sechs Bilder](assets/rtf06.png)

`http://server?fmt=png&size=300,50&bgc=f0f0f0&text=normal{\up20raised}normal{\dn20lowered}`

![RTF-Kodierungsbeispiel für sieben Bilder](assets/rtf07.png)

`http://server?fmt=png&size=300,100&bgc=f0f0f0&text=\fs80F.P.T.V.W.Y.{\fs20(kerning%20on)}\line{\kerning0F.P.T.V.W.Y.}{\fs20(kerning%20off)}`

![RTF-Kodierungsbeispiel Acht Bild](assets/rtf08.png)

`http://server?fmt=png&size=300,50&bgc=f0f0f0&text={\fonttbl{\f0\fmodern\fprq1\fcharset0%20Courier%20New;}}\f0\fs72{\rtlch%20desrever}`

![RTF-Kodierungsbeispiel zehn Bild](assets/rtf09.png)

## Siehe auch {#section-e702276fd0e847779cb75a6ccb92fbc8}

[text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f) , [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767), [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d), [HTTP-Codierung](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7)

<!-- OBSOLETE LINK WITH NO SUITABLE REPLACEMENT , [RTF 1.9.1 Specification](https://interoperability.blob.core.windows.net/files/Archive_References/%5bMSFT-RTF%5d.pdf) -->

