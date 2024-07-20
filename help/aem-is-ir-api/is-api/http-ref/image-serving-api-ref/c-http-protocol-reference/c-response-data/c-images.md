---
description: Bilddaten werden zurückgegeben, wenn eine Anfrage erfolgreich abgeschlossen wurde und die Anfrage entweder keinen req= -Befehl enthält oder wenn req=img oder req=tmb.
solution: Experience Manager
title: Bilder
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3aa46d48-82eb-4a21-a5e5-b33904b97888
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 1%

---

# Bilder{#images}

Bilddaten werden zurückgegeben, wenn eine Anfrage erfolgreich abgeschlossen wurde und die Anfrage entweder keinen req= -Befehl enthält oder wenn req=img oder req=tmb.

Der MIME-Typ der HTTP-Antwort wird durch `fmt=` bestimmt oder, wenn `fmt=` nicht angegeben ist, durch `<image/jpeg>`.

Der HTTP-Antwortstatus lautet &quot;200 OK&quot;, wenn die Anforderungsmethode eine unbedingte `GET` oder `HEAD` war.

Der Server kann mit dem Status &#39;304&#39; (nicht geändert) antworten und keine Bilddaten als Antwort auf eine bedingte `GET` -Anfrage zurückgeben (die eine gültige `If-Modified-Since` - oder `If-None-Match` -Kopfzeile enthält).
