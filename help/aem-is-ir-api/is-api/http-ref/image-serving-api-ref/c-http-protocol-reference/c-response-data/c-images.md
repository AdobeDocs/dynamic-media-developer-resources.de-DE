---
description: Bilddaten werden zurückgegeben, wenn eine Anfrage erfolgreich abgeschlossen wurde und die Anfrage entweder keinen Befehl req=oder req=img oder req=tmb enthält.
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

Bilddaten werden zurückgegeben, wenn eine Anfrage erfolgreich abgeschlossen wurde und die Anfrage entweder keinen Befehl req=oder req=img oder req=tmb enthält.

Der MIME-Typ der HTTP-Antwort wird durch `fmt=` bestimmt oder, wenn `fmt=` nicht angegeben ist, durch `<image/jpeg>`.

Der HTTP-Antwortstatus ist „200 OK“, wenn die Anfragemethode eine unbedingte `GET` oder `HEAD` war.

Der Server kann mit dem Status &#39;304&#39; (nicht geändert) antworten und gibt keine Bilddaten als Antwort auf eine bedingte `GET`-Anfrage zurück (die eine gültige `If-Modified-Since` oder `If-None-Match` Kopfzeile enthält).
