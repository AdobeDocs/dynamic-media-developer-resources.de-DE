---
description: Ruft ein XMP-Metadatenpaket für das angegebene Asset ab.
seo-description: Ruft ein XMP-Metadatenpaket für das angegebene Asset ab.
seo-title: getXMPPacket
solution: Experience Manager
title: getXMPPacket
topic: Scene7 Image Production System API
uuid: c4b40e76-a459-4036-ace2-8df202305bf9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getXMPPacket{#getxmppacket}

Ruft ein XMP-Metadatenpaket für das angegebene Asset ab.

Syntax

## Autorisierte Benutzertypen {#section-7cb9c26045214f01b1d6b6948b6c6a18}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-b4075df0e4414b00b961d978d5471db9}

**Input (getXMPPacketParam**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Der Firma-Handle mit dem Paket, das Sie zurückgeben möchten (z.B. `c|656`). |
| ` *`assetHandle`*` | `xsd:string` | Ja | Das Asset, für das das XMP-Paket abgerufen werden soll. |

**Output (getXMPPacketReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`compressionPacket`*` | `xsd:Base 64 binary` | Ja | [!DNL zlib-compressed] XMP-Paket. |

## Beispiele {#section-d681af49122e4ca9bcd04110a2e98e6f}

**Anforderung**

```java
<ns:getXMPPacketParam>
   <ns:companyHandle>c|680</ns:companyHandle>
   <ns:assetHandle>a|918567</ns:assetHandle>
</ns:getXMPPacketParam>
```

**Antwort**

```java
<getXMPPacketReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <compressedPacket>H4sIAAAAAAAAAAGqAVX+eNqNU9FumzAUfc9XWN5rwTbpUGNBpC3RtpdqU9NOe3XABTRsU9sM8vezMUUp6qQhhDg+
      955zfX2djXQUneCWgVG00tAxh6xUZ07dv19GEEwh9ncOP3kC/Lr/AQ5Kc/AxxlGBUwxSEpPtLUm3NyDBeIdIghISkTuKU3qLwfzA/QZkunymD8
      cvs5lDOayt7ShCwzDEwzZWukJkt9sh7ESSyEVE5iItGyNpPniJoHHkptBNZxslgcfsrHqbQ7jxTkG8q5VVplbdYiFNPO0tLpRAC4
      1IjNF1YlksGV2v26mkskC85YJLa1w8CfGLBH3SFZfFJYfbFXFgllKO+bn/ZpqrFv+xsS519WKO1mX9y/yoHppveRXrgWTlxX9qJk0ojHG9eaBP3
      PtKnNaNRNJ kq6lNC8bO5/sugbVa5/4Hnd05blc9y1zmGCCI0zcO50PyK40+q4LbWPt3IqGmykqnONnVgUUYNvsdfOH6wzN6C03OMd6zQb0KpSh
      /3LPyoIWfgNKX1Vz4i8rx5MSHHyX/D3L1+gMvRUL7NWE+sFH8+TvNxla7t+8xdjuhqNPERMBaoBAAA=
   </compressedPacket>
</getXMPPacketReturn>
```

