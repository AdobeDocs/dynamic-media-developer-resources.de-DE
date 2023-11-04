---
description: Verwenden Sie diese Servereinstellungen, um die Bildgröße zu begrenzen.
solution: Experience Manager
title: Bildgrößenbeschränkungen
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 75ec58ee-8c98-46cb-96b2-79d1c32e576f
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---

# Bildgrößenbeschränkungen{#image-size-limits}

Verwenden Sie diese Servereinstellungen, um die Bildgröße zu begrenzen.

## IS::MaxMessageSize - Maximale Antwortgröße {#section-bd942385d4d144cd904003695d72c85e}

Schränkt die Größe der Daten ein, die der Image-Server an die [!DNL Platform Server]. Dadurch wird die Größe des kodierten/komprimierten Antwortbilds begrenzt, das Image Serving über HTTP (Mbytes) an den Client zurückgeben kann.

## IS::MaxRenderRgnPixels - Maximale Größe des Ausgabebilds {#section-868ceb9764dd42dfb133ffeb72f9d3fb}

Beschränkt die Größe der vom Image-Server erzeugten Bilder (ohne in einer Datei gespeicherte Bilder). Ganzzahlwert größer als 0 in Millionen von Pixeln. Wenn ein Rendervorgang die Größenbeschränkung überschreiten würde, wird ein Fehler zurückgegeben. Der Standardwert ist „16“.

## IS::MaxSavePixels - Größenbeschränkung für das Speichern in Dateien {#section-d1547c4afa88467080ab08356f775e06}

Schränkt die Größe der Bilder ein, die der Image-Server in Dateien mit dem `req=saveToFile` Befehl. Ganzzahlwert größer als 0 in Millionen von Pixeln. Wenn der Dateispeichervorgang diese Grenze überschreitet, wird ein Fehler zurückgegeben. Der Standardwert beträgt 100 Millionen Pixel.

## IS::MaxNonDsfSize - Größenbeschränkung für Nicht-PTIFF-Eingabebilder {#section-50de28a7158a436393cce5da0d1e4d46}

Die maximale Größe (in Pixeln) von Bildern, bei denen es sich nicht um PTIFFs handelt, die der Image-Server öffnen darf. Image Serving gibt einen Fehler zurück, wenn versucht wird, auf ein Nicht-PTIFF-Bild zuzugreifen, das diese Grenze überschreitet.

>[!NOTE]
>
>Wird dieser Wert zu hoch eingestellt, kann der Image-Server an Speicher verhungern und zu Fehlern, einschließlich Abstürzen, führen.
