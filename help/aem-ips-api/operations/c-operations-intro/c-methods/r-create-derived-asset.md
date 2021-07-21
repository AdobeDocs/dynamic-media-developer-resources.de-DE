---
description: Erstellt ein neues Asset, das von einem vorhandenen Bild-Asset aus der Primärquelle abgeleitet wurde.
solution: Experience Manager
title: createabgeleiteteAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: a3b20a8a-ed0d-40be-9a8c-41ba09b1d724
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 8%

---

# createabgeleiteteAsset{#createderivedasset}

Erstellt ein neues Asset, das von einem vorhandenen Bild-Asset aus der Primärquelle abgeleitet wurde.

Syntax

<!--<a id="section_FE43FF204ED644C2AC901AF45982E942"></a>-->

Abgeleitete Assets geben Image Server-Protokollbefehle an, mit denen die Darstellung des Eigentümerbilds geändert wird. Der abgeleitete Typ `AdjustedView` hilft beim Anwenden einfacher Änderungen an einem einzelnen Bild (z. B. durch Angabe eines Zuschnittrechtecks), während der Typ `LayerView` bei der Erstellung einer Mehrschichtansicht hilft, die Text oder zusätzliche Bilder enthalten kann.

Im Gegensatz zu einer Bildkopie (siehe [copyImage](../../../operations/c-operations-intro/c-methods/r-copy-image.md#reference-0785131e690b4ad08be69172023f35d0)) wird ein abgeleitetes Bild mit seinem Eigentümerbild verknüpft. Änderungen am Bild des Eigentümers ändern verknüpfte abgeleitete Assets. Wenn Sie das Bild des Eigentümers löschen, werden alle zugehörigen abgeleiteten Bilder gelöscht.

## Autorisierte Benutzertypen {#authorized-user-types}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-5a0dde01cff6454da3646ea805c2be1e}

**Eingabe (createabgeleitedAssetParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Der Handle für das Unternehmen, das das Asset enthält, von dem Sie das neue Asset ableiten. |
| `*`ownerHandle`*` | `xsd:string` | Ja | Das Handle zum primären Bild-Asset, von dem das neue Bild abgeleitet wird. |
| `*`folderHandle`*` | `xsd:string` | Ja | Das Handle für den Ordner, in dem das neue abgeleitete Asset erstellt wird. |
| `*`name`*` | `xsd:string` | Ja | Der Name des abgeleiteten Assets. |
| `*`type`*` | `xsd:string` | Ja | Der Asset-Typ des neuen abgeleiteten Assets: `AdjustedView` oder `LayerView`. |
| `*`urlModifier`*` | `xsd:string` | Nein | Image Serving- oder Image Rendering-Protokollbefehle wurden *vor* der Anforderung oder den Befehlen `urlPostApplyModifier` angewendet. |
| `*`urlPostApplyModifier`*` | `xsd:string` | Nein | Image Serving- oder Image Rendering-Protokollbefehle, die *nach* auf die Anforderung oder `urlPostApplyModifier`-Befehle angewendet werden. |

**Ausgabe (createabgeleitedAssetParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`assetHandle`*` | `xsd:string` | Ja | Das Handle für das abgeleitete Asset. |

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
