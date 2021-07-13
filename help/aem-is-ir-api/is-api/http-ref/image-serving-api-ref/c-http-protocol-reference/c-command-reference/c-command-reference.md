---
description: In diesem Abschnitt werden die HTTP-Protokollbefehle beschrieben.
solution: Experience Manager
title: Befehlsreferenz
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 959cb193-d0b7-4aa9-a747-fa17484f80c7
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 10%

---

# Befehlsreferenz{#command-reference}

In diesem Abschnitt werden die HTTP-Protokollbefehle beschrieben.

**Nur für Dynamic Media in AEM**: Neben den grundlegenden Bildeinstellungen, die in der Benutzeroberfläche verfügbar sind, unterstützt  [!DNL Dynamic Media] in AEM (  [!DNL Adobe Experience Manager]) zahlreiche erweiterte Bildänderungen, die Sie im Feld  **Bildmodifikatoren** angeben können. Diese Parameter sind unten definiert. Beachten Sie jedoch, dass die folgende Funktion in Dynamic Media in AEM nicht unterstützt wird.

* Farbkorrekturbefehle: `icc=` und `iccEmbed=`.
* Grundlegende Befehle zum Vorlagen- und Text-Rendering: `text= textAngle= textAttr= textFlowPath= textFlowXPath= textPath=` und `textPs=`.
* Lokalisierungsbefehle: `locale=` und `req=xlate`.
* `req=set` ist nicht für die allgemeine Anwendung verfügbar.
* `req=mbrset`
* `req=saveToFile`
* `req=targets`
* `template=`
* Nicht zum Kerngeschäft gehörende Dynamic Media-Dienste: SVG, Bild-Rendering und Web-to-Print.

<!-- Adobe IS command examples website  http://sj1010010254235.corp.adobe.com/iscommands/ -->

Weitere Informationen finden Sie unter Dynamic Media [Bildvorgabenoptionen](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/managing-image-presets.html#dynamic) in der AEM 6.5-Dokumentation.

* [align](r-align.md)
* [anchor](r-anchor.md)
* [bfc](r-bfc.md)
* [bgc](r-bgc.md)
* [bgColor](r-bgcolor.md)
* [blendMode](r-blendmode.md)
* [cache](r-is-http-cache.md)
* [clipPath](r-clippath.md)
* [clipXPath](r-clipxpath.md)
* [Farbe](r-color-commandref.md)
* [Zuschneiden](r-crop.md)
* [cropPathE](r-croppath.md)
* [defaultImage](r-is-http-defaultimage.md)
* [Effekt](r-effect.md)
* [EffectMask](r-effectmask.md)
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
* [Layer](r-layer.md)
* [standort](r-locale.md)
* [Karte](r-map.md)
* [mask](r-mask.md)
* [maskUse](r-maskuse.md)
* [op_blur](r-op-blur.md)
* [op_brightness](r-op-brightness.md)
* [op_colorbalance](r-op-colorbalance.md)
* [op_colorize](r-op-colorize.md)
* [op_contrast](r-op-contrast.md)
* [op_expand](r-op-grow.md)
* [op_expandMask](r-op-growmask.md)
* [op_expandMaskR](r-op-growmaskr.md)
* [op_hue](r-op-hue.md)
* [op_invert](r-op-invert.md)
* [op_geräusch](r-op-noise.md)
* [op_sättigung](r-op-saturation.md)
* [op_sharpen](r-op-sharpen.md)
* [op_usm](r-op-usm.md)
* [op_usmR](r-op-usmr.md)
* [opac](r-opac.md)
* [origin](r-origin.md)
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
* [drehen](r-rotate.md)
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
* [Typ](r-type.md)
* [wid](r-is-http-wid.md)
* [xmpEmbed](r-xmpembed.md)
