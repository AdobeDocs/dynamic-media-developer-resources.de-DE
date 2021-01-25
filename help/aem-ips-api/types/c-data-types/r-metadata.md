---
description: Ein Metadatenfeld, das von searchAssets zurückgegeben wird.
seo-description: Ein Metadatenfeld, das von searchAssets zurückgegeben wird.
seo-title: Metadaten
solution: Experience Manager
title: Metadaten
topic: Dynamic Media Image Production System API
uuid: fb7a0ef8-a16c-41e3-84cf-160602cb284b
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 15%

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

