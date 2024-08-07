---
title: Netzwerk
description: Erfahren Sie mehr über die Verwendung der Optimierung der Netzwerkbandbreite, um die Bildqualität anzupassen, die basierend auf der tatsächlichen Netzwerkbandbreite bereitgestellt wird.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7df6eeed-1856-40e1-bd5d-8f06efc7f700
source-git-commit: 63c0e3b494b6d583117dad01643946900855802e
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 4%

---

# Netzwerk{#network}

Beim Aktivieren der Netzwerkbandbreite wird die Bildqualität automatisch an die tatsächliche Netzwerkbandbreite angepasst. Bei geringer Netzwerkbandbreite wird die Optimierung von [DPR (Device Pixel Ratio)](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-dpr.md) automatisch deaktiviert, auch wenn sie bereits aktiviert ist.

Falls gewünscht, kann Ihr Unternehmen die Optimierung der Netzwerkbandbreite auf individueller Bildebene deaktivieren, indem es `network=off` an die URL des Bildes anhängt.

`network=on|off`

<table id="simpletable_2D23B1B282CD4216AB5BE7E7430D1B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> on|off </span> </p> </td> 
  <td class="stentry"> <p>Gibt an, ob die Netzwerkbandbreite die Bildqualität basierend auf der tatsächlichen Netzwerkbandbreite (ein) anpasst oder die Optimierung der Netzwerkbandbreite deaktiviert ist, um die Bildqualität nicht zu ändern.</p> </td> 
 </tr> 
</table>

Netzwerkbandbreitenwerte basieren auf den erkannten clientseitigen Werten des gebündelten CDN.

## Eigenschaften

Ein Anfrageattribut. Es hat keine Auswirkung, wenn die Netzwerkbedingungen ausgezeichnet sind.

## Standard

`network=off`

## Beispiel

`https://smartimaging.scene7.com/is/image/ADBE/AdobeStock_409826521?dpr=on,3&network=on`

## Verwandte Themen

[bfc](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bfc.md), [drp](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-dpr.md), [Smart Imaging](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/imaging-faq.html?lang=en)
