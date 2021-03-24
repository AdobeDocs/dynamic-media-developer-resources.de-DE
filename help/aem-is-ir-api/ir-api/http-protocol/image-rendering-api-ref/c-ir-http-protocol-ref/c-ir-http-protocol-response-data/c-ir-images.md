---
description: Bilddaten werden zurückgegeben, wenn eine Anforderung erfolgreich abgeschlossen wurde und die Anforderung entweder keinen req=-Befehl enthält oder wenn req= einen der folgenden Werte img enthält, debug
solution: Experience Manager
title: Bilder
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 1%

---


# Bilder{#images}

Bilddaten werden zurückgegeben, wenn eine Anforderung erfolgreich abgeschlossen wurde und die Anforderung entweder keinen Befehl req= enthält oder wenn req= einen der folgenden Werte aufweist: img, debug

Der MIME-Typ der HTTP-Antwort wird von `fmt=` oder, wenn `fmt=` nicht angegeben ist, vom Wert von `attribute::Format` bestimmt.

Der HTTP-Antwortstatus ist &quot;200 OK&quot;, wenn die Anforderungsmethode ein bedingungsloser `GET` oder `HEAD` war.

Der Server kann mit dem Status &#39;304&#39; (nicht modifiziert) antworten und keine Bilddaten als Antwort auf eine bedingte `GET`-Anforderung zurückgeben (wobei das [!DNL If-Modified-Since]-Feld im `request-header` vorhanden ist).
