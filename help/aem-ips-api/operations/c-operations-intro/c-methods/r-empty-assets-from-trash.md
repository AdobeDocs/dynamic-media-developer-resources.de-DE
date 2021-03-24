---
description: Leert Assets aus dem IPS-Papierkorb.
solution: Experience Manager
title: emptyAssetsFromTrash
feature: Dynamic Media Classic, SDK/API, Asset Management
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 7%

---


# emptyAssetsFromTrash{#emptyassetsfromtrash}

Leert Assets aus dem IPS-Papierkorb.

Assets werden bis zum manuellen Leeren im Papierkorb oder bis zum Verlassen des Papierkorbs gespeichert. Wenn sie manuell geleert werden, leben sie bis zum nächsten Bereinigungsauftrag (normalerweise nachts) im Papierkorb, wenn sie schließlich aus dem System entfernt werden. Wenn die Assets aus dem Papierkorb auslaufen, werden sie im Rahmen derselben Bereinigungs-Aktivität entfernt. Die Zeitüberschreitung ist konfigurierbar (standardmäßig 7 Tage).

## Autorisierte Benutzertypen {#section-24dee2bf5f9f4714a64955c80f2803b4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* &quot;

## Parameter {#section-8e1fb0ee3aae453581e99ef76e298569}

**Input (emptyAssetsFromTrashParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Das Handle der Firma, der die Assets gehören. |
| `*`assetHandleArray`*` | `types:HandleArray` | Ja | Das Array der Griffe, die die Elemente darstellen, die aus dem Papierkorb geleert werden sollen. |

**Output (emptyAssetsFromTrashParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`successCount`*` | `xsd:Int` | Ja | Die Anzahl der Assets, die erfolgreich aus dem Papierkorb geleert wurden. |
| `*`warningCount`*` | `xsd:Int` | Ja | Die Anzahl der Warnungen, die beim Versuch des Vorgangs generiert wurden, Assets aus dem Papierkorb zu leeren. |
| `*`errorCount`*` | `xsd:Int` | Ja | Die Anzahl der Fehler, die beim Versuch des Vorgangs generiert wurden, Assets aus dem Papierkorb zu leeren. |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | Nein | Das Array mit den Details zu den Assets, die Warnungen generiert haben, wenn der Vorgang versuchte, sie aus dem Papierkorb zu leeren. |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | Nein | Das Array mit Details zu den Assets, die Fehler generiert haben, wenn der Vorgang versuchte, sie aus dem Papierkorb zu leeren. |

## Beispiele {#section-6154a873b6c342bf92e2036280cafdcf}

Dieses Codebeispiel verwendet das Handle der Firma und ein Asset-Handle-Array, das Griffe an den Assets enthält, die aus dem Papierkorb geleert werden sollen.

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

