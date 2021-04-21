---
description: In diesem Abschnitt werden die HTTP-Protokollbefehle beschrieben.
solution: Experience Manager
title: Befehlsreferenz
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 10%

---


# Befehlsreferenz{#command-reference}

In diesem Abschnitt werden die HTTP-Protokollbefehle beschrieben.

**Nur für Dynamic Media in AEM**: Neben den grundlegenden Bildeinstellungen, die auf der Benutzeroberfläche verfügbar sind, unterstützt AEM  [!DNL Dynamic Media] in (  [!DNL Adobe Experience Manager]) zahlreiche erweiterte Bildänderungen, die Sie im Feld  **Bildmodifikatoren** angeben können. Diese Parameter werden unten definiert. Beachten Sie jedoch, dass folgende Funktionen in Dynamic Media in AEM nicht unterstützt werden.

* Farbkorrekturbefehle: `icc=` und `iccEmbed=`.
* Grundlegende Befehle zum Vorbereiten und Wiedergeben von Text: `text= textAngle= textAttr= textFlowPath= textFlowXPath= textPath=` und `textPs=`.
* lokale Anpassung, Befehle: `locale=` und `req=xlate`.
* `req=set` ist nicht für die allgemeine Verwendung verfügbar.
* `req=mbrset`
* `req=saveToFile`
* `req=targets`
* `template=`
* Nicht-Core-Dynamic Media-Dienste: SVG, Image Rendering und Web-to-Print.

<!-- Adobe IS command examples website  http://sj1010010254235.corp.adobe.com/iscommands/ -->

Siehe auch Dynamic Media [Bildvorgabeoptionen](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/managing-image-presets.html#dynamic) in der Dokumentation zu AEM 6.5.

* [align](r-align.md)
* [anchor](r-anchor.md)
* [bfc](r-bfc.md)
* [bgc](r-bgc.md)
* [bgColor](r-bgcolor.md)
* [blendMode](r-blendmode.md)
* [cache](r-is-http-cache.md)
* [clipPath](r-clippath.md)
* [clipXPath](r-clipxpath.md)
* [color](r-color-commandref.md)
* [Zuschneiden](r-crop.md)
* [cutPathE](r-croppath.md)
* [defaultImage](r-is-http-defaultimage.md)
* [effect](r-effect.md)
* [effectMask](r-effectmask.md)
* [erweitern](r-extend.md)
* [anpassen](r-fit.md)
* [flip](r-flip.md)
* [fmt](r-is-http-fmt.md)
* [hei](r-is-http-hei.md)
* [ausblenden](r-hide.md)
* [icc](r-icc.md)
* [iccEmbed](r-iccembed.md)
* [id](r-id.md)
* [imageSet](r-imageset.md)
* [jpegSize](r-jpegsize.md)
* [layer](r-layer.md)
* [locale](r-locale.md)
* [Karte](r-map.md)
* [Maske](r-mask.md)
* [maskUse](r-maskuse.md)
* [op_blur](r-op-blur.md)
* [op_brightness](r-op-brightness.md)
* [op_colorbalance](r-op-colorbalance.md)
* [op_colorize](r-op-colorize.md)
* [op_stroke](r-op-contrast.md)
* [op_large](r-op-grow.md)
* [op_largeMask](r-op-growmask.md)
* [op_largeMaskR](r-op-growmaskr.md)
* [op_hue](r-op-hue.md)
* [op_invert](r-op-invert.md)
* [op_geräusch](r-op-noise.md)
* [op_Saturation](r-op-saturation.md)
* [op_sharpen](r-op-sharpen.md)
* [op_usm](r-op-usm.md)
* [op_usmR](r-op-usmr.md)
* [opac](r-opac.md)
* [Herkunft](r-origin.md)
* [pathAttr](r-pathattr.md)
* [pathEmbed](r-pathembed.md)
* [Perspektive](r-perspective.md)
* [pos](r-pos.md)
* [printRes](r-printres.md)
* [pscan](r-pscan.md)
* [qlt](r-is-http-qlt.md)
* [quantifizieren](r-is-http-quantize.md)
* [rect](r-rect.md)
* [req](r-req/r-req.md)
* [res](r-res.md)
* [resMode](r-is-http-resmode.md)
* [rgn](r-rgn.md)
* [rotate](r-rotate.md)
* [scale](r-is-http-scale.md)
* [scl](r-scl.md)
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
* [type](r-type.md)
* [wid](r-is-http-wid.md)
* [xmpEmbed](r-xmpembed.md)
