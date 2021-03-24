---
description: Pfaddaten einbetten. Gibt an, ob in die Vignette eingebettete Photoshop-Pfade in das Antwortbild einbezogen werden sollen.
solution: Experience Manager
title: pathEmbed
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 3%

---


# pathEmbed{#pathembed}

Pfaddaten einbetten. Gibt an, ob in die Vignette eingebettete Photoshop-Pfade in das Antwortbild einbezogen werden sollen.

`pathEmbed=0|1`

## Eigenschaften {#section-be50b6d1ebd14a9c93f80ac338b44bfc}

Anforderungsattribut. Wird ignoriert, wenn die Vignette keine Pfaddaten enthält. Die Pfaddaten werden bei Bedarf auf `wid=` und/oder `hei=` skaliert.

Wird ignoriert, wenn das Ausgabebildformat keine Pfadeinbettung unterstützt. Eine Liste der Ausgabebildformate, die die Pfadeinbettung unterstützen, finden Sie in der Beschreibung von `fmt=`.

## Standard {#section-3be88ed9053b48919ff33af9418078cc}

`pathEmbed=0`, damit keine Pfade in Ausgabebilder einbettet werden.

## Verwandte Themen {#section-4e6151658c384b6f9d0446f55dde7b7f}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c),  [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec),  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)
