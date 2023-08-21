---
title: Netzwerk
description: Erfahren Sie mehr über die Verwendung der Optimierung der Netzwerkbandbreite, um die Bildqualität anzupassen, die basierend auf der tatsächlichen Netzwerkbandbreite bereitgestellt wird.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
source-git-commit: 347aa2f52bc6433043ba65fc75fe9f7f221e6aa3
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 2%

---

# Netzwerk{#network}

Beim Aktivieren der Netzwerkbandbreite wird die Bildqualität automatisch an die tatsächliche Netzwerkbandbreite angepasst. Bei geringer Netzwerkbandbreite: [DSGVO (Gerätepixelverhältnis)](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-dpr.md) Die Optimierung wird automatisch deaktiviert, auch wenn sie bereits aktiviert ist.

Bei Bedarf kann Ihr Unternehmen die Optimierung der Netzwerkbandbreite auf individueller Bildebene durch Anhängen von `network=off` zur URL des Bildes.

`network=on|off`

<table id="simpletable_2D23B1B282CD4216AB5BE7E7430D1B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> on_off </span> </p> </td> 
  <td class="stentry"> <p>Gibt an, ob die Netzwerkbandbreite die Bildqualität basierend auf der tatsächlichen Netzwerkbandbreite (ein) anpasst oder die Optimierung der Netzwerkbandbreite deaktiviert ist, um die Bildqualität nicht zu ändern.</p> </td> 
 </tr> 
</table>

Die Werte für die DPR- und Netzwerkbandbreite basieren auf den erkannten clientseitigen Werten des gebündelten CDN. Diese Werte sind manchmal ungenau. Beispiel: iPhone5 mit `dpr=2`und iPhone12 mit `dpr=3`, beide zeigen `dpr=2`. Bei hochauflösenden Geräten wird jedoch das Senden von `dpr=2` ist besser als dpr=1 zu senden. Die beste Möglichkeit, diese Ungenauigkeit zu überwinden, besteht jedoch darin, die clientseitige DSGVO zu verwenden, um Ihnen 100 % genaue Werte zu geben. Und es funktioniert für jedes Gerät, ob es sich um Apple oder ein anderes Gerät handelt, das gestartet wurde. Siehe [Verwenden der intelligenten Bildbearbeitung mit dem clientseitigen Gerätepixelverhältnis](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/client-side-dpr.html?lang=en).

## Eigenschaften



## Standard

`network=off`

## Beispiel

`https://smartimaging.scene7.com/is/image/ADBE/AdobeStock_409826521?dpr=on,3&network=on`

## Verwandte Themen

[trp](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-dpr.md), [Intelligente Bildbearbeitung](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/imaging-faq.html?lang=en)