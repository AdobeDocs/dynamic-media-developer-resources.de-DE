---
description: Bestimmt, ob ein Asset-Batch zur Veröffentlichung bereit ist.
solution: Experience Manager
title: setAssetsPublishState
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: dce324e4-cf86-4a65-ab00-8cd2bba20f8f
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 11%

---

# setAssetsPublishState{#setassetspublishstate}

Bestimmt, ob ein Asset-Batch zur Veröffentlichung bereit ist.

Dies ist die Batch-Version von [setAssetState](../../../operations/c-operations-intro/c-methods/r-set-asset-publish-state.md#reference-9efc2eeea42348e0b1d5f3d1005c6563).

## Autorisierte Benutzertypen {#section-0804726f683944dbbe9acfc3d35ccf25}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Der Benutzer muss Lese- und Schreibzugriff auf das Asset haben.

## Parameter {#section-3e49d7859f8647b990d75373cc8dbc24}

**Input (setAssetsPublishStateParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Handle des Unternehmens. |
| publishStateUpdateArray | `types:PublishStateUpdateArray` | Ja | Array von Veröffentlichungsstatuswerten für die Assets. |

**Output (setAssetsPublishStateParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| successCount | `xsd:int` | Ja | Die Anzahl der erfolgreich aktualisierten Assets. |
| warningCount | `xsd:int` | Ja | Die Anzahl der Assets, die eine Warnung generiert haben, als der Vorgang versuchte, sie zu aktualisieren. |
| errorCount | `xsd:int` | Ja | Die Anzahl der Assets, die einen Fehler generiert haben, als der Vorgang versuchte, sie zu löschen. |
| warningDetailArray | `types:AssetOperationFaultArray` | Nein | Details zu den Asset-Aktualisierungen, die eine Warnung generiert haben. |
| errorDetailArray | `types:AssetOperationFaultArray` | Nein | Details zu den Asset-Aktualisierungen, die einen Fehler generiert haben. |

## Beispiele {#section-38cfdd3436214a06a1bae16875501d51}

In diesem Codebeispiel wird der Veröffentlichungsstatus eines Assets festgelegt.

**Anfrage**

```java
<element name="setAssetsPublishStateParam">
   <complexType>
      <sequence>
         <element name="companyHandle" type="xsd:string"/>
         <element name="publishStateUpdateArray" type="types:PublishStateUpdateArray"/>
      </sequence>
   </complexType>
</element>
```

**Antwort**

```java
<element name="setAssetsPublishStateReturn">
   <complexType>
      <sequence>
         <element name="successCount" type="xsd:int"/>
         <element name="warningCount" type="xsd:int"/>
         <element name="errorCount" type="xsd:int"/>
         <element name="warningDetailArray"type="types:AssetOperationFaultArray" minOccurs="0"/>
         <element name="errorDetailArray"type="types:AssetOperationFaultArray" minOccurs="0"/>
      </sequence>
   </complexType>
</element>
```
