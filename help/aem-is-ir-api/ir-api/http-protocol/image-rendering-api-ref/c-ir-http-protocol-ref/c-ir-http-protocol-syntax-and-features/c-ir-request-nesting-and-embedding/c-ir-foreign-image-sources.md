---
title: Fremdbildquellen
description: Image Serving unterstützt den Zugriff auf Quellbilder auf fremden HTTP- und FTP-Servern.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 90f96a76-e9f3-4ad0-84af-bc0d093acf19
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 0%

---

# Fremdbildquellen{#foreign-image-sources}

Image Serving unterstützt den Zugriff auf Quellbilder auf fremden HTTP- und FTP-Servern.

Um eine Fremd-URL für einen `src=` oder einen `mask=`-Befehl anzugeben, trennen Sie einfach die gesamte eingebettete URL durch geschweifte Klammern ab:

` …&src={ *[!DNL foreignUrl]*}&…`

Vollständige absolute URLs (sofern `attribute::AllowDirectUrls` festgelegt ist) und URLs relativ zu `attribute::RootUrl` sind zulässig. Ein Fehler tritt auf, wenn eine absolute URL eingebettet ist und das Attribut: `AllowDirectUrls` gleich 0 ist oder wenn eine relative URL angegeben und `attribute::RootUrl` leer ist.

Fremdbilder werden vom Server entsprechend den in der HTTP-Antwort enthaltenen Caching-Kopfzeilen zwischengespeichert.
