---
description: Erstellt ein Bildformat.
solution: Experience Manager
title: saveImageFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: cafbd715-237b-4454-920e-643f0c84e208
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 10%

---

# saveImageFormat{#saveimageformat}

Erstellt ein Bildformat.

>[!NOTE]
>
>Der Feldwert `urlModifier` muss aus einer gültigen XML bestehen. Ändern Sie beispielsweise `&` in `&`. Rufen Sie den Wert `urlModfier` von der IPS-Benutzeroberfläche ab.

## Autorisierte Benutzertypen {#section-12c9d8d5933f4692bafb194060b4f882}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameter {#section-b1fc2fe8d606490ba3a2c979ab8bbd78}

**Input (saveImageFormatParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Der Handle für das Unternehmen mit dem Bildformat, mit dem Sie arbeiten möchten. |
| imageFormatHandle | `xsd:string` | Nein | Bildformat-Handle, das Sie speichern möchten. |
| name | `xsd:string` | Ja | Name des Bildformats. |
| urlModifier | `xsd:string` | Ja | Dies kann eine beliebige IPS-Protokoll-Abfragezeichenfolge sein. Die einfachste Möglichkeit, einen URL-Modifikator zu generieren, besteht darin, einen mit der IPS-Benutzeroberfläche zu erstellen und dann die Abfragezeichenfolge auszuschneiden und einzufügen. |

**Output (saveImageFormatReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| imageFormatHandle | `xsd:string` | Ja | Umgang mit dem Bildformat. |

## Beispiele {#section-c7bd733212ef494297a97093f3af193f}

Dieses Codebeispiel erstellt ein Bildformat. In diesem Beispiel wurde `urlModifier` durch den Wert in der IPS-Benutzeroberfläche mit einem gültigen HTML-Format bestimmt.

**Anfrage**

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
