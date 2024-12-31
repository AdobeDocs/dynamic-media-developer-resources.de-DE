---
description: Allgemeine Server-Einstellungen
solution: Experience Manager
title: Allgemein
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 3e4079e7-6def-4938-bb5b-c8122502712d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---

# Allgemein{#general}

Allgemeine Server-Einstellungen

## TC::PSport - Haupt-Überwachungs-Port {#section-d31d3051aa994a76b60b70c3d9f7e89f}

Gibt den Haupt-Listening-Port für die [!DNL Platform Server] an. Über diesen Port können Sie auch auf die Dokumentations- und Beispielseiten für Image Serving, Image Rendering und Dynamic Media Viewer (falls installiert) zugreifen.

## IS:CacheServerUrl - Zwischenspeicherung der Dienststamm-URL {#section-bcca227a1f91453b834db4ea050968e2}

Gibt den HTTP-Stammpfad an, der dem Bildserver Zugriff auf den Caching-Service gewährt. Muss auf [!DNL http://localhost:TC::PsPort /is/cache/secondary] gesetzt werden, wobei die Port-Nummer mit `TC::PsPort` übereinstimmt.

## IS::RemoteUrlDefaultExpiration - Standard-TTL für Remote-Image Source {#section-e4c31228b459492cacd2f482d9575f71}

Die TTL für zwischengespeicherte Bilder, die über HTTP aus einer Remote-Quelle unter Verwendung des `src={…}` abgerufen wurden. Wird nur verwendet, wenn der Remote-Server in seiner HTTP-Antwort keine Ablaufkopfzeile enthält. Ganzzahliger Wert in Sekunden.

## IS::RemoteUrlTimeout - Zeitüberschreitung bei Remote-Image Source {#section-437646c479cc4bea81dae42100a3c50a}

Die Zeit, die der Bild-Server wartet, bis ein Remote-Server die angeforderte Bilddatei per HTTP bereitstellt, bevor ein Fehler zurückgegeben wird. Ganzzahliger Wert in Sekunden.

## PS::allowDefaultCatalogRequests - Standardkataloganforderungen aktivieren/deaktivieren {#section-484e442a115a49b4ac269d1718b351e1}

Legen Sie dies auf „false“ fest, um Anfragen zu verbieten, die keine gültige Katalog-ID im Pfad enthalten. Der Standardwert ist `true`. Bei Festlegung auf `false` wird bei Anfragen ohne Katalog-ID ein Fehler zurückgegeben.

>[!NOTE]
>
>`req=catalogprops` ist von dieser Einstellung nicht betroffen.

## PS::saveToFile.saveTimeout - Zeitüberschreitung bei Dateispeicherung {#section-d22afd8ad86144b28684ed95a59db40e}

Standardwert für die maximale Wartezeit für `req=saveToFile`, wenn `timeout=`nicht angegeben ist. `msec`. Wenn der Speichervorgang nicht innerhalb der angegebenen Zeitspanne abgeschlossen wird, wird ein Fehler zurückgegeben.
