---
description: Image Serving unterstützt den Zugriff auf Quellbilder auf ausländischen HTTP- und FTP-Servern.
solution: Experience Manager
title: Ausländische Bildquellen
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 0%

---


# Ausländische Bildquellen{#foreign-image-sources}

Image Serving unterstützt den Zugriff auf Quellbilder auf ausländischen HTTP- und FTP-Servern.

So geben Sie eine ausländische URL für einen Befehl `src=` oder `mask=` an die gesamte eingebettete URL mit geschweiften Klammern trennen:

` …&src={ *[!DNL foreignUrl]*}&…`

Vollständige absolute URLs (wenn `attribute::AllowDirectUrls` eingestellt ist) und URLs relativ zu `attribute::RootUrl` sind zulässig. Ein Fehler tritt auf, wenn eine absolute URL eingebettet und ein Attribut: `AllowDirectUrls` ist 0, oder wenn eine relative URL angegeben ist und `attribute::RootUrl` leer ist.

Ausländische Bilder werden vom Server gemäß den in der HTTP-Antwort enthaltenen Cache-Headern zwischengespeichert.
