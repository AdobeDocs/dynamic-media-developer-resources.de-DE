---
description: Legt fest, ob ein Asset-Batch zur Veröffentlichung bereit ist.
solution: Experience Manager
title: setAssetsPublishState
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: dce324e4-cf86-4a65-ab00-8cd2bba20f8f
TQID: 'https://experienceleague.adobe.com/VV11khRodimEOAdPB-6mHR-gIT4AMiKOKeuuH6J15VA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: null
workflow-type: tm+mt
source-wordcount: 151
ht-degree: 11%

---

# setAssetsPublishState{#setassetspublishstate}

Legt fest, ob ein Asset-Batch zur Veröffentlichung bereit ist.

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

**Eingabe (setAssetsPublishStateParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Firmengriff. |
| publishStateUpdateArray | `types:PublishStateUpdateArray` | Ja | Array von Werten des Veröffentlichungsstatus für die Assets. |

**Ausgabe (setAssetsPublishStateParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| successCount | `xsd:int` | Ja | Die Anzahl der erfolgreich aktualisierten Assets. |
| warningCount | `xsd:int` | Ja | Die Anzahl der Assets, die eine Warnung generiert haben, als der Vorgang versucht hat, sie zu aktualisieren. |
| errorCount | `xsd:int` | Ja | Die Anzahl der Assets, die einen Fehler erzeugt haben, als der Vorgang versucht hat, sie zu löschen. |
| warningDetailArray | `types:AssetOperationFaultArray` | Nein | Details zu den Asset-Aktualisierungen, die eine Warnung generiert haben. |
| errorDetailArray | `types:AssetOperationFaultArray` | Nein | Details, die mit den Asset-Aktualisierungen verknüpft sind, die einen Fehler verursacht haben. |

## Beispiele {#section-38cfdd3436214a06a1bae16875501d51}

Dieses Code-Beispiel legt den Veröffentlichungsstatus eines Assets fest.

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
