---
description: Erstellt ein neues Asset, das von einem vorhandenen Primärquellen-Bild-Asset abgeleitet wird.
solution: Experience Manager
title: createDerivedAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: a3b20a8a-ed0d-40be-9a8c-41ba09b1d724
source-git-commit: 67e12fae514341137e4218ea950f34da0d9997f3
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 8%

---

# createDerivedAsset{#createderivedasset}

Erstellt ein neues Asset, das von einem vorhandenen Primärquellen-Bild-Asset abgeleitet wird.

Syntax

<!--<a id="section_FE43FF204ED644C2AC901AF45982E942"></a>-->

Abgeleitete Assets geben Image Server-Protokollbefehle an, die die Darstellung des Bild-Eigentümers ändern. Der abgeleitete `AdjustedView`-Typ hilft beim Anwenden einfacher Änderungen auf ein einzelnes Bild (z. B. durch Angabe eines Zuschnittsrechtecks), während der `LayerView` beim Erstellen einer mehrschichtigen Ansicht hilft, die Text oder zusätzliche Bilder enthalten kann.

Im Gegensatz zu einer Bildkopie (siehe [copyImage](../../../operations/c-operations-intro/c-methods/r-copy-image.md#reference-0785131e690b4ad08be69172023f35d0)) wird ein abgeleitetes Bild mit dem Bild des Eigentümers verknüpft. Durch Änderungen am Besitzerbild werden die zugehörigen abgeleiteten Assets geändert. Durch Löschen des Bild des Inhabers werden alle zugehörigen abgeleiteten Bilder gelöscht.

## Autorisierte Benutzertypen {#authorized-user-types}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-5a0dde01cff6454da3646ea805c2be1e}

**Eingabe (createDerivedAssetParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Das Handle für das Unternehmen, das das Asset enthält, von dem Sie das neue Asset ableiten. |
| ownerHandle | `xsd:string` | Ja | Das Handle für das primäre Bild-Asset, von dem das neue Bild abgeleitet wird. |
| folderHandle | `xsd:string` | Ja | Das Handle für den Ordner, in dem das neue abgeleitete Asset erstellt wird. |
| name | `xsd:string` | Ja | Der Name des abgeleiteten Assets. |
| Typ | `xsd:string` | Ja | Der Asset-Typ des neuen abgeleiteten Assets: `AdjustedView` oder `LayerView`. |
| urlModifier | `xsd:string` | Nein | Protokollbefehle für die Bildbereitstellung oder das Bild-Rendering, *(vor* der Anfrage- oder `urlPostApplyModifier` angewendet wurden. |
| urlPostApplyModifier | `xsd:string` | Nein | Befehle des Image-Serving- oder Image-Rendering-Protokolls, die *nachher* auf die Anfrage oder `urlPostApplyModifier`-Befehle angewendet werden. |

**Ausgabe (createDerivedAssetParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| assetHandle | `xsd:string` | Ja | Das Handle des abgeleiteten Assets. |

## Beispiele {#section-5d5ea893a1ef4edc8b3a396f1936e8c9}

Der Beispiel-Code erstellt ein abgeleitetes Asset mit einer angepassten Ansicht und `urlModifier` und `urlPostApplyModifier` mit beliebigen Werten. Die Antwort gibt das Handle für das neu abgeleitete Asset zurück.

**Anfrage**

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
