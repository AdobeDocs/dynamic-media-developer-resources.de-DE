---
description: Stellt fest, ob ein Stapel Assets veröffentlicht werden kann.
seo-description: Stellt fest, ob ein Stapel Assets veröffentlicht werden kann.
seo-title: setAssetsPublishState
solution: Experience Manager
title: setAssetsPublishState
topic: Scene7 Image Production System API
uuid: 2910cd6c-573b-405c-864d-a0136ac5472d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setAssetsPublishState{#setassetspublishstate}

Stellt fest, ob ein Stapel Assets veröffentlicht werden kann.

Dies ist die Stapelversion von [setAssetState](../../../operations/c-operations-intro/c-methods/r-set-asset-publish-state.md#reference-9efc2eeea42348e0b1d5f3d1005c6563).

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
| ` *`companyHandle`*` | `xsd:string` | Ja | Firma Handle. |
| ` *`publishStateUpdateArray`*` | `types:PublishStateUpdateArray` | Ja | Array mit Werten für den Veröffentlichungsstatus der Assets. |

**Output (setAssetsPublishStateParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`successCount`*` | `xsd:int` | Ja | Die Anzahl der erfolgreich aktualisierten Assets. |
| ` *`warningCount`*` | `xsd:int` | Ja | Die Anzahl der Assets, die beim Versuch der Aktualisierung eine Warnung generiert haben. |
| ` *`errorCount`*` | `xsd:int` | Ja | Die Anzahl der Assets, die beim Versuch des Vorgangs, sie zu löschen, einen Fehler generiert haben. |
| ` *`warningDetailArray`*` | `types:AssetOperationFaultArray` | Nein | Details zu den Asset-Aktualisierungen, die eine Warnung generiert haben. |
| ` *`errorDetailArray`*` | `types:AssetOperationFaultArray` | Nein | Details zu den Asset-Aktualisierungen, die einen Fehler generiert haben. |

## Beispiele {#section-38cfdd3436214a06a1bae16875501d51}

In diesem Codebeispiel wird der Veröffentlichungsstatus eines Assets festgelegt.

**Anforderung**

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

