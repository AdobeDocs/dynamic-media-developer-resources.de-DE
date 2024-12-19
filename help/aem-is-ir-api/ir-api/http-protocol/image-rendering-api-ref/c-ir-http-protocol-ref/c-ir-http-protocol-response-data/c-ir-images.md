---
title: Bilder
description: 'Bilddaten werden zurückgegeben, wenn eine Anforderung erfolgreich abgeschlossen wurde und die Anforderung entweder keinen Befehl req= enthält oder wenn req= einen der folgenden Werte aufweist: img, debug.'
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 089aaf9d-f414-4ca4-9d6d-7f429de2531e
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 1%

---

# Bilder{#images}

Bilddaten werden zurückgegeben, wenn eine Anforderung erfolgreich abgeschlossen wurde und die Anforderung entweder keinen Befehl req= enthält oder wenn req= einen der folgenden Werte aufweist: img, debug

Der MIME-Typ der HTTP-Antwort wird durch `fmt=` bestimmt oder, wenn `fmt=` nicht angegeben ist, hängt er vom Wert von `attribute::Format` ab.

Der HTTP-Antwortstatus ist „200 OK“, wenn die Anfragemethode eine unbedingte `GET` oder `HEAD` war.

Der Server kann mit dem Status &#39;304&#39; (nicht geändert) antworten und gibt als Reaktion auf eine bedingte `GET`-Anforderung keine Bilddaten zurück (mit dem [!DNL If-Modified-Since] Feld im `request-header`).
