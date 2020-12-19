---
description: Gibt einen beschnittenen Bereich für ein Bild basierend auf seiner Hintergrundfarbe oder Transparenz zurück.
seo-description: Gibt einen beschnittenen Bereich für ein Bild basierend auf seiner Hintergrundfarbe oder Transparenz zurück.
seo-title: getAutoCropRect
solution: Experience Manager
title: getAutoCropRect
topic: Scene7 Image Production System API
uuid: bb00d89a-5fc4-476f-aa47-3cf69ef99afe
translation-type: tm+mt
source-git-commit: 22b447e66c223126f4e6b91f9a0102e86731c4a4
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 13%

---


# getAutoCropRect{#getautocroprect}

Gibt einen beschnittenen Bereich für ein Bild basierend auf seiner Hintergrundfarbe oder Transparenz zurück.

Syntax

## Autorisierte Benutzertypen {#section-32dfe7bb68764b93ae01e05ff7a7bdd0}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `IpsUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-965d5973b8344d43a74b3e07cf0b7eb3}

**Input (getAutoCropRectParam)**

>[!NOTE]
>
>Geben Sie beim Aufrufen dieser Methode entweder ` *`autoColorCropOptions`*` oder ` *`autoTransparentCropOptions`*` an.

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Der Griff zur Firma mit dem Asset, mit dem Sie arbeiten möchten. |
| ` *`assetHandle`*` | `xsd:string` | Ja | Das Handle des Assets, mit dem Sie arbeiten möchten. |
| ` *`autoColorCropOptions`*` | `types:AutoColorCropOptions` | Nein | Beschneidungsrechteck anhand der Farbe berechnen. Siehe [AutoColorCropOptions](../../../types/c-data-types/r-auto-color-crop-options.md#reference-976c3a1f8e47473cae016a4e9e09e4a6). |
| ` *`autoTransparentCropOptions`*` | `types:AutoTransparentCropOptions` | Nein | Beschneidungsrechteck basierend auf Transparenz berechnen. Siehe [AutoTransparentCropOptions](../../../types/c-data-types/r-auto-transparent-crop-options.md#reference-f4460b3bdf814f4c85e4f097ea4e6e2b). |

**Output (getAutoCropRectReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`xOffset`*` | `xsd:int` | Ja | Die Koordinate der linken Startpixel des berechneten Beschneidungsbereichs. |
| ` *`yOffset`*` | `xsd:int` | Ja | Die Koordinate des ersten Pixels des berechneten Zuschnitts. |
| ` *`width`*` | `xsd:int` | Ja | Breite des berechneten Zuschnitts (in Pixel). |
| ` *`height`*` | `xsd:int` | Ja | Höhe des berechneten Zuschnitts (in Pixel). |

## Beispiele {#section-ba65bd66086d491cad1cea535954ee1f}

**Anforderung**

```java
<getAutoCropRectParam xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31-beta">
  <companyHandle>c|3578</companyHandle>
  <assetHandle>a|3192146</assetHandle>
  <autoColorCropOptions>
    <corner>UpperLeft</corner>
    <tolerance>0.5</tolerance>
  </autoColorCropOptions>
</getAutoCropRectParam>
```

**Antwort**

```java
<getAutoCropRectReturn xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31-beta">
  <xOffset>452</xOffset>
  <yOffset>66</yOffset>
  <width>1271</width>
  <height>1874</height>
</getAutoCropRectReturn>
```

>[!MORELIKETHIS]
>
>* [AutoColorCropOptions](../../../types/c-data-types/r-auto-color-crop-options.md#reference-976c3a1f8e47473cae016a4e9e09e4a6)
>* [AutoTransparentCropOptions](../../../types/c-data-types/r-auto-transparent-crop-options.md#reference-f4460b3bdf814f4c85e4f097ea4e6e2b)

