---
description: Ein Metadatenfeld, das von searchAssets zurückgegeben wird.
solution: Experience Manager
title: Metadaten
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: 62e3e215-31ea-49fd-937e-d136fdf84aff
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 14%

---

# [!DNL Metadata]{#metadata}

Ein Metadatenfeld, das von searchAssets zurückgegeben wird.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| name | `xsd:string` | Metadatenname. |
| value | `xsd:string` | Metadatenwert. |
| boolVal | `xsd:boolean` | Boolescher Metadatenwert (nur für boolesche Felder). |
| longVal | `xsd:long` | Lange Metadatenwerte (nur für int-typisierte Felder). |
| doubleVal | `xsd:double` | Doppelter Metadatenwert (nur für Felder mit Fließtext). |
| dateVal | `xsd:dateTime` | Datum-Metadatenwert (nur für Felder mit Datentyp ). |
