---
description: Erstellt ein Bildset.
solution: Experience Manager
title: createImageSet
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: 01ccc705-97e4-4e75-a322-e24bb78cb496
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 13%

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
>Die Benutzerin bzw. der Benutzer muss Lese-/Schreibzugriff auf den Zielordner haben.

## Parameter {#section-03d22ba7d290477e91c25ca1d4439200}

**Input (createImageSetParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Das Handle für das Unternehmen, zu dem das Bildset gehört. |
| folderHandle | `xsd:string` | Ja | Der Handle zum Ordner. |
| name | `xsd:string` | Ja | Name des Bildsets. |
| Typ | `xsd:string` | Ja | Typ des Bildsets. |
| thumbAssetHandle | `xsd:string` | Nein | Handle des Assets, das als Miniatur für das neue Bildset fungiert. Wenn kein Wert angegeben ist, versucht IPS, das erste Bild-Asset zu verwenden, auf das vom Set verwiesen wird. |

**Ausgabe**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| assetHandle | `xsd:string` | Ja | Der Ziehpunkt zum neuen Bildset. |

## Beispiele {#section-385fe3b0af8044b0a2451336ec137fc5}

Dieses Codebeispiel erstellt ein Bildset, das durch Firma, Ordner, Name und Typ angegeben wird. Die Antwort ist ein Asset-Handle des neu erstellten Bildsets.

**Anfrage**

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
