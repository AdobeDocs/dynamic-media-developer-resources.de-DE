---
description: Allgemeine Servereinstellungen
solution: Experience Manager
title: Allgemein
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 3e4079e7-6def-4938-bb5b-c8122502712d
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 1%

---

# Allgemein{#general}

Allgemeine Servereinstellungen

## TC::PsPort - Haupt-Listening-Port {#section-d31d3051aa994a76b60b70c3d9f7e89f}

Gibt den Haupt-Listening-Anschluss für den Platform-Server an. Dieser Anschluss wird auch verwendet, um auf die Dokumentations- und Beispielseiten für Image Serving, Image Rendering und die Dynamic Media-Viewer zuzugreifen (falls installiert).

## IS::CacheServerUrl - Caching Service Root Url {#section-bcca227a1f91453b834db4ea050968e2}

Gibt den HTTP-Stammpfad an, um dem Image-Server Zugriff auf den Caching-Dienst zu gewähren. Muss auf [!DNL http://localhost:TC::PsPort /is/cache/secondary], wobei die Anschlussnummer mit der `TC::PsPort`.

## IS::RemoteUrlDefaultExpiration - Remote Image Source Default TTL {#section-e4c31228b459492cacd2f482d9575f71}

TTL für zwischengespeicherte Bilder, die über HTTP von einer Remote-Quelle mit der `src={…}` -Konstrukt. Wird nur verwendet, wenn der Remote-Server in seiner HTTP-Antwort keinen Ablaufheader enthält. Ganzzahlwert in Sekunden.

## IS::RemoteUrlTimeout - Remote Image Source Timeout {#section-437646c479cc4bea81dae42100a3c50a}

Die Zeit, die der Image-Server wartet, bis ein Remote-Server die angeforderte Bilddatei über HTTP bereitstellt, bevor ein Fehler zurückgegeben wird. Ganzzahlwert in Sekunden.

## PS::allowDefaultCatalogRequests - Enable/Disable Default Catalog Requests {#section-484e442a115a49b4ac269d1718b351e1}

Auf false gesetzt, um Anfragen zu verweigern, die keine gültige Katalogkennung im Pfad enthalten. Die Standardgrenze ist `true`. Wenn auf `false`wird bei Anfragen ohne Katalogkennung ein Fehler zurückgegeben.

>[!NOTE]
>
>`req=catalogprops` unterliegt dieser Einstellung nicht.

## PS::saveToFile.saveTimeout - Zeitüberschreitung bei Dateispeicherung {#section-d22afd8ad86144b28684ed95a59db40e}

Standardwert für Zeitüberschreitung für `req=saveToFile` when `timeout=`nicht angegeben ist. `msec`. Wenn der Speichervorgang nicht innerhalb der angegebenen Zeit abgeschlossen ist, wird ein Fehler zurückgegeben.
