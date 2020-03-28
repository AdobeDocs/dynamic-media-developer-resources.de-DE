---
description: Festlegen oder Aktualisieren des Veröffentlichungsstatus für ein oder mehrere Assets Sie können für jeden Veröffentlichungskontext in einer Firma separate Veröffentlichungsstatus festlegen.
seo-description: Festlegen oder Aktualisieren des Veröffentlichungsstatus für ein oder mehrere Assets Sie können für jeden Veröffentlichungskontext in einer Firma separate Veröffentlichungsstatus festlegen.
seo-title: setAssetsContextState
solution: Experience Manager
title: setAssetsContextState
topic: Scene7 Image Production System API
uuid: 4b94f9ea-3f7b-45ee-9381-6434f2bc4e31
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setAssetsContextState{#setassetscontextstate}

Festlegen oder Aktualisieren des Veröffentlichungsstatus für ein oder mehrere Assets Sie können für jeden Veröffentlichungskontext in einer Firma separate Veröffentlichungsstatus festlegen.

## Autorisierte Benutzertypen {#section-815eb031f85143278c1560c18c5e3431}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Der Benutzer muss über Lesezugriff verfügen, um das Asset zurückgeben zu können.

## Parameter {#section-009b9006de8e4c16ad657c47f28ace9f}

**Input (setAssetsContextStateParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Benutzen Sie die Firma. |
| ` *`assetsContextHandle`*` | `types:AssetsContextStateUpdateArray` | Ja | Ein Array mit Assets und ihren neuen Veröffentlichungsstatus. |

**Output (setAssetsContexStateReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`successCount`*` | `xsd:int` | Ja | Die Anzahl der Assets wurde erfolgreich geändert. |
| ` *`warningCount`*` | `xsd:int` | Ja | Die Anzahl der Warnungen, die beim Versuch des Vorgangs generiert wurden, Assets zu ändern. |
| ` *`errorCount`*` | `xsd:int` | Ja | Die Anzahl der Fehler, die beim Versuch des Vorgangs generiert wurden, Assets zu ändern. |
| ` *`warningDetailArray`*` | `types:AssetOperationFaultArray` | Nein | Array von Fehlern, die von Assets generiert wurden, wenn der Vorgang versuchte, sie zu ändern. |

## Beispiele {#section-283a073f3cb14bcda5abed863c538aa4}

In diesem Codebeispiel wird der Veröffentlichungsstatus eines Assets mit `NotMarkedForPublish`festgelegt.

**Anforderung**

```java
<setAssetsContextStateParam xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
  <companyHandle>c|301</companyHandle>
  <assetsContextStateUpdateArray>
    <items>
      <assetHandle>a|27007</assetHandle>
      <contextStateUpdateArray>
        <items>
          <contextHandle>pc|3001</contextHandle>
          <publishState>NotMarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3002</contextHandle>
          <publishState>MarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3003</contextHandle>
          <publishState>NotMarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3004</contextHandle>
          <publishState>NotMarkedForPublish</publishState>
        </items>
      </contextStateUpdateArray>
    </items>
    <items>
      <assetHandle>a|27008</assetHandle>
      <contextStateUpdateArray>
        <items>
          <contextHandle>pc|3001</contextHandle>
          <publishState>MarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3002</contextHandle>
          <publishState>NotMarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3003</contextHandle>
          <publishState>NotMarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3004</contextHandle>
          <publishState>MarkedForPublish</publishState>
        </items>
      </contextStateUpdateArray>
    </items>
  </assetsContextStateUpdateArray>
</setAssetsContextStateParam>
```

**Antwort**

```java
<setAssetsContextStateReturn xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04-beta">
  <successCount>8</successCount>
  <warningCount>0</warningCount>
  <errorCount>0</errorCount>
</setAssetsContextStateReturn>
```

