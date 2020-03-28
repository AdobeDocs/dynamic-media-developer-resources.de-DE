---
description: Erstellt ein Bildformat.
seo-description: Erstellt ein Bildformat.
seo-title: saveImageFormat
solution: Experience Manager
title: saveImageFormat
topic: Scene7 Image Production System API
uuid: b11ea668-7a82-439c-b16b-909dc86c00a2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# saveImageFormat{#saveimageformat}

Erstellt ein Bildformat.

>[!NOTE]
>
>Der `urlModifier` Feldwert muss aus einer gültigen XML bestehen. Ändern Sie beispielsweise `&` in `&`. Rufen Sie den `urlModfier` Wert über die IPS-Benutzeroberfläche ab.

## Autorisierte Benutzertypen {#section-12c9d8d5933f4692bafb194060b4f882}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameter {#section-b1fc2fe8d606490ba3a2c979ab8bbd78}

**Input (saveImageFormatParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Der Griff zur Firma mit dem Bildformat, mit dem Sie arbeiten möchten. |
| ` *`imageFormatHandle`*` | `xsd:string` | Nein | Bildformat-Handle, das Sie speichern möchten. |
| ` *`name`*` | `xsd:string` | Ja | Name des Bildformats. |
| ` *`urlModifier`*` | `xsd:string` | Ja | Dabei kann es sich um eine beliebige IPS-Protokoll-Abfrage handeln. Die einfachste Methode zum Generieren eines URL-Modifikators besteht darin, einen mit der IPS-Benutzeroberfläche zu erstellen und dann die Abfrage-Zeichenfolge auszuschneiden und einzufügen. |

**Output (saveImageFormatReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`imageFormatHandle`*` | `xsd:string` | Ja | Bearbeiten Sie das Bildformat. |

## Beispiele {#section-c7bd733212ef494297a97093f3af193f}

Dieses Codebeispiel erstellt ein Bildformat. In diesem Beispiel `urlModifier` wurde der Wert in der IPS-Benutzeroberfläche mit einem gültigen HTML-Format bestimmt.

**Anforderung**

```java
<saveImageFormatParam xmlns="http://www.scene7.com/IpsApi/xsd"> 
   <companyHandle>47</companyHandle> 
   <name>My Image Format Name</name> 
   <urlModifier>wid=400&amp;hei=400&amp;fmt=jpeg&amp;qlt=750&amp;op_sharpen=0&amp; 
   resMode=bicub&amp;op_usm=0.0,0.0,0,0&amp;iccEmbed=0 
   </urlModifier> 
</saveImageFormatParam>
```

**Antwort**

```java
<saveImageFormatReturn xmlns="http://www.scene7.com/IpsApi/xsd"> 
   <imageFormatHandle>47|301</imageFormatHandle> 
</saveImageFormatReturn>
```

