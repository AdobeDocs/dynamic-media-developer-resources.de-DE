---
title: Befehlsreferenz
description: In diesem Abschnitt werden die HTTP-Protokollbefehle beschrieben.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 959cb193-d0b7-4aa9-a747-fa17484f80c7
TQID: 'https://experienceleague.adobe.com/NURaQ7eznu6tyM5IhrlLMxaZ1L38L7t9lHb826jSyfs'
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
source-wordcount: 324
ht-degree: 3%

---

# Befehlsreferenz{#command-reference}

In diesem Abschnitt werden die HTTP-Protokollbefehle beschrieben.

>[!TIP]
>
>Probieren Sie die Vorteile von Dynamic Media-Bildmodifikatoren und der intelligenten Bildbearbeitung mithilfe von Dynamic Media ([_)_](https://snapshot.scene7.com/).
>
> „Momentaufnahme“ ist ein visuelles Demonstrations-Tool, das die Leistungsfähigkeit von Dynamic Media für eine optimierte und dynamische Bildbereitstellung veranschaulicht. Experimentieren Sie mit Testbildern oder Dynamic Media-URLs, um die Ausgabe verschiedener Dynamic Media-Bildmodifikatoren visuell zu beobachten, und optimieren Sie die intelligente Bildbearbeitung auf Folgendes:
>* Dateigröße (mit WebP- und AVIF-Bereitstellung)
>* Netzwerkbandbreite
>* DPR (Device Pixel Ratio)
>
>Um zu erfahren, wie einfach es ist, „Momentaufnahme“ zu verwenden[&#x200B; spielen Sie das Schulungsvideo zu Momentaufnahmen &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-learn/assets/dynamic-media/images/dynamic-media-snapshot.html?lang=en) (3 Minuten und 17 Sekunden).


**Nur für Dynamic Media in Adobe Experience Manager** - Über die grundlegenden Bildeinstellungen, die in der Benutzeroberfläche verfügbar sind, hinaus unterstützt [!DNL Dynamic Media] in AEM ( [!DNL Adobe Experience Manager]) zahlreiche erweiterte Bildänderungen, die Sie im Feld **Bildmodifikatoren“** können. Diese Parameter werden unten definiert. Beachten Sie jedoch, dass die folgenden Funktionen in Dynamic Media in AEM nicht unterstützt werden.

* Befehle zur Farbkorrektur: `icc=` und `iccEmbed=`.
* Grundlegende Vorlagen- und Rendering-Befehle für Text: `text= textAngle= textAttr= textFlowPath= textFlowXPath= textPath=` und `textPs=`.
* Lokalisierungsbefehle: `locale=` und `req=xlate`.
* `req=set` ist nicht für die allgemeine Verwendung verfügbar.
* `req=mbrset`
* `req=saveToFile`
* `req=targets`
* `template=`
* Nicht-Kern-Dynamic Media-Services: SVG, Image Rendering und Web-to-Print.

<!-- Adobe IS command examples website  http://sj1010010254235.corp.adobe.com/iscommands/ -->

Siehe auch Dynamic Media [Bildvorgabenoptionen) in &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/managing-image-presets.html#dynamic) Dokumentation zu AEM 6.5.

* [in eine Linie bringen](r-align.md)
* [anchor](r-anchor.md)
* [bfc](r-bfc.md)
* [BGC](r-bgc.md)
* [bgColor](r-bgcolor.md)
* [blendMode](r-blendmode.md)
* [Cache](r-is-http-cache.md)
* [clipPath](r-clippath.md)
* [clipXPath](r-clipxpath.md)
* [Farbe](r-color-commandref.md)
* [Zuschneiden](r-crop.md)
* [CropPathE](r-croppath.md)
* [defaultImage](r-is-http-defaultimage.md)
* [DPR](r-dpr.md)
* [Ergebnis](r-effect.md)
* [effektmaskieren](r-effectmask.md)
* [ausdehnen](r-extend.md)
* [Anpassen](r-fit.md)
* [leicht schlagen](r-flip.md)
* [fmt](r-is-http-fmt.md)
* [hei](r-is-http-hei.md)
* [ausblenden](r-hide.md)
* [ICC](r-icc.md)
* [iccEmbed](r-iccembed.md)
* [id](r-id.md)
* [imageSet](r-imageset.md)
* [jpegSize](r-jpegsize.md)
* [Schicht](r-layer.md)
* [standort](r-locale.md)
* [Karte](r-map.md)
* [Maske](r-mask.md)
* [Maskenverwendung](r-maskuse.md)
* [Netzwerk](r-network.md)
* [op_blur](r-op-blur.md)
* [op_bright](r-op-brightness.md)
* [op_colorbalance](r-op-colorbalance.md)
* [op_colorize](r-op-colorize.md)
* [op_contrast](r-op-contrast.md)
* [op_growth](r-op-grow.md)
* [op_growthMask](r-op-growmask.md)
* [op_growthMaskR](r-op-growmaskr.md)
* [op_hue](r-op-hue.md)
* [op_invert](r-op-invert.md)
* [op_rauschen](r-op-noise.md)
* [op_Saturation](r-op-saturation.md)
* [op_sharpen](r-op-sharpen.md)
* [op_sum](r-op-usm.md)
* [op_usmR](r-op-usmr.md)
* [OPAC](r-opac.md)
* [Ursprung](r-origin.md)
* [pathAttr](r-pathattr.md)
* [pathEmbed](r-pathembed.md)
* [Perspektive](r-perspective.md)
* [POS](r-pos.md)
* [printRes](r-printres.md)
* [pscan](r-pscan.md)
* [qlt](r-is-http-qlt.md)
* [quanteln](r-is-http-quantize.md)
* [aufrecht](r-rect.md)
* [Erf](r-req/r-req.md)
* [res](r-res.md)
* [resMode](r-is-http-resmode.md)
* [Ring](r-rgn.md)
* [drehen](r-rotate.md)
* [Skala](r-is-http-scale.md)
* [SCL](r-scl.md)
* [Größe](r-size-reference.md)
* [src](r-src.md)
* [Vorlage](r-template.md)
* [Text](r-text.md)
* [textAngle](r-textangle.md)
* [textAttr](r-textattr.md)
* [textFlowPath](r-textflowpath.md)
* [textFlowXPath](r-textflowxpath.md)
* [textPath](r-textpath.md)
* [textPs](r-textps.md)
* [Typ](r-type.md)
* [WID](r-is-http-wid.md)
* [xmpEmbed](r-xmpembed.md)
