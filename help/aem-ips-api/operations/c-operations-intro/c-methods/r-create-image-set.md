---
description: Erstellt einen Bildsatz.
seo-description: Erstellt einen Bildsatz.
seo-title: createImageSet
solution: Experience Manager
title: createImageSet
topic: Scene7 Image Production System API
uuid: 688f3954-bc8f-4687-8d66-e064561cd4a0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# createImageSet{#createimageset}

Erstellt einen Bildsatz.

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

**Input (createImageSetParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Der Griff der Firma, zu der der Bildsatz gehört. |
| ` *`folderHandle`*` | `xsd:string` | Ja | Das Handle zum Ordner. |
| ` *`name`*` | `xsd:string` | Ja | Name des Bildsatzes. |
| ` *`type`*` | `xsd:string` | Ja | Bildsatztyp. |
| ` *`thumbAssetHandle`*` | `xsd:string` | Nein | Handhabung des Assets, das als Miniaturansicht für den neuen Bildsatz fungiert. Ist dies nicht der Fall, versucht IPS, das erste Bild-Asset zu verwenden, auf das der Satz verweist. |

**Ausgabe**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`assetHandle`*` | `xsd:string` | Ja | Der Griff zum neuen Bildsatz. |

## Beispiele {#section-385fe3b0af8044b0a2451336ec137fc5}

In diesem Codebeispiel wird ein Bildsatz erstellt, der nach Firma, Ordner, Name und Typ angegeben wird. Die Antwort ist ein Asset-Handle des neu erstellten Bildsatzes.

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

