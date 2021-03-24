---
description: Allgemeine Servereinstellungen
solution: Experience Manager
title: Allgemein
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator, Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 1%

---


# Allgemein{#general}

Allgemeine Servereinstellungen

## TC::PsPort - Main Listening Port {#section-d31d3051aa994a76b60b70c3d9f7e89f}

Gibt den Haupt-Listening-Anschluss für den Plattformserver an. Dieser Anschluss wird auch verwendet, um auf die Dokumentations- und Beispielseiten für Image Serving, Image Rendering und Dynamic Media Viewers (falls installiert) zuzugreifen.

## IS::CacheServerUrl - Caching-Dienst-Stammordner-URL {#section-bcca227a1f91453b834db4ea050968e2}

Gibt den HTTP-Stammpfad an, um dem Image-Server Zugriff auf den Cache-Dienst zu gewähren. Muss auf [!DNL http://localhost:TC::PsPort /is/cache/secondary] gesetzt werden, wobei die Anschlussnummer `TC::PsPort` übereinstimmt.

## IS::RemoteUrlDefaultExpiration - Standard für Remote-Bildquelle TTL {#section-e4c31228b459492cacd2f482d9575f71}

Die TTL für zwischengespeicherte Bilder, die über HTTP von einer Remote-Quelle mit dem `src={…}`-Konstrukt abgerufen werden. Wird nur verwendet, wenn der Remote-Server keinen Ablaufheader in seiner HTTP-Antwort enthält. Ganzzahlwert in Sekunden.

## IS::RemoteUrlTimeout - Remote Image Source Timeout {#section-437646c479cc4bea81dae42100a3c50a}

Die Zeit, die der Image-Server auf die Bereitstellung der angeforderten Bilddatei per HTTP wartet, bevor ein Fehler zurückgegeben wird. Ganzzahlwert in Sekunden.

## PS::allowDefaultCatalogRequests - Aktivieren/Deaktivieren von Standardkataloganforderungen {#section-484e442a115a49b4ac269d1718b351e1}

Auf &quot;false&quot;setzen, um Anforderungen zu deaktivieren, die keine gültige Katalog-ID im Pfad enthalten. Die Standardgrenze ist `true`. Bei Festlegung auf `false` wird bei Anforderungen ohne Katalog-ID ein Fehler zurückgegeben.

>[!NOTE]
>
>`req=catalogprops` nicht dieser Einstellung unterliegt.

## PS::saveToFile.saveTimeout - File Save Timeout {#section-d22afd8ad86144b28684ed95a59db40e}

Standardwert für `req=saveToFile`, wenn `timeout=`nicht angegeben ist. `msec`. Wenn der Speichervorgang nicht innerhalb der angegebenen Zeitspanne abgeschlossen ist, wird ein Fehler zurückgegeben.
