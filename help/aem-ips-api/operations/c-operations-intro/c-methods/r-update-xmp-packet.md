---
description: Legt ein XMP-Metadatenpaket für ein Asset fest oder aktualisiert es.
solution: Experience Manager
title: updateXMPPacket
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 04d85dba-cc86-4069-ab5d-9a5b3fe542c9
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 23%

---

# updateXMPPacket{#updatexmppacket}

Legt ein XMP-Metadatenpaket für ein Asset fest oder aktualisiert es.

Syntax

## Autorisierte Benutzertypen {#section-ee88a759f4774482a4734201a971f610}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalcontribUser`

## Parameter {#section-7a89621d441840faba639746b410a489}

**Eingabe (updateXMPPacketParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Firmengriff. |
| assetHandle | `xsd:string` | Ja | Asset-Handle. |
| compactPacket | `xsd:Base 64 binary` | Ja | [!DNL zlib-compressed] XMP-Paket, das Sie festlegen oder aktualisieren möchten. |

**Ausgabe (updateXMPPacketReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| Erfolg | `xsd:boolean` | Ja | Gibt `true` zurück, wenn das Paket aktualisiert wurde. |

## Beispiele {#section-38b556b94e5044bf97a954519ff6c212}

**Anfrage**

```java
<ns:updateXMPPacketParam>
   <ns:companyHandle>c|680</ns:companyHandle>
   <ns:assetHandle>a|918567</ns:assetHandle>
   <ns:compressedPacket>H4sIAAAAAAAAAAGqAVX+eNqNU9FumzAUfc9XWN5rwTbpUGNBpC3RtpdqU9NOe3XABTRsU9sM8vezMUUp6qQhhDg
+955zfX2djXQUneCWgVG00tAxh6xUZ07dv19GEEwh9ncOP3kC/LrQ5KcAxxlGBUwxSEpPtLUm3NyDBeIdIghISkTuKU3qLwfzAQZkunymD8cvs5
lDOayt7ShCwzDEwzZWukJkt9sh7ESSyEVE5iItGyNpPniJoHHkptBNZxslgcfsrHqbQ7jxTkG8q5VVplbdYiFNPO0tLpRAC41IjNF1YlksGV2v2
6mkskC85YJLa1w8CfGLBH3SFZfFJYfbFXFglldKO+bn/ZpqrFv+xsS519WKO1mX9yyoHppveRXrgWTlxX9qJk0ojHG9eaBP3PtKnNaNRNJkq6lN
C8bO5sugbVa5/4Hnd05blc9y1zmGCCI0zcO50PyK40+q4LbWPt3IqGmykqnONnVgUUYNvsdfOH6wzN6C03OMd6zQb0KpSh3LPyoIWfgNKX1Vz4i
8rx5MSHHyX/D3L1+gMvRUL7NWE+sFH8+TvNxla7tx+8xdjuhqNPERMBaoBAAA=</ns:compressedPacket>
</ns:updateXMPPacketParam>
```

**Antwort**

```java
<updateXMPPacketReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <success>true</success>
</updateXMPPacketReturn>
```
