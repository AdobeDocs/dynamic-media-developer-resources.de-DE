---
description: Leert Assets aus dem IPS-Papierkorb.
solution: Experience Manager
title: emptyAssetsFromTrash
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 36866dc8-6a16-4445-942f-d0ea3c168272
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 7%

---

# emptyAssetsFromTrash{#emptyassetsfromtrash}

Leert Assets aus dem IPS-Papierkorb.

Assets befinden sich im Müll, bis sie manuell geleert werden oder bis sie aus dem Papierkorb auslaufen. Wenn sie manuell geleert werden, befinden sie sich im Papierkorb bis zum nächsten Bereinigungsauftrag (normalerweise nächtlich), wenn sie schließlich aus dem System gelöscht werden. Wenn die Assets aus dem Papierkorb entfernt werden, werden sie im Rahmen derselben Bereinigungsaktivität bereinigt. Die Zeitüberschreitung ist konfigurierbar (standardmäßig 7 Tage).

## Autorisierte Benutzertypen {#section-24dee2bf5f9f4714a64955c80f2803b4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* &quot;

## Parameter {#section-8e1fb0ee3aae453581e99ef76e298569}

**Eingabe (emptyAssetsFromTrashParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Der Handle für das Unternehmen, dem die Assets gehören. |
| `*`assetHandleArray`*` | `types:HandleArray` | Ja | Das Array von Handles, die die Elemente darstellen, die aus dem Papierkorb geleert werden sollen. |

**Ausgabe (emptyAssetsFromTrashParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`successCount`*` | `xsd:Int` | Ja | Die Anzahl der Assets, die erfolgreich aus dem Papierkorb geleert wurden. |
| `*`warningCount`*` | `xsd:Int` | Ja | Die Anzahl der Warnungen, die generiert wurden, wenn der Vorgang versucht hat, Assets aus dem Papierkorb zu löschen. |
| `*`errorCount`*` | `xsd:Int` | Ja | Die Anzahl der Fehler, die beim Versuch erzeugt wurden, Assets aus dem Papierkorb zu leeren. |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | Nein | Das Array von Details, die mit den Assets verknüpft sind, die Warnungen generiert haben, wenn der Vorgang versucht hat, sie aus dem Papierkorb zu löschen. |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | Nein | Das Array von Details, die mit den Assets verknüpft sind, die Fehler generiert haben, wenn der Vorgang versucht hat, sie aus dem Papierkorb zu löschen. |

## Beispiele {#section-6154a873b6c342bf92e2036280cafdcf}

Dieses Codebeispiel verwendet das Handle des Unternehmens und ein Asset-Handle-Array, das Handles zu den Assets enthält, die aus dem Papierkorb geleert werden sollen.

**Anforderung**

```java
<emptyAssetsFromTrashParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandleArray>
      <items>a|942|1|579</items>
      <items>a|943|1|580</items>
   </assetHandleArray>
</emptyAssetsFromTrashParam>
```

**Antwort**

```java
<emptyAssetsFromTrashReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</emptyAssetsFromTrashReturn>
```
