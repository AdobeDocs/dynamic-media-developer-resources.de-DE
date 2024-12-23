---
title: Debug_Trace-Protokollierung
description: Verwenden Sie diese Server-Einstellungen, um die Ablaufverfolgungsprotokollierung zu debuggen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: fe1fc984-3c6b-4bd1-b5ba-630860ac7319
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 0%

---

# Debug_Trace-Protokollierung{#debug-trace-logging}

Verwenden Sie diese Server-Einstellungen, um die Ablaufverfolgungsprotokollierung zu debuggen.

>[!NOTE]
>
>Adobe empfiehlt, alle Protokolldateien so zu konfigurieren, dass sie in denselben Ordner geschrieben werden wie `TC::directory`. Dadurch wird sichergestellt, dass alle Image-Serving-Protokolldateien an der automatischen Protokolldateirotation beteiligt sind, die mit `TC::maxDays` konfiguriert wurde, was eine potenzielle Server-Instabilität aufgrund von Bedingungen verhindert, die zu wenig Speicherplatz belegen.

## SV::log - Dateipfad für Trace-Protokolle des Server-Verantwortlichen {#section-3697bc480ff646e79cacc2812c55ef26}

Ordner- und Basisdateiname für Server Supervisor-Protokolldateien. Der Pfad kann absolut oder relativ zu *[!DNL install_folder]* sein. Der Server Supervisor fügt einen Bindestrich und das aktuelle Datum ( *[!DNL -yyyy-mm-dd]*) an den Dateinamen an (vor dem Dateisuffix, falls vorhanden). Adobe empfiehlt, alle Protokolldateien in denselben Ordner wie [!DNL Platform Server] Protokolldateien ( `PS::LogFolder`) zu senden, um die von [!DNL Platform Server] (`PS::LogDays`) implementierte Protokolldateiverwaltung zu verwenden. Der Standardwert lautet [!DNL logs/Supervisor.log].

>[!NOTE]
>
>Der neue Ordner muss erstellt werden, bevor diese Einstellung geändert werden kann. Stellen Sie sicher, dass die Zugriffsberechtigungen so festgelegt sind, dass der Server Supervisor über die erforderlichen Berechtigungen zum Erstellen, Lesen und Schreiben verfügt.

## SV::traceLevel - Trace-Protokollebene des Server-Verantwortlichen {#section-36f8634741da4c618d67aa628b5fe474}

Die Protokollebene kann 1, 2, 3 oder 4 sein. Der Standardwert ist 2.

## IS::log - Pfad der Debugging-Protokolldatei des Image-Servers {#section-73a3f09b77f2446c9f82207b7d8aec39}

Ordner- und Basisdateiname für Trace-Protokolldateien des Bildservers. Der Pfad kann absolut oder relativ zu *[!DNL install_folder]* sein. ImageServer fügt einen Bindestrich und das aktuelle Datum ( *[!DNL -yyyy-mm-dd]*) an den Dateinamen an (vor dem Dateisuffix, falls vorhanden). Adobe empfiehlt, die Protokolldateien des Image-Servers an denselben Ordner zu senden wie [!DNL Platform Server] Protokolldateien ( `PS::LogFolder`), um die vom [!DNL Platform Server] implementierte Protokolldateiverwaltung zu verwenden (siehe `PS::LogDays`).

>[!NOTE]
>
>Der neue Ordner muss erstellt werden, bevor diese Einstellung geändert werden kann. Stellen Sie sicher, dass die Zugriffsberechtigungen so festgelegt sind, dass Image Serving über die erforderlichen Berechtigungen zum Erstellen, Lesen und Schreiben verfügt.

## IS:TraceClient - Debugging-Protokollebene des Bildservers {#section-3851f1f68e404430985c629ac80534db}

Protokollebene kann 1, 2, 3 oder 4 sein (Standard ist 2)

Level 1 protokolliert Ereignisse im Zusammenhang mit dem Starten, Herunterfahren und [!DNL Platform Server] von Verbindungen.

Level 2 protokolliert auch das Verbinden mit und Trennen von Quellbildern.

Stufe 3 fügt die Protokollierung von Anfragen für Pixeldaten und deren Versand an die [!DNL Platform Server] hinzu.

Ebene 4 zeichnet alle Nachrichten auf, die von der [!DNL Platform Server] empfangen wurden.

Die Ebenen 3 und 4 sollten nur zu Debugging-Zwecken verwendet werden, da die Protokolldateien groß werden können.

## IS::TraceStatsInterval - Protokollintervall für Bildserver-Statistiken {#section-1d8df96d61044e33a5b2b2b0309c2d59}

Der Bild-Server schreibt in dem von dieser Einstellung angegebenen Intervall Speicherstatistiken in seine Trace-Protokolldatei. Der gültige Bereich ist 5-86.400 Sekunden.
