---
title: dpr
description: Device Pixel Ratio (DPR)&mdash; auch CSS-Pixelverhältnis&mdash genannt; ist die Beziehung zwischen den physischen Pixeln und logischen Pixeln eines Geräts.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
source-git-commit: 21d6aed6baee24922732461fe680f6cc93bd0d06
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 2%

---

# dpr{#dpr}

Device Pixel Ratio (DPR) - auch als CSS-Pixelverhältnis bezeichnet - ist die Beziehung zwischen den physischen Pixeln und logischen Pixeln eines Geräts. Besonders mit der Einführung von Retina-Bildschirmen wächst die Pixelauflösung moderner Mobilgeräte schnell.

Durch Aktivierung der Optimierung des Gerätepixelverhältnisses wird das Bild in der nativen Bildschirmauflösung gerendert, wodurch es scharf wird.

Derzeit stammt die Pixeldichte der Anzeige von Akamai CDN-Kopfzeilenwerten.

`dpr=off|on,dprValue`

<table id="simpletable_4CB26F72A56D4515B767C303F8E8A1CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> off </span> </span> </p> </td> 
  <td class="stentry"> <p>Deaktivieren Sie die DSGVO-Optimierung auf Ebene der einzelnen Bild-URL. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> on, dprValue </span> </span> </p> </td> 
  <td class="stentry"> <p>Überschreiben Sie den von der intelligenten Bildbearbeitung erkannten DPR-Wert mit einem benutzerdefinierten Wert (wie von jeder clientseitigen Logik oder anderen Mitteln erkannt). Der zulässige Wert für dprValue ist eine beliebige Zahl größer als 0. </p> </td> 
 </tr> 
</table>


Sie können `dpr=on,dprValue` selbst wenn die DSGVO auf Unternehmensebene deaktiviert ist.

Aufgrund der DSGVO-Optimierung wird die MaxPix-Breite immer erkannt, wenn das resultierende Bild größer ist als die MaxPix-Dynamic Media-Einstellung, indem das Seitenverhältnis des Bildes beibehalten wird.

| Angeforderte Bildgröße | DPR-Wert | Ausgelieferte Bildgröße |
|-|-|-|
| 816 x 500 | 1 | 816 x 500 |
| 816 x 500 | 2 | 1632 x 1000 |
| 816 x 500 | 3 | 2448 x 1500 |
| 816 x 500 | 4 | 3264 x 2000 |

Die DPR-Werte basieren auf den erkannten clientseitigen Werten des gebündelten CDN. Diese Werte sind manchmal ungenau. Beispiel: iPhone5 mit `dpr=2`und iPhone12 mit dpr=3, zeigen beide `dpr=2`. Bei hochauflösenden Geräten wird jedoch das Senden von `dpr=2` ist besser als Senden `dpr=1`. Die beste Möglichkeit, diese Ungenauigkeit zu überwinden, besteht jedoch darin, die clientseitige DSGVO zu verwenden, um Ihnen 100 % genaue Werte zu geben. Und es funktioniert für jedes Gerät, ob es sich um Apple oder ein anderes Gerät handelt, das gestartet wurde. Siehe [Verwenden der intelligenten Bildbearbeitung mit dem clientseitigen Gerätepixelverhältnis](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/client-side-dpr.html?lang=en).

## Eigenschaften



## Standard

`dpr=off`


## Beispiel

`https://smartimaging.scene7.com/is/image/ADBE/AdobeStock_409826521?dpr=on,3`


## Verwandte Themen

[bfc](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bfc.md), [network](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-network.md), [Intelligente Bildbearbeitung](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/imaging-faq.html?lang=en)