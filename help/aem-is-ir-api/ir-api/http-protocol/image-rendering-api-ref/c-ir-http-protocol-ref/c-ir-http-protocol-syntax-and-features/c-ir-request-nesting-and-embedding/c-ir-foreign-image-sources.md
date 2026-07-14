---
title: Fremdbildquellen
description: Image Serving unterstützt den Zugriff auf Quellbilder auf fremden HTTP- und FTP-Servern.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 90f96a76-e9f3-4ad0-84af-bc0d093acf19
TQID: 'https://experienceleague.adobe.com/doS6fbVfaXGtLVNBAmOkB-TquNmOc5B2B--IewouFDY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 103
ht-degree: 0%

---

# Fremdbildquellen{#foreign-image-sources}

Image Serving unterstützt den Zugriff auf Quellbilder auf fremden HTTP- und FTP-Servern.

Um eine Fremd-URL für einen `src=` oder einen `mask=`-Befehl anzugeben, trennen Sie einfach die gesamte eingebettete URL durch geschweifte Klammern ab:

` …&src={ *[!DNL foreignUrl]*}&…`

Vollständige absolute URLs (sofern `attribute::AllowDirectUrls` festgelegt ist) und URLs relativ zu `attribute::RootUrl` sind zulässig. Ein Fehler tritt auf, wenn eine absolute URL eingebettet ist und das Attribut: `AllowDirectUrls` gleich 0 ist oder wenn eine relative URL angegeben und `attribute::RootUrl` leer ist.

Fremdbilder werden vom Server entsprechend den in der HTTP-Antwort enthaltenen Caching-Kopfzeilen zwischengespeichert.

