---
description: 'Bilddaten werden zurückgegeben, wenn eine Anfrage erfolgreich abgeschlossen wurde und die Anfrage entweder keinen req= -Befehl enthält oder wenn req= einen der folgenden Werte hat: img, debug.'
solution: Experience Manager
title: Bilder
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 089aaf9d-f414-4ca4-9d6d-7f429de2531e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 1%

---

# Bilder{#images}

Bilddaten werden zurückgegeben, wenn eine Anfrage erfolgreich abgeschlossen wurde und die Anfrage entweder keinen req= -Befehl enthält oder wenn req= einen der folgenden Werte aufweist: img, debug

Der MIME-Typ der HTTP-Antwort wird von `fmt=` bestimmt. Wenn `fmt=` nicht angegeben ist, hängt er vom Wert von `attribute::Format` ab.

Der HTTP-Antwortstatus lautet &quot;200 OK&quot;, wenn die Anforderungsmethode eine unbedingte `GET` oder `HEAD` war.

Der Server kann mit dem Status &#39;304&#39; (nicht geändert) antworten und keine Bilddaten aufgrund einer bedingten `GET`-Anfrage zurückgeben (wobei das Feld [!DNL If-Modified-Since] im Feld `request-header` vorhanden ist).
