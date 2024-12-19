---
title: pathEmbed
description: Einbetten von Datenpfaden. Gibt an, ob in die Vignette eingebettete Photoshop-Pfade in das Antwortbild aufgenommen werden sollen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 66cc57ef-964e-4062-bb66-efeda15be744
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 2%

---

# pathEmbed{#pathembed}

Einbetten von Datenpfaden. Gibt an, ob in die Vignette eingebettete Photoshop-Pfade in das Antwortbild aufgenommen werden sollen.

`pathEmbed=0|1`

## Eigenschaften {#section-be50b6d1ebd14a9c93f80ac338b44bfc}

Anforderungsattribut. Ignoriert, wenn die Vignette keine Datenpfade enthält. Die Datenpfade werden bei Bedarf auf `wid=` und/oder `hei=` skaliert.

Wird ignoriert, wenn das Ausgabebildformat das Einbetten von Pfaden nicht unterstützt. Unter der Beschreibung von `fmt=` finden Sie eine Liste der Ausgabebildformate, die die Pfadeinbettung unterstützen.

## Standard {#section-3be88ed9053b48919ff33af9418078cc}

`pathEmbed=0`, für keine Einbettung von Pfaden in die Ausgabebilder.

## Verwandte Themen {#section-4e6151658c384b6f9d0446f55dde7b7f}

[Fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c), [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec), [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)
