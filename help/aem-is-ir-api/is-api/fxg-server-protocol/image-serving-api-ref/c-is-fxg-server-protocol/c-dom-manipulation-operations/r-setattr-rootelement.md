---
description: Legen Sie Attribute auf das FXG-Stammelement fest.
seo-description: Legen Sie Attribute auf das FXG-Stammelement fest.
seo-title: setAttr.rootElement
solution: Experience Manager
title: setAttr.rootElement
topic: Scene7 Image Serving - Image Rendering API
uuid: dda16612-57c7-4abe-8aa4-00e599a8ea69
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setAttr.rootElement{#setattr-rootelement}

Legen Sie Attribute auf das FXG-Stammelement fest.

` setAttr.rootElement={ *[!DNL attributeName]*= *[!DNL attributeValue]*%26 *[!DNL attributeName]*= *[!DNL attributeValue]*}`

Mit diesem Befehl können Attribute des Stammelements bearbeitet werden.

## Beispiel {#section-2758a6e316c34b99b13b02147e5973bb}

Wenn wir das folgende Stammelement haben:

`<Graphic version="1.0" viewHeight="692" viewWidth="792" s7:appVersion="1.0.0.11" ai:appVersion="14.0.0.367" d:id="1" xmlns="http://ns.adobe.com/fxg/2008" xmlns:ai="http://ns.adobe.com/ai/2008" xmlns:d="http://ns.adobe.com/fxg/2008/dt" xmlns:s7="http://ns.adobe.com/S7FXG/2008">`

Nach der Anwendung des folgenden Befehls:

`setAttr.rootElement={viewHeight=300%26viewWidth=200}`

Das Stammelement wird jetzt wie folgt geändert:

`<Graphic xmlns="http://ns.adobe.com/fxg/2008" xmlns:ai="http://ns.adobe.com/ai/2008" xmlns:d="http://ns.adobe.com/fxg/2008/dt" xmlns:s7="http://ns.adobe.com/S7FXG/2008" ai:appVersion="14.0.0.367" d:id="1" s7:appVersion="1.0.0.11" version="1.0" viewHeight="300" viewWidth="200">`
