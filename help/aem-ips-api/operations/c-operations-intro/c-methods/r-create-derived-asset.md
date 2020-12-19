---
description: Erstellt ein neues Asset, das von einem vorhandenen primären Quellbild-Asset abgeleitet ist.
seo-description: Erstellt ein neues Asset, das von einem vorhandenen primären Quellbild-Asset abgeleitet ist.
seo-title: createDerivedAsset
solution: Experience Manager
title: createDerivedAsset
topic: Scene7 Image Production System API
uuid: e1f9b690-af34-4da5-a534-c3a8c6b0a8fc
translation-type: tm+mt
source-git-commit: 55015831ed1971a305ddbd8085c95626507355e0
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 8%

---


# createDerivedAsset{#createderivedasset}

Erstellt ein neues Asset, das von einem vorhandenen primären Quellbild-Asset abgeleitet ist.

Syntax

<!--<a id="section_FE43FF204ED644C2AC901AF45982E942"></a>-->

Abgeleitete Assets geben Befehle zum Image-Server-Protokoll an, mit denen die Darstellung des Eigentümerbilds geändert wird. Der abgeleitete Typ `AdjustedView` unterstützt das Anwenden einfacher Änderungen auf ein einzelnes Bild (z. B. durch Angabe eines Zuschnittrahmens), während `LayerView` beim Erstellen einer mehrschichtigen Ansicht hilft, die Text oder zusätzliche Bilder enthalten kann.

Im Gegensatz zu einer Bildkopie (siehe [copyImage](../../../operations/c-operations-intro/c-methods/r-copy-image.md#reference-0785131e690b4ad08be69172023f35d0)) wird ein abgeleitetes Bild mit dem Bild des Eigentümers verknüpft. Durch Änderungen am Bild des Eigentümers werden verknüpfte abgeleitete Assets geändert. Wenn Sie das Eigentümerbild löschen, werden alle zugehörigen abgeleiteten Bilder gelöscht.

## Autorisierte Benutzertypen {#authorized-user-types}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-5a0dde01cff6454da3646ea805c2be1e}

**Input (createDerivedAssetParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Das Handle für die Firma, die das Asset enthält, von dem Sie das neue Asset ableiten werden. |
| ` *`ownerHandle`*` | `xsd:string` | Ja | Das Handle zum primären Bild-Asset, von dem das neue Bild abgeleitet wird. |
| ` *`folderHandle`*` | `xsd:string` | Ja | Das Handle für den Ordner, in dem das neue abgeleitete Asset erstellt wird. |
| ` *`name`*` | `xsd:string` | Ja | Der Name des abgeleiteten Assets. |
| ` *`type`*` | `xsd:string` | Ja | Der Asset-Typ des neuen abgeleiteten Assets: `AdjustedView` oder `LayerView`. |
| ` *`urlModifier`*` | `xsd:string` | Nein | Image Serving- oder Image Rendering-Protokollbefehle wurden mit *vor* der Anforderung oder mit `urlPostApplyModifier` Befehlen angewendet. |
| ` *`urlPostApplyModifier`*` | `xsd:string` | Nein | Für die Befehle zum Image Serving oder Image Rendering wurde *after* auf die Anforderung oder `urlPostApplyModifier`-Befehle angewendet. |

**Output (createDerivedAssetParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`assetHandle`*` | `xsd:string` | Ja | Das Handle für den abgeleiteten Asset. |

## Beispiele {#section-5d5ea893a1ef4edc8b3a396f1936e8c9}

Der Beispielcode erstellt ein abgeleitetes Asset mit einer angepassten Ansicht und `urlModifier` und `urlPostApplyModifier` mit beliebigen Werten. Die Antwort gibt das Handle an das neu abgeleitete Asset zurück.

**Anforderung**

```java
<createDerivedAssetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <ownerHandle>a|943|1|580</ownerHandle>
   <folderHandle>ApiTestCo/</folderHandle>
   <name>ApiDerivedAsset</name>
   <type>AdjustedView</type>
   <urlModifier>modify=this</urlModifier>
   <urlPostApplyModifier>action=awesome</urlPostApplyModifier>
</createDerivedAssetParam>
```

**Antwort**

```java
<createDerivedAssetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <assetHandle>a|944|10|2</assetHandle>
</createDerivedAssetReturn>
```

