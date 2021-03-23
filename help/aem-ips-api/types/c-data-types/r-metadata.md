---
description: Ein Metadatenfeld, das von searchAssets zurückgegeben wird.
seo-description: Ein Metadatenfeld, das von searchAssets zurückgegeben wird.
seo-title: Metadaten
solution: Experience Manager
title: Metadaten
uuid: fb7a0ef8-a16c-41e3-84cf-160602cb284b
feature: Dynamic Media Classic, SDK/API, Metadaten
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 13%

---


# Metadaten{#metadata}

Ein Metadatenfeld, das von searchAssets zurückgegeben wird.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| `*`name`*` | `xsd:string` | Metadatenname. |
| `*`Wert`*` | `xsd:string` | Metadatenwert. |
| `*`boolVal`*` | `xsd:boolean` | Boolescher Metadatenwert (nur für boolesche Felder). |
| `*`longVal`*` | `xsd:long` | Wert für lange Metadaten (nur für Felder mit int-Typ). |
| `*`doubleVal`*` | `xsd:double` | Metadatenwert der Dublette (nur für Felder mit Fließkomma-Typ). |
| `*`dateVal`*` | `xsd:dateTime` | Datumsmetadatenwert (nur für datentypisierte Felder). |

