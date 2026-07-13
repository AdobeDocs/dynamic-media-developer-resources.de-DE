---
description: Löscht einen Eigenschaftssatztyp und den zugehörigen Eigenschaftssatz und die zugehörigen Eigenschaften.
solution: Experience Manager
title: deletePropertySetType
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 97ec0f41-794f-4340-b86d-ab07a742d447
TQID: 'https://experienceleague.adobe.com/MslFY4FLpUm0zZRKTL6ZK4-seRyEMbF55r1LRToIFQY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 93
ht-degree: 9%

---

# deletePropertySetType{#deletepropertysettype}

Löscht einen Eigenschaftssatztyp und den zugehörigen Eigenschaftssatz und die zugehörigen Eigenschaften.

Syntax

## Autorisierte Benutzertypen {#section-16a17b4ebf9a4639bdb2784a2e9fe00d}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameter {#section-1c8973f5d35f44b4a6a483a41609e455}

**Input (deletePropertySetTypeParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| typeHandle | `xsd:string` | Ja | Das Handle des Eigenschaftssatztyps, der gelöscht werden soll. |

**Ausgabe (deletePropertySetTypeParam)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-85faa2e3411a4e23aa6489037f7ce078}

Dieses Codebeispiel verwendet das Handle des Typs als Feld in der `deletePropertySetTypeParam`, die an den IPS-Webservice-Server gesendet wird, um den Eigenschaftssatztyp zu löschen.

**Anfrage**

```java
<deletePropertySetTypeParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
</deletePropertySetTypeParam>
```

**Antwort**

Keine.

