---
title: Netzwerk
description: Erfahren Sie, wie Sie mit der Optimierung der Netzwerkbandbreite die Bildqualität, die bereitgestellt wird, an die tatsächliche Netzwerkbandbreite anpassen können.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7df6eeed-1856-40e1-bd5d-8f06efc7f700
TQID: 'https://experienceleague.adobe.com/9odHf3s93xaQyc1WSkXGamAgoQP070p7ItB9HhyT-dQ'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 162
ht-degree: 3%

---

# Netzwerk{#network}

Beim Aktivieren der Netzwerkbandbreite wird die Bildqualität automatisch an die tatsächliche Netzwerkbandbreite angepasst. Bei geringer Netzwerkbandbreite wird [DPR (Device Pixel Ratio, Gerätepixelverhältnis)-](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-dpr.md) automatisch deaktiviert, auch wenn sie bereits aktiviert ist.

Falls gewünscht, kann Ihr Unternehmen die Optimierung der Netzwerkbandbreite auf individueller Bildebene deaktivieren, indem `network=off` an die URL des Bildes angehängt wird.

`network=on|off`

<table id="simpletable_2D23B1B282CD4216AB5BE7E7430D1B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ein|aus </span> </p> </td> 
  <td class="stentry"> <p>Gibt an, ob die Netzwerkbandbreite die Bildqualität anpasst, die basierend auf der tatsächlichen Netzwerkbandbreite bereitgestellt wird (ein), oder ob die Netzwerkbandbreitenoptimierung für keine Bildqualitätsanpassung deaktiviert wird.</p> </td> 
 </tr> 
</table>

Die Netzwerkbandbreitenwerte basieren auf den erkannten Client-seitigen Werten des gebündelten CDN.

## Eigenschaften

Ein Anforderungsattribut. Es hat keine Auswirkung, wenn die Netzwerkbedingungen ausgezeichnet sind.

## Standard

`network=off`

## Beispiel

`https://smartimaging.scene7.com/is/image/ADBE/AdobeStock_409826521?dpr=on,3&network=on`

## Verwandte Themen

[bfc](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bfc.md), [drp](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-dpr.md), [Smart Imaging](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/imaging-faq.html?lang=de)
