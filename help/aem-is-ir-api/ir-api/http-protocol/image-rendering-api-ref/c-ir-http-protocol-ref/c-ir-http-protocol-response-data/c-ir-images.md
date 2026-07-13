---
title: Bilder
description: 'Bilddaten werden zurückgegeben, wenn eine Anforderung erfolgreich abgeschlossen wurde und die Anforderung entweder keinen Befehl req= enthält oder wenn req= einen der folgenden Werte aufweist: img, debug.'
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 089aaf9d-f414-4ca4-9d6d-7f429de2531e
TQID: 'https://experienceleague.adobe.com/4wHyyXX0gxz9ojr5g5Puu5fBhKXo4hZDjyBuVTao3rQ'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 1%

---

# Bilder{#images}

Bilddaten werden zurückgegeben, wenn eine Anforderung erfolgreich abgeschlossen wurde und die Anforderung entweder keinen Befehl req= enthält oder wenn req= einen der folgenden Werte aufweist: img, debug

Der MIME-Typ der HTTP-Antwort wird durch `fmt=` bestimmt oder, wenn `fmt=` nicht angegeben ist, hängt er vom Wert von `attribute::Format` ab.

Der HTTP-Antwortstatus ist „200 OK“, wenn die Anfragemethode eine unbedingte `GET` oder `HEAD` war.

Der Server kann mit dem Status &#39;304&#39; (nicht geändert) antworten und gibt als Reaktion auf eine bedingte `GET`-Anforderung keine Bilddaten zurück (mit dem [!DNL If-Modified-Since] Feld im `request-header`).

