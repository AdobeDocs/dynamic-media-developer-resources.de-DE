---
description: Image Serving unterstützt den Zugriff auf Quellbilder auf ausländischen HTTP- und FTP-Servern.
seo-description: Image Serving unterstützt den Zugriff auf Quellbilder auf ausländischen HTTP- und FTP-Servern.
seo-title: Ausländische Bildquellen
solution: Experience Manager
title: Ausländische Bildquellen
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 28a17400-4807-4e14-937a-80309be53d55
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---


# Ausländische Bildquellen{#foreign-image-sources}

Image Serving unterstützt den Zugriff auf Quellbilder auf ausländischen HTTP- und FTP-Servern.

So geben Sie eine ausländische URL für einen Befehl `src=` oder `mask=` an die gesamte eingebettete URL mit geschweiften Klammern trennen:

` …&src={ *[!DNL foreignUrl]*}&…`

Vollständige absolute URLs (wenn `attribute::AllowDirectUrls` eingestellt ist) und URLs relativ zu `attribute::RootUrl` sind zulässig. Ein Fehler tritt auf, wenn eine absolute URL eingebettet und ein Attribut: `AllowDirectUrls` ist 0, oder wenn eine relative URL angegeben ist und `attribute::RootUrl` leer ist.

Ausländische Bilder werden vom Server gemäß den in der HTTP-Antwort enthaltenen Cache-Headern zwischengespeichert.
