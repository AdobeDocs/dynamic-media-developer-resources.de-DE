---
description: Verwenden Sie diese Servereinstellungen, um die Ablaufverfolgungsprotokollierung zu debuggen.
seo-description: Verwenden Sie diese Servereinstellungen, um die Ablaufverfolgungsprotokollierung zu debuggen.
seo-title: Debug_trace-Protokollierung
solution: Experience Manager
title: Debug_trace-Protokollierung
topic: Scene7 Image Serving - Image Rendering API
uuid: 33f1d093-007d-453b-965a-9d701a845954
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---


# Debug_trace-Protokollierung{#debug-trace-logging}

Verwenden Sie diese Servereinstellungen, um die Ablaufverfolgungsprotokollierung zu debuggen.

>[!NOTE]
>
>Es wird empfohlen, alle Protokolldateien so zu konfigurieren, dass sie in denselben Ordner geschrieben werden wie `TC::directory`. Dadurch wird sichergestellt, dass alle Image Serving-Protokolldateien an der automatischen Protokolldatei-Drehung teilnehmen, mit der konfiguriert wurde, `TC::maxDays`wodurch eine potenzielle Serverinstabilität aufgrund von nicht auf der Festplatte gespeicherten Speicherbedingungen verhindert wird.

## SV::log - Dateipfad des Serveraufzeichnungsprotokolls {#section-3697bc480ff646e79cacc2812c55ef26}

Ordner- und Basisdateiname für Serveraufsehprotokolldateien. Der Pfad kann absolut oder relativ zu *[!DNL install_folder]* sein. Der Server Supervisor hängt einen Bindestrich und das aktuelle Datum ( *[!DNL -yyyy-mm-dd]*) an den Dateinamen an (gegebenenfalls vor dem Dateisuffix). Es wird empfohlen, alle Protokolldateien in denselben Ordner wie die Protokolldateien von Platform Server ( `PS::LogFolder`) zu senden, um die vom Platform Server implementierte Protokolldateiverwaltung zu nutzen ( `PS::LogDays`). Die Standardgrenze ist [!DNL logs/Supervisor.log].

>[!NOTE]
>
>Der neue Ordner muss erstellt werden, bevor diese Einstellung geändert werden kann. Stellen Sie sicher, dass die Zugriffsberechtigungen so festgelegt sind, dass der Server Supervisor über die erforderlichen Berechtigungen zum Erstellen, Lesen und Schreiben verfügt.

## SV::tracelevel - Server Supervisor Trace Log Level {#section-36f8634741da4c618d67aa628b5fe474}

Die Protokollebene kann 1, 2, 3 oder 4 betragen. Der Standardwert ist „2“.

## IS:Log - Image-Server-Debug-Protokolldateipfad {#section-73a3f09b77f2446c9f82207b7d8aec39}

Ordner- und Basisdateiname für Image-Server-Ablaufverfolgungsprotokolldateien. Der Pfad kann absolut oder relativ zu *[!DNL install_folder]* sein. Der ImageServer hängt einen Bindestrich und das aktuelle Datum ( *[!DNL -yyyy-mm-dd]*) an den Dateinamen an (gegebenenfalls vor dem Dateisuffix). Es wird empfohlen, Image-Server-Protokolldateien in denselben Ordner wie Platform Server-Protokolldateien zu senden ( `PS::LogFolder`), um die vom Platform-Server implementierte Protokolldateiverwaltung zu nutzen (siehe `PS::LogDays`).

>[!NOTE]
>
>Der neue Ordner muss erstellt werden, bevor diese Einstellung geändert werden kann. Stellen Sie sicher, dass die Zugriffsberechtigungen so festgelegt sind, dass Image Serving über die erforderlichen Berechtigungen zum Erstellen, Lesen und Schreiben verfügt.

## IS:TraceClient - Debug-Protokollebene des Image-Servers {#section-3851f1f68e404430985c629ac80534db}

Die Protokollebene kann 1, 2, 3 oder 4 betragen (Standard ist 2)

Stufe 1 protokolliert Ereignis im Zusammenhang mit Beginn-Up-, Abschaltungs- und Platform-Server-Verbindungen.

Stufe 2 protokolliert auch die Verbindung zu den Quellbildern und deren Trennung.

Stufe 3 fügt die Protokollierung von Anforderungen für Pixeldaten und den gleichen Versand zum Platform-Server hinzu.

In Stufe 4 werden alle vom Platform-Server erhaltenen Meldungen aufgezeichnet.

Level 3 und 4 sollten nur zu Debugging-Zwecken verwendet werden, da die Protokolldateien sehr groß werden können.

## IS::TraceStatsInterval - Image Server Statistics Log Interval {#section-1d8df96d61044e33a5b2b2b0309c2d59}

Der Image-Server schreibt Speicherstatistiken in die Ablaufverfolgungsprotokolldatei in dem von dieser Einstellung festgelegten Intervall. Der gültige Bereich liegt zwischen 5 und 86.400 Sekunden.
