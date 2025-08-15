---
title: emptyAssetsFromTrash
description: Leert Assets aus dem IPS-Papierkorb.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 36866dc8-6a16-4445-942f-d0ea3c168272
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 6%

---

# emptyAssetsFromTrash{#emptyassetsfromtrash}

Leert Assets aus dem IPS-Papierkorb.

Assets leben im Papierkorb, bis sie manuell geleert werden oder bis sie aus dem Papierkorb herauskommen. Wenn sie manuell geleert werden, leben sie im Papierkorb bis zum nächsten Bereinigungsauftrag (normalerweise nachts), wenn sie schließlich aus dem System bereinigt werden. Wenn sie aus dem Papierkorb entfernt werden, werden die Assets im Rahmen derselben Bereinigungsaktivität bereinigt. Die maximale Wartezeit kann konfiguriert werden (die Standardeinstellung ist 7 Tage).

## Autorisierte Benutzertypen {#section-24dee2bf5f9f4714a64955c80f2803b4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-8e1fb0ee3aae453581e99ef76e298569}

**Eingabe (emptyAssetsFromTrashParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | xsd:string | Ja | Das -Handle an das Unternehmen, dem die Assets gehören. |
| assetHandleArray | Typen:HandleArray | Ja | Das Array von Handles, die die Elemente darstellen, die aus dem Papierkorb geleert werden sollen. |

**Ausgabe (emptyAssetsFromTrashParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| successCount | xsd:Int | Ja | Die Anzahl der Assets, die erfolgreich aus dem Papierkorb geleert wurden. |
| warningCount | xsd:Int | Ja | Die Anzahl der Warnungen, die generiert wurden, wenn versucht wurde, Assets aus dem Papierkorb zu leeren. |
| errorCount | xsd:Int | Ja | Die Anzahl der Fehler, die generiert wurden, als der Vorgang versucht hat, Assets aus dem Papierkorb zu leeren. |
| warningDetailArray | Typen:AssetOperationFaultArray | Nein | Das Array von Details, die mit den Assets verknüpft sind und Warnungen generiert haben, wenn der Vorgang versucht hat, sie aus dem Papierkorb zu leeren. |
| errorDetailArray | Typen:AssetOperationFaultArray | Nein | Das Array von Details, die mit den Assets verknüpft sind und Fehler generiert haben, als der Vorgang versucht hat, sie aus dem Papierkorb zu leeren. |

## Beispiele {#section-6154a873b6c342bf92e2036280cafdcf}

Dieses Codebeispiel verwendet das -Handle des Unternehmens und ein -Asset-Handle-Array, das Handles für die Assets enthält, die aus dem Papierkorb geleert werden sollen.

**Anfrage**

```java
<emptyAssetsFromTrashParam xmlns="http://www.scene7.com/IpsApi/xsd/2023-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandleArray>
      <items>a|942|1|579</items>
      <items>a|943|1|580</items>
   </assetHandleArray>
</emptyAssetsFromTrashParam>
```

**Antwort**

```java
<emptyAssetsFromTrashReturn xmlns="http://www.scene7.com/IpsApi/xsd/2023-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</emptyAssetsFromTrashReturn>
```
