---
description: 'Bilddaten werden zurückgegeben, wenn eine Anforderung erfolgreich abgeschlossen wurde und die Anforderung entweder keinen Befehl req= enthält oder wenn req= einen der folgenden Werte hat: img, debug.'
solution: Experience Manager
title: Bilder
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 1%

---


# Bilder{#images}

Bilddaten werden zurückgegeben, wenn eine Anforderung erfolgreich abgeschlossen wurde und die Anforderung entweder keinen Befehl req= enthält oder wenn req= einen der folgenden Werte aufweist: img, debug

Der MIME-Typ der HTTP-Antwort wird von `fmt=` oder, wenn `fmt=` nicht angegeben ist, vom Wert von `attribute::Format` bestimmt.

Der HTTP-Antwortstatus ist &quot;200 OK&quot;, wenn die Anforderungsmethode ein bedingungsloser `GET` oder `HEAD` war.

Der Server kann mit dem Status &#39;304&#39; (nicht modifiziert) antworten und keine Bilddaten als Antwort auf eine bedingte `GET`-Anforderung zurückgeben (wobei das [!DNL If-Modified-Since]-Feld im `request-header` vorhanden ist).
