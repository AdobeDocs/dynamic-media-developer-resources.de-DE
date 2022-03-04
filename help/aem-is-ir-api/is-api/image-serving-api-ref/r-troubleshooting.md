---
description: Dieser Abschnitt enthält Lösungen für Probleme, die gelegentlich beim Image Serving aufgetreten sind.
solution: Experience Manager
title: Fehlerbehebung
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b80d3c9a-a0c4-4944-9f91-e791a072cd5f
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '525'
ht-degree: 1%

---

# Fehlerbehebung{#troubleshooting}

Dieser Abschnitt enthält Lösungen für Probleme, die gelegentlich beim Image Serving aufgetreten sind.

**Allgemein**

ImageServer speichert jetzt ein Installationsprotokoll und einen Sicherungsordner aller Dateien, die während einer Upgrade-Installation geändert wurden. Diese Datei und dieser Ordner befinden sich im Stammverzeichnis des Image Serving-Installationsordners.

**Beim Starten des Image-Servers wird das Startskript mit der Meldung &quot;Start ausstehend&quot; angehalten (nur LINUX).**

Dies kann auf ein Problem mit der Image Serving-Lizenz hindeuten, z. B. eine fehlende Lizenzdatei oder eine abgelaufene temporäre Lizenz. Eine gültige Lizenzdatei muss sich unter [!DNL /usr/local/scene7/licenses].

**Image-Server stürzt oder stürzt ab und die Image-Server-Protokolldatei zeigt an, dass in der Datei nicht genügend Speicherplatz oder eine Ressource vorübergehend nicht verfügbar ist [!DNL IgcVirtualMemory.cpp]&quot;**

Der Grund für diese Fehlermeldung besteht darin, dass Image Server die Menge des konfigurierten Speicherplatzes nicht zugewiesen hat.

* Überprüfen Sie die Einstellung Physischer Speicher unter [!DNL ImageServerRegistry.xml]. Es sollte nicht mehr als 50 % betragen, weniger, wenn andere speicherintensive Anwendungen auf demselben System ausgeführt werden. Der Standardwert ist 20%.
* Stellen Sie sicher, dass der Swap-Speicherplatz auf dem Server mindestens doppelt so groß ist wie der physische RAM. Diese Probleme können durch Einstellungen mit geringem Swap-Speicherplatz verursacht werden.

**Der tatsächliche Speicherplatz, der vom Cache-Ordner verwendet wird, überschreitet ` *[!DNL cache.maxSize]*`festgelegt in[!DNL PlatformServer.conf]**

Dies weist nicht auf ein Problem hin. Der Verwaltungsaufwand für das Dateisystem ist nicht in der Cacheeinstellung des Plattformservers enthalten. Der vom System gemeldete Gesamtbetrag kann wesentlich höher sein als die Einstellung. Es wird empfohlen, doppelt so viel Festplattenspeicher zu reservieren, wie in ` *[!DNL cache.maxSize]*`.

**Beschädigte Bilder in den is-docs-Beispielen**

Dies tritt auf, wenn der Image-Server nicht ausgeführt wird. Sie tritt auch auf, wenn der Katalogstammpfad oder der Pfad des Stammverzeichnisses für Bilder vom Installationsstandard geändert wurde, die Beispielbilder und -kataloge jedoch nicht an die neuen Speicherorte verschoben wurden. Überprüfen Sie den Wert des Image Server Root Path in den Konfigurationsdateien. Verschieben Sie bei Bedarf den Demoordner mit den Beispielbildern in den aktuellen Bildstamm und verschieben Sie [!DNL sample*.*] zum aktuellen Katalogstamm.

In den Beispielen wird außerdem davon ausgegangen, dass bestimmte Einstellungen in [!DNL default.ini] sind Standard (z. B. Verschleierung oder Sperrung darf nicht aktiviert sein).

**Zu viele Cache-Fehler nach umfangreichen Betriebszeiten**

Abhängig von der Servernutzung kann die Leistung verbessert werden, indem die Cachegröße des Platform Server-Speichers erhöht wird, wenn Festplattenspeicher verfügbar ist. Die Einstellungen können durch manuelles Bearbeiten von Konfigurationsdateien geändert werden. Siehe Dokumentation.

**Protokolldateien benötigen zu viel Speicherplatz**

Image Server und Platform Server starten täglich eine neue Protokolldatei. Diese werden standardmäßig in [!DNL *[!DNL install_root]*/ImageServing/logs]. Die Größe der Protokolldatei, die Anzahl der beibehaltenen Protokolle und der Protokollinhalt können konfiguriert werden. Siehe Dokumentation.

**Wenn Sie Anti-Virus-Software auf Ihrem Server installiert haben**

Es wird empfohlen, die Überprüfung auf Image Serving-Verzeichnisse zu deaktivieren. Andernfalls kann das Überprüfen von Lese-/Schreibordnern mit hohem Volumen (wie Cache, Bilder, Schriftarten, Profile und Katalogordner) Probleme verursachen.

**Digimarc verursacht Leistungsprobleme bei Zoombildern**

Verwenden Sie Digimarc nicht für gezoomte Bilder. Die Leistung ist nicht akzeptabel. Erstellen Sie bei Bedarf einen separaten Katalog für Bilder, die zum Zoomen verwendet werden sollen, und deaktivieren Sie Digimarc für diesen Katalog.
