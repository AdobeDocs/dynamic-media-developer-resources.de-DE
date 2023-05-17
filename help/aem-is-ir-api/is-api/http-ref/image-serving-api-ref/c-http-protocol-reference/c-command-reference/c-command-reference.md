---
title: Befehlsreferenz
description: In diesem Abschnitt werden die HTTP-Protokollbefehle beschrieben.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 959cb193-d0b7-4aa9-a747-fa17484f80c7
source-git-commit: 187de979d7d1f7ce92b7b4c8b7661a787ab6889f
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 6%

---

# Befehlsreferenz{#command-reference}

In diesem Abschnitt werden die HTTP-Protokollbefehle beschrieben.

>[!TIP]
>
>Probieren Sie die Vorteile von Dynamic Media-Bildmodifikatoren und der intelligenten Bildbearbeitung mithilfe von Dynamic Media aus. [_Momentaufnahme_](https://snapshot.scene7.com/).
>
> Snapshot ist ein visuelles Demonstrationswerkzeug, das die Leistungsfähigkeit von Dynamic Media für eine optimierte und dynamische Bildbereitstellung veranschaulicht. Experimentieren Sie mit Testbildern oder Dynamic Media-URLs, um die Ausgabe verschiedener Dynamic Media-Bildmodifikatoren visuell zu beobachten, und optimieren Sie die intelligente Bildbearbeitung für Folgendes:
>* Dateigröße (mit WebP- und AVIF-Bereitstellung)
>* Netzwerkbandbreite
>* DSGVO (Gerätepixelverhältnis)
>
>Um zu erfahren, wie einfach es ist, Snapshot zu verwenden, spielen Sie die [Schulungsvideo zu Momentaufnahmen](https://experienceleague.adobe.com/docs/experience-manager-learn/assets/dynamic-media/images/dynamic-media-snapshot.html?lang=en) (3 Minuten und 17 Sekunden).


**Nur für Dynamic Media in Adobe Experience Manager** - Über die grundlegenden Bildeinstellungen hinaus, die in der Benutzeroberfläche verfügbar sind, [!DNL Dynamic Media] AEM ( [!DNL Adobe Experience Manager]) unterstützt zahlreiche erweiterte Bildänderungen, die Sie im Abschnitt **Bild-Modifikatoren** -Feld. Diese Parameter sind unten definiert. Beachten Sie jedoch, dass die folgende Funktion in Dynamic Media in AEM nicht unterstützt wird.

* Farbkorrekturbefehle: `icc=` und `iccEmbed=`.
* Grundlegende Befehle zum Vorlagen- und Text-Rendering: `text= textAngle= textAttr= textFlowPath= textFlowXPath= textPath=` und `textPs=`.
* Lokalisierungsbefehle: `locale=` und `req=xlate`.
* `req=set` ist nicht für die allgemeine Anwendung verfügbar.
* `req=mbrset`
* `req=saveToFile`
* `req=targets`
* `template=`
* Nicht zum Kerngeschäft gehörende Dynamic Media-Dienste: SVG, Image Rendering und Web-to-Print.

<!-- Adobe IS command examples website  http://sj1010010254235.corp.adobe.com/iscommands/ -->

Siehe auch Dynamic Media [Bildvorgabenoptionen](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/managing-image-presets.html#dynamic) in der Dokumentation zu AEM 6.5.

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
* [fit](r-fit.md)
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
