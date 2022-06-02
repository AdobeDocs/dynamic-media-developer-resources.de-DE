---
title: SynthesizeFontStyles
description: Aktivieren Sie synthetisierte Schriftvarianten. Steuert, ob der Server eine Fehlerantwort generieren oder einen fett, kursiv oder fett/kursiv formatierten Schriftstil synthetisieren soll, wenn ein solcher Stil angefordert wird, der jedoch nicht in der Schriftzuordnung zu finden ist.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08f20748-71c7-4b9f-9b45-70352f9abf35
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 3%

---

# SynthesizeFontStyles{#synthesizefontstyles}

Aktivieren Sie synthetisierte Schriftvarianten. Steuert, ob der Server eine Fehlerantwort generieren oder einen fett, kursiv oder fett/kursiv formatierten Schriftstil synthetisieren soll, wenn ein solcher Stil angefordert wird, der jedoch nicht in der Schriftzuordnung zu finden ist.

>[!NOTE]
>
>Die Synchronisierung von Schriftstilen führt häufig zu einer geringeren Qualität bei der Darstellung als bei der Verwendung von tatsächlichen Schriftarten für solche Stile.

## Eigenschaften {#section-3205560a74774ebf9c916b07bd15aca6}

Flag. Legen Sie auf 0 fest, um die Stile für synthetische Schriftarten zu deaktivieren, und auf 1, um sie zu aktivieren.

## Standard {#section-71f94aa65e404d14b441674c040b59e3}

Vererbt von `default::SynthesizeFontStyles` wenn nicht definiert oder leer ist.

## Verwandte Themen {#section-47a79659cc844272b6d5f36c946e12ac}

[Schriftartverweis](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-font-map-reference/c-font-map-reference.md#concept-f81f319d03c646c5a8ef87b3277dd37d)
