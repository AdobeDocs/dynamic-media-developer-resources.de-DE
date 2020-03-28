---
description: Benennt ein Asset um.
seo-description: Benennt ein Asset um.
seo-title: renameAsset
solution: Experience Manager
title: renameAsset
topic: Scene7 Image Production System API
uuid: f285d7e4-00df-4d90-a05a-71747a4c54cc
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# renameAsset{#renameasset}

Benennt ein Asset um.

>[!NOTE]
>
>Der `renameFiles` Parameter wurde für frühere Versionen nicht mehr unterstützt und aus `renameAsset`entfernt. Der Pfad der virtuellen Datei wird an den Namen des neuen Assets angepasst (unter Beibehaltung der Dateierweiterung), während die physischen Dateipfade nicht betroffen sind. API-Clients müssen Verweise auf diesen Parameter bei der Aktualisierung auf die neue API-Version entfernen.

## Autorisierte Benutzertypen {#section-cc27ad713c6d498b8f056850b20976f4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImpagePortalContribUser`

>[!NOTE]
>
>Der Benutzer muss Lese- und Schreibzugriff auf das Asset haben.

## Parameter {#section-ef95a994106841e0ab346dd4cf672258}

**Eingabe (renameAssetParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Das Handle der Firma, zu der das Asset gehört. |
| ` *`assetHandle`*` | `xsd:string` | Ja | Das Handle für das Asset, das Sie umbenennen möchten. |
| ` *`newName`*` | `xsd:string` | Ja | Der neue Name des Assets. |
| ` *`validateName`*` | `xsd:boolean` | Ja | Wenn der `validateName` Asset-Typ `true` und der Asset-Typ eine eindeutige IPS-ID erfordern, wird der neue Name auf globale Eindeutigkeit geprüft und es wird ein Fehler `renameAsset` ausgegeben, wenn er nicht eindeutig ist. |

**Output (renameAssetReturn)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück. Hinweise zu diesem Element finden Sie in der Beschreibung des `<ns1:validateName>` Elements.

## Beispiele {#section-a0ddffd62bec42e09069f22ceb486f8a}

Dieses Codebeispiel benennt ein Asset um

**Anforderung**

```java
<ns1:renameAssetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24265|1|17061</ns1:assetHandle>
   <ns1:newName>My Newly Renamed Image</ns1:newName>
   <ns1:validateName>true</ns1:validateName>
   <ns1:renameFiles>true</ns1:renameFiles>
</ns1:renameAssetParam>
```

**Antwort**

Keine.
