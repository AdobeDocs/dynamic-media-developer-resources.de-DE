---
description: Bilddaten werden zurückgegeben, wenn eine Anforderung erfolgreich abgeschlossen wurde und die Anforderung entweder keinen req=-Befehl enthält oder wenn req= einen der folgenden Werte img enthält, debug
seo-description: Bilddaten werden zurückgegeben, wenn eine Anforderung erfolgreich abgeschlossen wurde und die Anforderung entweder keinen req=-Befehl enthält oder wenn req= einen der folgenden Werte img enthält, debug
seo-title: Bilder
solution: Experience Manager
title: Bilder
topic: Scene7 Image Serving - Image Rendering API
uuid: 8e8c5ec9-dc15-4894-b6a1-8e5241f03977
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Bilder{#images}

Bilddaten werden zurückgegeben, wenn eine Anforderung erfolgreich abgeschlossen wurde und die Anforderung entweder keinen Befehl req= enthält oder wenn req= einen der folgenden Werte aufweist: img, debug

Der MIME-Typ der HTTP-Antwort wird vom Wert `fmt=`oder, falls `fmt=` nicht angegeben, vom Wert `attribute::Format`der Antwort bestimmt.

Der HTTP-Antwortstatus lautet &quot;200 OK&quot;, wenn die Anforderungsmethode eine nicht bedingte `GET` oder `HEAD`.

Der Server kann mit dem Status &#39;304&#39; (nicht geändert) antworten und keine Bilddaten als Antwort auf eine bedingte `GET` Anforderung (mit dem [!DNL If-Modified-Since] Feld im `request-header`) zurückgeben.
