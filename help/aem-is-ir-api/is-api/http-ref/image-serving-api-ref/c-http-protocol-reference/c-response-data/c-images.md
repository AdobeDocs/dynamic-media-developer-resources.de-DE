---
description: Bilddaten werden zurückgegeben, wenn eine Anforderung erfolgreich abgeschlossen wurde und die Anforderung entweder keinen Befehl req= enthält oder wenn req=img oder req=tmb.
seo-description: Bilddaten werden zurückgegeben, wenn eine Anforderung erfolgreich abgeschlossen wurde und die Anforderung entweder keinen Befehl req= enthält oder wenn req=img oder req=tmb.
seo-title: Bilder
solution: Experience Manager
title: Bilder
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 715154b6-f9ac-459e-a566-f78a4ca4580d
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 2%

---


# Bilder{#images}

Bilddaten werden zurückgegeben, wenn eine Anforderung erfolgreich abgeschlossen wurde und die Anforderung entweder keinen Befehl req= enthält oder wenn req=img oder req=tmb.

Der MIME-Typ der HTTP-Antwort wird von `fmt=` oder, wenn `fmt=` nicht angegeben ist, von `<image/jpeg>` bestimmt.

Der HTTP-Antwortstatus ist &quot;200 OK&quot;, wenn die Anforderungsmethode ein bedingungsloser `GET` oder `HEAD` war.

Der Server kann mit dem Status &#39;304&#39; (nicht modifiziert) antworten und keine Bilddaten als Antwort auf eine bedingte `GET`-Anforderung (die eine gültige `If-Modified-Since`- oder `If-None-Match`-Kopfzeile enthält) zurückgeben.
