---
title: setAttr.rootElement
description: Legen Sie Attribute auf das FXG-Stammelement fest.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 47bd947f-c078-4fd3-99cb-5ef48ea3e05e
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 2%

---

# setAttr.rootElement{#setattr-rootelement}

Legen Sie Attribute auf das FXG-Stammelement fest.

` setAttr.rootElement={ *[!DNL attributeName]*= *[!DNL attributeValue]*%26 *[!DNL attributeName]*= *[!DNL attributeValue]*}`

Mit diesem Befehl können die Attribute des Stammelements bearbeitet werden.

## Beispiel {#section-2758a6e316c34b99b13b02147e5973bb}

Wenn Sie über das folgende Stammelement verfügen:

`<Graphic version="1.0" viewHeight="692" viewWidth="792" s7:appVersion="1.0.0.11" ai:appVersion="14.0.0.367" d:id="1" xmlns="http://ns.adobe.com/fxg/2008" xmlns:ai="http://ns.adobe.com/ai/2008" xmlns:d="http://ns.adobe.com/fxg/2008/dt" xmlns:s7="http://ns.adobe.com/S7FXG/2008">`

Nach Anwendung des folgenden Befehls:

`setAttr.rootElement={viewHeight=300%26viewWidth=200}`

Das Stammelement wird jetzt wie folgt geändert:

`<Graphic xmlns="http://ns.adobe.com/fxg/2008" xmlns:ai="http://ns.adobe.com/ai/2008" xmlns:d="http://ns.adobe.com/fxg/2008/dt" xmlns:s7="http://ns.adobe.com/S7FXG/2008" ai:appVersion="14.0.0.367" d:id="1" s7:appVersion="1.0.0.11" version="1.0" viewHeight="300" viewWidth="200">`
