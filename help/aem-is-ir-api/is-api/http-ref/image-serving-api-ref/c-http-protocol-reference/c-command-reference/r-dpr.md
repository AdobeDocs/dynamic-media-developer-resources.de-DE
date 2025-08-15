---
title: DPR
description: Das Gerätepixelverhältnis (Device Pixel Ratio, DPR)&mdash;auch als CSS-Pixelverhältnis&mdash;bezeichnet, ist das Verhältnis zwischen den physischen Pixeln und logischen Pixeln eines Geräts.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d64ca9ed-7d8e-4a13-9c9d-acb7de3e31ed
source-git-commit: 63c0e3b494b6d583117dad01643946900855802e
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 2%

---

# DPR{#dpr}

Das Gerätepixelverhältnis (Device Pixel Ratio, DPR), auch als CSS-Pixelverhältnis bezeichnet, ist das Verhältnis zwischen den physischen Pixeln und logischen Pixeln eines Geräts. Insbesondere mit dem Aufkommen von Netzhautbildschirmen wächst die Pixelauflösung moderner Mobilgeräte rasant.

Durch Aktivierung der Optimierung des Gerätepixelverhältnisses wird das Bild in der nativen Bildschirmauflösung gerendert, wodurch es gestochen scharf erscheint.

Derzeit stammt die Pixeldichte der Anzeige aus den CDN-Kopfzeilenwerten von Akamai.

`dpr=off|on,dprValue`

<table id="simpletable_4CB26F72A56D4515B767C303F8E8A1CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> </span> </span> </p> </td> 
  <td class="stentry"> <p>Deaktivieren Sie die DPR-Optimierung auf Ebene der einzelnen Bild-URLs. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> am, dprValue </span> </span> </p> </td> 
  <td class="stentry"> <p>Überschreiben Sie den von der intelligenten Bildbearbeitung erkannten DPR-Wert mit einem benutzerdefinierten Wert (wie von einer beliebigen Client-seitigen Logik oder auf andere Weise erkannt). Der zulässige Wert für dprValue ist eine beliebige Zahl, die größer ist als 0. </p> </td> 
 </tr> 
</table>


Sie können `dpr=on,dprValue` auch dann verwenden, wenn die DPR-Einstellung auf Unternehmensebene deaktiviert ist.

Aufgrund der DPR-Optimierung wird die MaxPix-Breite immer erkannt, wenn das resultierende Bild größer ist als die Dynamic Media-Einstellung für MaxPix, indem das Seitenverhältnis des Bildes beibehalten wird.

| Angeforderte Bildgröße | DPR-Wert | Bereitgestellte Bildgröße |
|-|-|-|
| 816 x 500 | 1 | 816 x 500 |
| 816 x 500 | 2 | 1632 x 1000 |
| 816 x 500 | 3 | 2448 x 1500 |
| 816 x 500 | 4 | 3264 x 2000 |

DPR-Werte basieren auf den erkannten Client-seitigen Werten des gebündelten CDN. Diese Werte sind manchmal ungenau. Zum Beispiel zeigen sowohl iPhone5 mit `dpr=2` als auch iPhone12 mit DPR=3 `dpr=2` an. Bei Geräten mit hoher Auflösung ist es jedoch immer noch besser, `dpr=2` zu senden als `dpr=1`. Die beste Möglichkeit, diese Ungenauigkeit zu überwinden, besteht jedoch darin, das Client-seitige Gerätepixelverhältnis zu verwenden, um 100 % genaue Werte zu erhalten. Und es funktioniert für jedes Gerät, ob es sich um Apple oder ein anderes Gerät handelt, das gestartet wurde. Siehe [Verwenden der intelligenten Bildbearbeitung mit dem Client-seitigen Gerätepixelverhältnis](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/client-side-dpr.html?lang=de).

## Eigenschaften

Ein Anforderungsattribut. Dies hat keine Auswirkung, wenn `dpr` deaktiviert oder `dprValue=1` ist.

## Standard

`dpr=off`


## Beispiel

`https://smartimaging.scene7.com/is/image/ADBE/AdobeStock_409826521?dpr=on,3`


## Verwandte Themen

[bfc](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bfc.md), [network](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-network.md), [Smart Imaging](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/imaging-faq.html?lang=de)
