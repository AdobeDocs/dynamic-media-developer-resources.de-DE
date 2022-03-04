---
title: Bilder
description: 'Bilddaten werden zurückgegeben, wenn eine Anfrage erfolgreich abgeschlossen wurde und die Anfrage entweder keinen req= -Befehl enthält oder wenn req= einen der folgenden Werte hat: img, debug.'
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 089aaf9d-f414-4ca4-9d6d-7f429de2531e
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 1%

---

# Bilder{#images}

Bilddaten werden zurückgegeben, wenn eine Anfrage erfolgreich abgeschlossen wurde und die Anfrage entweder keinen req= -Befehl enthält oder wenn req= einen der folgenden Werte aufweist: img, debug

Der MIME-Typ der HTTP-Antwort wird durch `fmt=`oder wenn `fmt=` nicht angegeben ist, hängt es vom Wert von `attribute::Format`.

Der HTTP-Antwortstatus lautet &quot;200 OK&quot;, wenn die Anforderungsmethode eine bedingungslose `GET` oder `HEAD`.

Der Server kann mit dem Status &#39;304&#39; (nicht geändert) antworten und keine Bilddaten als Antwort auf eine bedingte `GET` -Anfrage (mit der [!DNL If-Modified-Since] im Feld vorhanden `request-header`).
