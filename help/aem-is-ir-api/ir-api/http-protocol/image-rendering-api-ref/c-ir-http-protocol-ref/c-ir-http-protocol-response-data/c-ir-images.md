---
description: Bilddaten werden zurückgegeben, wenn eine Anforderung erfolgreich abgeschlossen wurde und die Anforderung entweder keinen req=-Befehl enthält oder wenn req= einen der folgenden Werte img enthält, debug
seo-description: Bilddaten werden zurückgegeben, wenn eine Anforderung erfolgreich abgeschlossen wurde und die Anforderung entweder keinen req=-Befehl enthält oder wenn req= einen der folgenden Werte img enthält, debug
seo-title: Bilder
solution: Experience Manager
title: Bilder
uuid: 8e8c5ec9-dc15-4894-b6a1-8e5241f03977
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 1%

---


# Bilder{#images}

Bilddaten werden zurückgegeben, wenn eine Anforderung erfolgreich abgeschlossen wurde und die Anforderung entweder keinen Befehl req= enthält oder wenn req= einen der folgenden Werte aufweist: img, debug

Der MIME-Typ der HTTP-Antwort wird von `fmt=` oder, wenn `fmt=` nicht angegeben ist, vom Wert von `attribute::Format` bestimmt.

Der HTTP-Antwortstatus ist &quot;200 OK&quot;, wenn die Anforderungsmethode ein bedingungsloser `GET` oder `HEAD` war.

Der Server kann mit dem Status &#39;304&#39; (nicht modifiziert) antworten und keine Bilddaten als Antwort auf eine bedingte `GET`-Anforderung zurückgeben (wobei das [!DNL If-Modified-Since]-Feld im `request-header` vorhanden ist).
