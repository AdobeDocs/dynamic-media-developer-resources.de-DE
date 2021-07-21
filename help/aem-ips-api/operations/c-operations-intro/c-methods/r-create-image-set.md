---
description: Erstellt ein Bildset.
solution: Experience Manager
title: createImageSet
feature: Dynamic Media Classic,SDK/API,Bildsets
role: Developer,Admin
exl-id: 01ccc705-97e4-4e75-a322-e24bb78cb496
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 14%

---

# createImageSet{#createimageset}

Erstellt ein Bildset.

Syntax

## Autorisierte Benutzertypen {#section-58bf5027e6d24ab5a9fcba59776d15dc}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Der Benutzer muss Lese-/Schreibzugriff auf den Zielordner haben.

## Parameter {#section-03d22ba7d290477e91c25ca1d4439200}

**Eingabe (createImageSetParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Das Handle des Unternehmens, zu dem das Bildset gehört. |
| `*`folderHandle`*` | `xsd:string` | Ja | Der Handle zum Ordner. |
| `*`name`*` | `xsd:string` | Ja | Name des Bildsets. |
| `*`type`*` | `xsd:string` | Ja | Bildset-Typ. |
| `*`thumbAssetHandle`*` | `xsd:string` | Nein | Handle des Assets, das als Miniaturansicht für das neue Bildset dient. Wenn kein Wert angegeben ist, versucht IPS, das erste Bild-Asset zu verwenden, auf das vom Set verwiesen wird. |

**Ausgabe**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`assetHandle`*` | `xsd:string` | Ja | Der Griff zum neuen Bildset. |

## Beispiele {#section-385fe3b0af8044b0a2451336ec137fc5}

In diesem Codebeispiel wird ein Bildset erstellt, das nach Unternehmen, Ordner, Name und Typ angegeben ist. Die Antwort ist ein Asset-Handle des neu erstellten Bildsets.

**Anforderung**

```java
<ns1:createImageSetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/eCatalogs/</ns1:folderHandle>
   <ns1:name>My Image Set</ns1:name>
   <ns1:type>ImageSet</ns1:type>
</ns1:createImageSetParam>
```

**Antwort**

```java
<createImageSetReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <assetHandle>25741|22|841</assetHandle>
</createImageSetReturn>
```
