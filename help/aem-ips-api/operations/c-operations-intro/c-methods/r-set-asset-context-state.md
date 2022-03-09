---
description: Legen Sie den Veröffentlichungsstatus für ein oder mehrere Assets fest oder aktualisieren Sie ihn. Sie können für jeden Veröffentlichungskontext in einem Unternehmen einen separaten Veröffentlichungsstatus festlegen.
solution: Experience Manager
title: setAssetsContextState
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 28d0a67b-3e36-43fc-800d-17c841dca3a0
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 11%

---

# setAssetsContextState{#setassetscontextstate}

Legen Sie den Veröffentlichungsstatus für ein oder mehrere Assets fest oder aktualisieren Sie ihn. Sie können für jeden Veröffentlichungskontext in einem Unternehmen einen separaten Veröffentlichungsstatus festlegen.

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

**Eingabe (setAssetsContextStateParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Handle mit dem Unternehmen. |
| assetsContextHandle | `types:AssetsContextStateUpdateArray` | Ja | Ein Array von Assets und deren neuen Veröffentlichungsstatus. |

**Ausgabe (setAssetsContextStateReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| successCount | `xsd:int` | Ja | Die Anzahl der Assets, die erfolgreich geändert wurden. |
| warningCount | `xsd:int` | Ja | Die Anzahl der Warnungen, die generiert wurden, wenn der Vorgang versucht hat, Assets zu ändern. |
| errorCount | `xsd:int` | Ja | Die Anzahl der Fehler, die beim Versuch des Vorgangs generiert wurden, Assets zu ändern. |
| warningDetailArray | `types:AssetOperationFaultArray` | Nein | Array von Fehlern, die von Assets generiert wurden, wenn der Vorgang versuchte, sie zu ändern. |

## Beispiele {#section-283a073f3cb14bcda5abed863c538aa4}

In diesem Codebeispiel wird der Veröffentlichungsstatus eines Assets mithilfe von `NotMarkedForPublish`.

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
