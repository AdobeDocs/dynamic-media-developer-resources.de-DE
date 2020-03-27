---
description: Verwenden Sie diese Servereinstellungen, um Bildgrößenbeschränkungen festzulegen.
seo-description: Verwenden Sie diese Servereinstellungen, um Bildgrößenbeschränkungen festzulegen.
seo-title: Bildgrößenbegrenzungen
solution: Experience Manager
title: Bildgrößenbegrenzungen
topic: Scene7 Image Serving - Image Rendering API
uuid: 6736e652-c495-45a2-bdd2-9975f99af0a2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Bildgrößenbegrenzungen{#image-size-limits}

Verwenden Sie diese Servereinstellungen, um Bildgrößenbeschränkungen festzulegen.

## IS::MaxMessageSize - Maximale Antwortgröße {#section-bd942385d4d144cd904003695d72c85e}

Begrenzt die Größe der Daten, die der Image-Server an den Platform Server senden darf. Dadurch wird die Größe des kodierten/komprimierten Antwortbilds begrenzt, das Image Serving über HTTP (Mbyte) an den Client zurückgeben kann.

## IS::MaxRenderRgnPixels - Maximale Bildgröße {#section-868ceb9764dd42dfb133ffeb72f9d3fb}

Begrenzt die Größe der Bilder, die vom Image-Server erstellt werden können (mit Ausnahme der in einer Datei gespeicherten Bilder). Ganzzahlwert größer als 0 in Millionen Pixeln. Ein Fehler wird zurückgegeben, wenn ein Rendervorgang die Größenbeschränkung überschreitet. Der Standardwert ist „16“.

## IS::MaxSavePixels - Größenbeschränkung zum Speichern in Dateien {#section-d1547c4afa88467080ab08356f775e06}

Begrenzt die Größe der Bilder, die der Image-Server mit dem `req=saveToFile` Befehl in Dateien schreibt. Ganzzahlwert größer als 0 in Millionen Pixeln. Wenn der Dateispeichervorgang diesen Grenzwert überschreitet, wird ein Fehler zurückgegeben. Der Standardwert ist 100 Millionen Pixel.

## IS::MaxNonDsfSize - Größenbeschränkung für Nicht-PTIFF-Eingabebilder {#section-50de28a7158a436393cce5da0d1e4d46}

Die maximale Größe (in Pixel) von Bildern, bei denen es sich nicht um PTIFFs handelt, die der Image-Server öffnen darf. Beim Image Serving wird ein Fehler zurückgegeben, wenn versucht wird, auf ein Bild zuzugreifen, das kein PTIFF-Bild ist und diesen Grenzwert überschreitet.

>[!NOTE] {class=&quot;- topic/note &quot;
>
>Wenn Sie diesen Wert zu hoch einstellen, wird der Image-Server möglicherweise nicht mehr über Arbeitsspeicher verfügen und es kann zu Fehlern, einschließlich Abstürzen, kommen.

