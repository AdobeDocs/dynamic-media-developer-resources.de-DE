---
description: Image Serving unterstützt den Zugriff auf Quellbilder auf ausländischen HTTP- und FTP-Servern.
solution: Experience Manager
title: Ausländische Bildquellen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 90f96a76-e9f3-4ad0-84af-bc0d093acf19
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---

# Ausländische Bildquellen{#foreign-image-sources}

Image Serving unterstützt den Zugriff auf Quellbilder auf ausländischen HTTP- und FTP-Servern.

So geben Sie eine fremde URL für einen `src=`- oder `mask=`-Befehl an: die gesamte eingebettete URL einfach mit geschweiften Klammern trennen:

` …&src={ *[!DNL foreignUrl]*}&…`

Vollständige absolute URLs (wenn `attribute::AllowDirectUrls` festgelegt ist) und URLs relativ zu `attribute::RootUrl` sind zulässig. Ein Fehler tritt auf, wenn eine absolute URL eingebettet und das Attribut: `AllowDirectUrls` ist 0, oder wenn eine relative URL angegeben und `attribute::RootUrl` leer ist.

Ausländische Bilder werden vom Server gemäß den in der HTTP-Antwort enthaltenen Zwischenspeicherkopfzeilen zwischengespeichert.
