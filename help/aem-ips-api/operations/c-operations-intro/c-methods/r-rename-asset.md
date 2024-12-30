---
description: Benennt ein Asset um.
solution: Experience Manager
title: Asset umbenennen
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: f3fff3c1-1b48-4d86-8a81-f75be00fc329
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 6%

---

# Asset umbenennen{#renameasset}

Benennt ein Asset um.

>[!NOTE]
>
>Der `renameFiles`-Parameter wird seit früheren Versionen nicht mehr unterstützt und wurde aus `renameAsset` entfernt. Der virtuelle Dateipfad wird geändert, sodass er dem neuen Asset-Namen entspricht (wobei die Dateierweiterung beibehalten wird), während die physischen Dateipfade nicht betroffen sind. API-Clients müssen Verweise auf diesen Parameter entfernen, wenn sie auf die neue API-Version aktualisieren.

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
| assetHandle | `xsd:string` | Ja | Das Handle des Assets, das Sie umbenennen möchten. |
| newName | `xsd:string` | Ja | Der neue Name des Assets. |
| validateName | `xsd:boolean` | Ja | Wenn der `validateName` `true` ist und der Asset-Typ eine eindeutige IPS-ID erfordert, wird der neue Name auf globale Eindeutigkeit überprüft und gibt `renameAsset` einen Fehler aus, wenn er nicht eindeutig ist. |

**Ausgabe (renameAssetReturn)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück. Einschränkungen für dieses Element finden Sie in der Beschreibung des `<ns1:validateName>`.

## Beispiele {#section-a0ddffd62bec42e09069f22ceb486f8a}

Dieses Code-Beispiel benennt ein Asset um

**Anfrage**

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
