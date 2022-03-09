---
description: Gibt einen beschnittenen Bereich für ein Bild basierend auf seiner Hintergrundfarbe oder Transparenz zurück.
solution: Experience Manager
title: getAutoCropRect
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e291597a-b863-42dd-88dc-13398b734410
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 15%

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

**Eingabe (getAutoCropRectParam)**

>[!NOTE]
>
>Geben Sie entweder autoColorCropOptions oder autoTransparentCropOptions beim Aufruf dieser Methode an.

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Der Handle für das Unternehmen mit dem Asset, mit dem Sie arbeiten möchten. |
| assetHandle | `xsd:string` | Ja | Der Handle für das Asset, mit dem Sie arbeiten möchten. |
| autoColorCropOptions | `types:AutoColorCropOptions` | Nein | Berechnen Sie das Zuschnittrechteck anhand der Farbe. Siehe [AutoColorCropOptions](../../../types/c-data-types/r-auto-color-crop-options.md#reference-976c3a1f8e47473cae016a4e9e09e4a6). |
| autoTransparentCropOptions | `types:AutoTransparentCropOptions` | Nein | Berechnen Sie das Zuschnittrechteck auf Grundlage der Transparenz. Siehe [AutoTransparentCropOptions](../../../types/c-data-types/r-auto-transparent-crop-options.md#reference-f4460b3bdf814f4c85e4f097ea4e6e2b). |

**Ausgabe (getAutoCropRectReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| xOffset | `xsd:int` | Ja | Die Koordinaten der linken Startpixel des berechneten Zuschnittbereichs. |
| yOffset | `xsd:int` | Ja | Die anfängliche obere Pixelkoordinate des berechneten Zuschnittbereichs. |
| Breite | `xsd:int` | Ja | Breite des berechneten Zuschnittbereichs (in Pixel). |
| Höhe | `xsd:int` | Ja | Höhe des berechneten Zuschnittbereichs (in Pixel). |

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

