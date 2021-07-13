---
description: Verwenden Sie diese Servereinstellungen, um die Ablaufprotokollierung zu debuggen.
solution: Experience Manager
title: Debug_Trace-Protokollierung
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,User
exl-id: fe1fc984-3c6b-4bd1-b5ba-630860ac7319
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 0%

---

# Debug_Trace-Protokollierung{#debug-trace-logging}

Verwenden Sie diese Servereinstellungen, um die Ablaufprotokollierung zu debuggen.

>[!NOTE]
>
>Es wird empfohlen, alle Protokolldateien so zu konfigurieren, dass sie in denselben Ordner wie `TC::directory` geschrieben werden. Dadurch wird sichergestellt, dass alle Image Serving-Protokolldateien an der automatischen Protokolldateirotation teilnehmen, die mit `TC::maxDays` konfiguriert wurde. Dadurch wird potenzielle Server-Instabilität aufgrund von nicht genügend Festplattenspeicher zur Verfügung stehenden Bedingungen verhindert.

## SV::log - Pfad der Protokolldatei für den Server-Supervisor {#section-3697bc480ff646e79cacc2812c55ef26}

Ordner- und Basisdateinamen für Server Supervisor-Protokolldateien. Der Pfad kann absolut oder relativ zu *[!DNL install_folder]* sein. Der Server Supervisor hängt einen Bindestrich und das aktuelle Datum ( *[!DNL -yyyy-mm-dd]*) an den Dateinamen an (gegebenenfalls vor dem Dateisuffix). Es wird empfohlen, alle Protokolldateien in denselben Ordner wie die Platform Server-Protokolldateien ( `PS::LogFolder`) zu senden, um die vom Platform Server implementierte Protokolldateiverwaltung ( `PS::LogDays`) zu nutzen. Die Standardgrenze ist [!DNL logs/Supervisor.log].

>[!NOTE]
>
>Der neue Ordner muss erstellt werden, bevor diese Einstellung geändert werden kann. Stellen Sie sicher, dass die Zugriffsberechtigungen so festgelegt sind, dass der Server Supervisor über die erforderlichen Berechtigungen zum Erstellen, Lesen und Schreiben verfügt.

## SV: tracelevel - Server Supervisor Trace Log Level {#section-36f8634741da4c618d67aa628b5fe474}

Die Protokollebene kann 1, 2, 3 oder 4 betragen. Der Standardwert ist „2“.

## IS::Log - Image Server Debug Log File Path {#section-73a3f09b77f2446c9f82207b7d8aec39}

Ordner- und Basisdateinamen für Image Server-Ablaufverfolgungsprotokolldateien. Der Pfad kann absolut oder relativ zu *[!DNL install_folder]* sein. Der ImageServer hängt einen Bindestrich und das aktuelle Datum ( *[!DNL -yyyy-mm-dd]*) an den Dateinamen an (gegebenenfalls vor dem Dateisuffix). Es wird empfohlen, Image-Server-Protokolldateien in denselben Ordner zu senden wie Platform Server-Protokolldateien ( `PS::LogFolder`), um die vom Platform Server implementierte Protokolldateiverwaltung zu nutzen (siehe `PS::LogDays`).

>[!NOTE]
>
>Der neue Ordner muss erstellt werden, bevor diese Einstellung geändert werden kann. Stellen Sie sicher, dass die Zugriffsberechtigungen so festgelegt sind, dass das Image Serving über die erforderlichen Berechtigungen zum Erstellen, Lesen und Schreiben verfügt.

## IS:TraceClient - Image Server Debug Log Level {#section-3851f1f68e404430985c629ac80534db}

Die Protokollebene kann 1, 2, 3 oder 4 sein (Standard ist 2).

Level 1 protokolliert Ereignisse im Zusammenhang mit Start-, Fahren- und Platform Server-Verbindungen.

Stufe 2 protokolliert auch die Verbindung zu Quellbildern und deren Trennung von diesen.

Stufe 3 fügt die Protokollierung von Anforderungen für Pixeldaten und die Bereitstellung derselben an den Platform-Server hinzu.

Stufe 4 zeichnet alle vom Platform-Server empfangenen Nachrichten auf.

Level 3 und 4 sollten nur zu Debugging-Zwecken verwendet werden, da die Protokolldateien sehr groß werden können.

## IS::TraceStatsInterval - Image Server Statistics Log Interval {#section-1d8df96d61044e33a5b2b2b0309c2d59}

Der Image-Server schreibt Speicherstatistiken in seine Ablaufverfolgungsprotokolldatei in dem von dieser Einstellung festgelegten Intervall. Der gültige Bereich beträgt 5 bis 86.400 Sekunden.
