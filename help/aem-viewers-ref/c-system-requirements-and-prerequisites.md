---
title: Systemanforderungen für Dynamic Media HTML 5-Viewer
description: Systemanforderungen für Dynamic Media HTML5-Viewer.
solution: Experience Manager
contentOwner: Rick Brough
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: e4543358-92a6-4acc-a8a2-227e1daea722
source-git-commit: 7793e9befcf3050b9f4e12deeffa018d7c91aaf7
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 1%

---

# Systemanforderungen für Dynamic Media HTML 5 Viewer{#system-requirements}

Systemanforderungen für Dynamic Media HTML5-Viewer.

<!-- Updated March 03, 2022 Contact is now Deepa Gupta -->

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

## Serverhardware und -software {#section-05099146f1f0418988c196635110bee6}

<!-- Updated March 03, 2022 Contact is now Deepa Gupta -->

* Adobe Dynamic Media Image Serving 6.7.1 oder höher.
* HTML5-Viewer benötigen SDK-JavaScript-Server-seitige Bibliotheken 3.11.5 oder höher.
* *E-Mail an einen Freund* Social-Funktionen erfordern s7ondemand 5.0.9 oder höher.
* eCatalog-Viewer - [Popup für Infobereich](/help/aem-viewers-ref/c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-infopanelpopup.md) Für die Unterstützung ist Info Server 2.1.8 oder höher erforderlich.
* Für Suchfunktionskomponenten ist s7search 2.3.0 oder höher erforderlich.

## Systemanforderungen der Viewer {#section-cc72b1e209524d038b4d5b92b35e998e}

**Mindestanforderungen an den Client-Browser für Komponenten-Viewer:**

* Unterstützt für die folgenden Betriebssystemversionen oder höher:
   * Microsoft® Windows® 7
   * macOS X 10.12
* Unterstützt in den folgenden Browser-/Plattformversionen oder höher:
   * Android™ OS 4.x
   * BlackBerry® 10 in nativen Browsern. Es wird nur die Videowiedergabe unterstützt.
   * Chrome 82
   * Edge
   * Firefox 77
   * Internet Explorer 11
   * iOS6
   * iPad 2 (nur Safari und Chrome)
   * iPhone 3GS
   * Safari 11
* Internet Explorer wird auf Mobilgeräten nicht unterstützt.
* *PanoramicViewer* wird in den folgenden Browser-/Plattformversionen oder höheren Versionen unterstützt:
   * Android™ 4.4 (nur Smartphones)
   * Chrome 82
   * Edge
   * Firefox 77
   * Internet Explorer 11
   * iOS 10
   * Safari 11
* *Video360Viewer* und *DimensionalViewer* wird in den folgenden Browser-/Plattformversionen oder höheren Versionen unterstützt:
   * Android™ 5 (nur Smartphones)
   * Chrome 82
   * Edge
   * Firefox 77
   * iOS 12
   * Safari 12
* *ZoomVerticalViewer* wird in den folgenden Browser-/Plattformversionen oder höheren Versionen unterstützt:
   * Android™ 4.x
   * Chrome 82
   * Edge
   * Firefox 77
   * Internet Explorer 11
   * iOS 10
   * Safari 11

## Ende der Unterstützung für TLS 1.0 und 1.1 {#tls}

<!-- CQDOC-19433 -->

Ab dem 30. September 2022 stellt Adobe Dynamic Media Viewers die Unterstützung für Folgendes ein:

* TLS (Transport Layer Security) 1.0 und 1.1
* Die folgenden schwachen Chiffren in TLS 1.2:
   * TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA384
   * TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA
   * TLS_RSA_WITH_AES_256_GCM_SHA384
   * TLS_RSA_WITH_AES_256_CBC_SHA256
   * TLS_RSA_WITH_AES_256_CBC_SHA
   * TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA256
   * TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA
   * TLS_RSA_WITH_AES_128_GCM_SHA256
   * TLS_RSA_WITH_AES_128_CBC_SHA256
   * TLS_RSA_WITH_AES_128_CBC_SHA
   * TLS_RSA_WITH_CAMELLIA_256_CBC_SHA
   * TLS_RSA_WITH_CAMELLIA_128_CBC_SHA
   * TLS_ECDHE_RSA_WITH_3DES_EDE_CBC_SHA
   * TLS_RSA_WITH_SDES_EDE_CBC_SHA

## Nicht unterstützte Webbrowser- und Betriebssystemkombinationen für Dynamic Media-Viewer {#browser-os-support}

<!-- CQDOC-19433 -->

Adobe Dynamic Media Viewers unterstützt nicht die folgenden Webbrowser- und Betriebssystemkombinationen:

* Internet Explorer 11 + Windows 7
* Internet Explorer 11 + Windows 8.1
* Internet Explorer 11 + Windows Phone 8.1
* Aktualisierung von Internet Explorer 11 und Windows Phone 8.1
* Safari 6 + iOS 6.0.1
* Safari 7 + iOS 7.1
* Safari 7 + OS X 10.9 - Mavericks
* Safari 8 + iOS 8.4
* Safari 8 + OS X 10.10 Yosemite

<!-- CQDOC-19433 -->

<!-- 
NOTE
Effective September 30, 2018, Adobe Dynamic Media Classic Viewers ended support of Transport Layer Security 1.0 (TLS 1.0). As such, Dynamic Media Classic no longer supports viewers on the following browsers/platforms that support TLS 1.0 (Adobe recommends using TLS 1.2 or later):

* Android™ 2.3.7
* Android™ 4.0.4
* Android™ 4.1.1
* Android™ 4.2.2
* Android™ 4.3
* Internet Explorer 7 on Window Vista®
* Internet Explorer 8 on Windows® XP
* Internet Explorer 8-10 on Windows® 7
* Internet Explorer 10 on Windows® Phone 8.0
* Safari 5.1.9 on Apple OS X 10.6.8
* Safari 6.0.4 on Apple OS X 10.8.4
* Java™ 6u45
* Java™ 7u25
* OpenSSL 0.9.8y
* Baidu January 2015

NOTE
FLASH VIEWERS END-OF-LIFE — Effective January 31, 2017, Adobe Dynamic Media Classic officially ended support for the Flash viewer platform. -->

