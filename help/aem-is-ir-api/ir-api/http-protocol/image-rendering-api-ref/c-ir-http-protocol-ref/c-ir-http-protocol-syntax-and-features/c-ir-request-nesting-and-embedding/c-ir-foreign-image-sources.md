---
description: Image Serving unterstützt den Zugriff auf Quellbilder auf ausländischen HTTP- und FTP-Servern.
seo-description: Image Serving unterstützt den Zugriff auf Quellbilder auf ausländischen HTTP- und FTP-Servern.
seo-title: Ausländische Bildquellen
solution: Experience Manager
title: Ausländische Bildquellen
topic: Scene7 Image Serving - Image Rendering API
uuid: 28a17400-4807-4e14-937a-80309be53d55
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Ausländische Bildquellen{#foreign-image-sources}

Image Serving unterstützt den Zugriff auf Quellbilder auf ausländischen HTTP- und FTP-Servern.

So geben Sie eine ausländische URL für einen `src=` oder einen `mask=` Befehl an die gesamte eingebettete URL mit geschweiften Klammern trennen:

` …&src={ *[!DNL foreignUrl]*}&…`

Vollständige absolute URLs (sofern festgelegt) und URLs relativ zu `attribute::AllowDirectUrls` `attribute::RootUrl` diesen sind zulässig. Ein Fehler tritt auf, wenn eine absolute URL eingebettet und ein Attribut: ist 0 `AllowDirectUrls` oder wenn eine relative URL angegeben ist und leer `attribute::RootUrl` ist.

Ausländische Bilder werden vom Server gemäß den in der HTTP-Antwort enthaltenen Cache-Headern zwischengespeichert.
