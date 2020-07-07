---
description: Allgemeine Servereinstellungen
seo-description: Allgemeine Servereinstellungen
seo-title: Allgemein
solution: Experience Manager
title: Allgemein
topic: Scene7 Image Serving - Image Rendering API
uuid: d7ec3dba-64b8-431b-b446-84ab6139ba8a
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 2%

---


# Allgemein{#general}

Allgemeine Servereinstellungen

## TC::PsPort - Port für die Hauptüberwachung {#section-d31d3051aa994a76b60b70c3d9f7e89f}

Gibt den Haupt-Listening-Anschluss für den Platform-Server an. Dieser Anschluss wird auch verwendet, um auf die Dokumentations- und Beispielseiten für Image Serving, Image Rendering und Scene7 Viewer zuzugreifen (falls installiert).

## IS::CacheServerUrl - Caching-Dienst-Stammordner-URL {#section-bcca227a1f91453b834db4ea050968e2}

Gibt den HTTP-Stammpfad an, um dem Image-Server Zugriff auf den Cache-Dienst zu gewähren. Muss auf eingestellt sein, [!DNL http://localhost:TC::PsPort /is/cache/secondary]wobei die Anschlussnummer übereinstimmt `TC::PsPort`.

## IS::RemoteUrlDefaultExpiration - Standard für Remote-Bildquelle TTL {#section-e4c31228b459492cacd2f482d9575f71}

Die TTL für zwischengespeicherte Bilder, die über HTTP von einer Remote-Quelle mithilfe des `src={…}` Konstrukts abgerufen werden. Wird nur verwendet, wenn der Remote-Server keinen Ablaufheader in seiner HTTP-Antwort enthält. Ganzzahlwert in Sekunden.

## IS::RemoteUrlTimeout - Zeitlimit für Remote-Bildquelle {#section-437646c479cc4bea81dae42100a3c50a}

Die Zeit, die der Image-Server auf die Bereitstellung der angeforderten Bilddatei per HTTP wartet, bevor ein Fehler zurückgegeben wird. Ganzzahlwert in Sekunden.

## PS::allowDefaultCatalogRequests - Standardkataloganforderungen aktivieren/deaktivieren {#section-484e442a115a49b4ac269d1718b351e1}

Auf &quot;false&quot;setzen, um Anforderungen zu deaktivieren, die keine gültige Katalog-ID im Pfad enthalten. Die Standardgrenze ist `true`. Bei Festlegung auf `false`wird bei Anforderungen ohne Katalog-ID ein Fehler zurückgegeben.

>[!NOTE]
>
>`req=catalogprops` nicht dieser Einstellung unterliegt.

## PS::saveToFile.saveTimeout - Zeitlimit für Dateispeicherung {#section-d22afd8ad86144b28684ed95a59db40e}

Standardwert für Zeitüberschreitung, `req=saveToFile` wenn `timeout=`kein Wert angegeben ist. `msec`. Wenn der Speichervorgang nicht innerhalb der angegebenen Zeitspanne abgeschlossen ist, wird ein Fehler zurückgegeben.
