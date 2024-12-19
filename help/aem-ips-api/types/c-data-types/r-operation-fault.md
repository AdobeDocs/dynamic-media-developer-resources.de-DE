---
description: Detailmeldung, die auf eine der in der CDN-Invalidierungsanfrage angegebenen URLs antwortet.
solution: Experience Manager
title: Betriebsstörung
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e1fa7f66-f9d9-45cd-a9b3-d0ff344b137d
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 5%

---

# [!DNL OperationFault]{#operationfault}

Detailmeldung, die auf eine der in der CDN-Invalidierungsanfrage angegebenen URLs antwortet.

**Unterstützt seit**

4.5.0, Patch 2011-02

## Parameter {#section-cf4b0c923cef4c14869319af73ace58b}

| ** Name** | ** Typ** | ** Beschreibung** |
|---|---|---|
| Code | `xsd:int` | Vom CDN bereitgestellter Fehler-Code |
| Grund | `xsd:string` | Vom CDN bereitgestellte Fehlermeldung |
