---
description: Ein von SearchAssets zurückgegebenes Metadatenfeld.
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

Ein von SearchAssets zurückgegebenes Metadatenfeld.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| name | `xsd:string` | Name der Metadaten. |
| value | `xsd:string` | Metadatenwert. |
| boolVal | `xsd:boolean` | Boolescher Metadatenwert (nur für Felder mit boolescher Eingabe). |
| longVal | `xsd:long` | Langer Metadatenwert (nur für int-typisierte Felder). |
| doubleVal | `xsd:double` | Doppelter Metadatenwert (nur für schwebende Felder). |
| dateVal | `xsd:dateTime` | Datums-Metadatenwert (nur für Felder vom Typ „Datum„). |
