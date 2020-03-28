---
description: In diesem Abschnitt werden die HTTP-Protokollbefehle beschrieben.
seo-description: In diesem Abschnitt werden die HTTP-Protokollbefehle beschrieben.
seo-title: Befehlsreferenz
solution: Experience Manager
title: Befehlsreferenz
topic: Scene7 Image Serving - Image Rendering API
uuid: 72c4ed61-3436-4df5-b586-77808fb1903a
translation-type: tm+mt
source-git-commit: c5bac2c6e3f3a05bf69924072c4305dbd7ba1f4f

---


# Befehlsreferenz{#command-reference}

In diesem Abschnitt werden die HTTP-Protokollbefehle beschrieben.

**Nur** für dynamische Medien in AEM: Neben den grundlegenden Bildeinstellungen, die in der Benutzeroberfläche verfügbar sind, unterstützt AEM [!DNL Dynamic Media] ( [!DNL Adobe Experience Manager]) zahlreiche erweiterte Bildänderungen, die Sie im Feld &quot; **Bildmodifikatoren** &quot;angeben können. Diese Parameter werden unten definiert. Beachten Sie jedoch, dass folgende Funktionen in dynamischen Medien in AEM nicht unterstützt werden.

* Farbkorrekturbefehle: `icc=` und `iccEmbed=`.
* Grundlegende Befehle zum Vorbereiten und Wiedergeben von Text: `text= textAngle= textAttr= textFlowPath= textFlowXPath= textPath=` und `textPs=`.
* Lokale Anpassung, Befehle: `locale=` und `req=xlate`.
* `req=set` ist nicht für die allgemeine Verwendung verfügbar.
* `req=mbrset`
* `req=saveToFile`
* `req=targets`
* `template=`
* Nicht-Core-Dynamic Media-Dienste: SVG, Image Rendering und Web-to-Print.

<!-- Adobe IS command examples website  http://sj1010010254235.corp.adobe.com/iscommands/ -->

Siehe auch &quot;Dynamic Media- [Bildvorgabeoptionen](https://docs.adobe.com/content/help/en/experience-manager-65/assets/dynamic/managing-image-presets.html#image-preset-options) &quot;in der Dokumentation zu AEM 6.5.

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
