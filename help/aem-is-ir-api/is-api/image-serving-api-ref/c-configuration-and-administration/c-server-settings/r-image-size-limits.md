---
description: Verwenden Sie diese Server-Einstellungen, um Bildgrößenbeschränkungen festzulegen.
solution: Experience Manager
title: Bildgrößenbeschränkungen
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 75ec58ee-8c98-46cb-96b2-79d1c32e576f
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 1%

---

# Bildgrößenbeschränkungen{#image-size-limits}

Verwenden Sie diese Server-Einstellungen, um Bildgrößenbeschränkungen festzulegen.

## IS::MaxMessageSize - Maximale Antwortgröße {#section-bd942385d4d144cd904003695d72c85e}

Beschränkt die Größe der Daten, die der Bild-Server an den [!DNL Platform Server] senden darf. Dadurch wird die Größe des kodierten/komprimierten Antwortbildes begrenzt, das Image Serving über HTTP (MByte) an den Client zurückgeben kann.

## IS::MaxRenderRennPixel - Maximale Größe des Ausgabebilds {#section-868ceb9764dd42dfb133ffeb72f9d3fb}

Beschränkt die Größe der Bilder, die der Bild-Server erzeugen kann (mit Ausnahme der in einer Datei gespeicherten Bilder). Ganzzahliger Wert größer als 0 in Millionen von Pixeln. Ein Fehler wird zurückgegeben, wenn ein Render-Vorgang die Größenbeschränkung überschreiten würde. Die Standardgrenze ist 16.

## IS::MaxSavePixels - Größenbeschränkung für das Speichern in Dateien {#section-d1547c4afa88467080ab08356f775e06}

Beschränkt die Größe von Bildern, die der Bild-Server mit dem Befehl `req=saveToFile` in Dateien schreibt. Ganzzahliger Wert größer als 0 in Millionen von Pixeln. Ein Fehler wird zurückgegeben, wenn der Dateispeichervorgang dieses Limit überschreiten würde. Der Standardwert ist 100 Millionen Pixel.

## IS::MaxNonDSFsize - Größenbeschränkung für Nicht-PTIFF-Eingabebilder {#section-50de28a7158a436393cce5da0d1e4d46}

Die maximale Größe (in Megapixeln) von Bildern, bei denen es sich nicht um PTIFFs handelt, die der Bildserver öffnen darf. Image Serving gibt einen Fehler zurück, wenn versucht wird, auf ein Nicht-PTIFF-Bild zuzugreifen, das größer ist als diese Beschränkung.

>[!NOTE]
>
>Wenn Sie diesen Wert zu hoch einstellen, kann dies dazu führen, dass dem Bildserver der Speicher ausgeht, was zu Fehlern, einschließlich Abstürzen, führen kann.
