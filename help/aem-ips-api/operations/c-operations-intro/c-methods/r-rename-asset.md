---
description: Benennt ein Asset um.
solution: Experience Manager
title: renameAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: f3fff3c1-1b48-4d86-8a81-f75be00fc329
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 7%

---

# renameAsset{#renameasset}

Benennt ein Asset um.

>[!NOTE]
>
>Die `renameFiles` -Parameter wurde für frühere Versionen nicht mehr unterstützt und aus entfernt `renameAsset`. Der virtuelle Dateipfad wird so geändert, dass er mit dem neuen Asset-Namen übereinstimmt (wobei die Dateierweiterung beibehalten wird), während die physischen Dateipfade nicht betroffen sind. API-Clients müssen beim Aktualisieren auf die neue API-Version Verweise auf diesen Parameter entfernen.

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
| companyHandle | `xsd:string` | Ja | Das Handle des Unternehmens, zu dem das Asset gehört. |
| assetHandle | `xsd:string` | Ja | Das Handle für das Asset, das Sie umbenennen möchten. |
| newName | `xsd:string` | Ja | Der neue Name des Assets. |
| validateName | `xsd:boolean` | Ja | Wenn die Variable `validateName` is `true` und der Asset-Typ eine eindeutige IPS-ID erfordert, wird der neue Name auf globale Eindeutigkeit überprüft und `renameAsset` gibt einen Fehler aus, wenn dieser nicht eindeutig ist. |

**Ausgabe (renameAssetReturn)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück. Siehe Beschreibung der `<ns1:validateName>` -Element mit Einschränkungen zu diesem Element.

## Beispiele {#section-a0ddffd62bec42e09069f22ceb486f8a}

Mit diesem Codebeispiel wird ein Asset umbenannt.

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
