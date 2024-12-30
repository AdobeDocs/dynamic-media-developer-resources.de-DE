---
description: Pfad der Datendatei. Relativer Pfad und Name für Nicht-Bilddatendateien, die mit diesem Bild verknüpft sind.
solution: Experience Manager
title: AuxPath
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 55f82596-72f0-48c4-9b3a-f10ea5f610f1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 3%

---

# AuxPath{#auxpath}

Pfad der Datendatei. Relativer Pfad und Name für Nicht-Bilddatendateien, die mit diesem Bild verknüpft sind.

Der Server kombiniert diesen Wert mit dem Attribut::rootPath , um den tatsächlichen Dateipfad zu erstellen. Kann auch ein absoluter Dateipfad sein.

Wird verwendet, um eine Kabinettstil-Datei für ein Kabinettmaterial oder eine Fensterabdeckungs-Stildatei für ein Fensterabdeckungsmaterial anzugeben. Für alle anderen Materialien leer lassen.

## Eigenschaften {#section-4268350054b7421da0ce0327f0731a52}

Text-Zeichenfolgenwert. Wenn angegeben, muss es sich um einen gültigen relativen oder absoluten Dateipfad handeln. Erforderlich für Schrankmaterialien und Fensterabdeckmaterialien. Muss für alle anderen Materialien leer sein.

## Standard {#section-287005c2d8e948fa958f69ba7b90b437}

Keine.

## Verwandte Themen {#section-e1f7a61c00d04a80af28e2e67481ab92}

[attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3) , [catalog::Path](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-path.md#reference-59ebb624250a4965ad1737578a2ab590), [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
