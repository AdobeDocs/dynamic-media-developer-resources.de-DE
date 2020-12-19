---
description: Dieser Abschnitt enthält Lösungen für Probleme, die gelegentlich mit Image Serving aufgetreten sind.
seo-description: Dieser Abschnitt enthält Lösungen für Probleme, die gelegentlich mit Image Serving aufgetreten sind.
seo-title: Fehlerbehebung
solution: Experience Manager
title: Fehlerbehebung
topic: Scene7 Image Serving - Image Rendering API
uuid: 39fdaf86-004b-4553-bde0-0367f3ef76b8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '540'
ht-degree: 1%

---


# Fehlerbehebung{#troubleshooting}

Dieser Abschnitt enthält Lösungen für Probleme, die gelegentlich mit Image Serving aufgetreten sind.

**Allgemein**

ImageServer speichert jetzt ein Installationsprotokoll und einen Sicherungsordner aller Dateien, die während der Installation der Aktualisierung geändert wurden. Diese Datei und dieser Ordner befinden sich im Stammverzeichnis des Image Serving-Installationsordners.

**Beim Starten des Image-Servers wird das Startskript mit der Meldung &quot;Beginn ausstehend&quot;angehalten (nur LINUX)**

Dies kann auf ein Problem mit der Image Serving-Lizenz hindeuten, z. B. eine fehlende Lizenzdatei oder eine abgelaufene temporäre Lizenz. Eine gültige Lizenzdatei muss sich unter [!DNL /usr/local/scene7/licenses] befinden.

**Image-Server stürzt oder stürzt ab, und die Image-Server-Protokolldatei weist darauf hin, dass nicht genügend Speicherplatz oder &quot;Ressource vorübergehend nicht in Datei verfügbar&quot;vorhanden ist  [!DNL IgcVirtualMemory.cpp]**

Der Grund für diese Fehlermeldung ist, dass Image Server nicht den für die Verwendung konfigurierten Arbeitsspeicher zugewiesen hat.

* Überprüfen Sie die Einstellung Physikalischer Speicher unter [!DNL ImageServerRegistry.xml]. Es sollte nicht mehr als 50 % betragen, weniger, wenn andere speicherintensive Anwendungen auf demselben System ausgeführt werden. Der Standardwert ist 20%.
* Stellen Sie sicher, dass der Swap-Speicherplatz auf dem Server mindestens der Dublette des physischen RAM-Speichers entspricht. Die Einstellungen für den geringen Austausch können dieses Problem verursachen.

**Der vom Cache-Ordner verwendete tatsächliche Speicherplatz überschreitet die  ` *[!DNL cache.maxSize]*`Einstellung in[!DNL PlatformServer.conf]**

Das deutet nicht auf ein Problem hin. Der Dateisystemaufwand ist nicht in der Einstellung für den Datenträgercache des Plattformservers enthalten. Der vom System gemeldete Gesamtbetrag kann wesentlich höher sein als die Einstellung. Es wird empfohlen, doppelt so viel Speicherplatz wie in ` *[!DNL cache.maxSize]*` angegeben zu reservieren.

**Fehlerhafte Bilder in den i-docs-Beispielen**

Dies tritt auf, wenn Image Server nicht ausgeführt wird. Es tritt auch auf, wenn der Katalogstammpfad oder der Pfad des Bild-Stammordners vom Standard für die Installation geändert wurde, die Beispielbilder und -kataloge jedoch nicht an die neuen Speicherorte verschoben wurden. Überprüfen Sie den Wert für den Image-Server-Stammpfad in den Konfigurationsdateien. Verschieben Sie bei Bedarf den demo-Ordner mit den Beispielbildern in den aktuellen Image-Stammordner und verschieben Sie [!DNL sample*.*] in den aktuellen Katalog-Stammordner.

In den Beispielen wird auch davon ausgegangen, dass bestimmte Einstellungen in [!DNL default.ini] Standard sind (z. B. Verschleierung oder Sperrung darf nicht aktiviert werden).

**Zu viele Cache-Fehler nach längerer Betriebszeit**

Abhängig von der Servernutzung kann die Leistung verbessert werden, indem die Cache-Größe des Plattformservers erhöht wird, wenn Speicherplatz verfügbar ist. Einstellungen können durch manuelles Bearbeiten von Konfigurationsdateien geändert werden. Siehe Dokumentation.

**Protokolldateien nehmen zu viel Speicherplatz in Anspruch**

Der Image-Server- und Plattformserver-Beginn erhält täglich eine neue Protokolldatei. Standardmäßig werden diese in [!DNL *[!DNL install_root]*/ImageServing/logs] platziert. Die Größe der Protokolldatei, die Anzahl der gespeicherten Protokolle und der Protokollinhalt können konfiguriert werden. Siehe Dokumentation.

**Wenn Sie Anti-Virus-Software auf Ihrem Server installiert haben**

Es wird empfohlen, die Suche nach Image Serving-Ordnern zu deaktivieren. Andernfalls führt das Scannen von Lese-/Schreibordnern mit hohem Volumen (z. B. Cache, Bilder, Schriftarten, Profile und Katalogordner) zu Problemen.

**Digimarc verursacht Leistungsprobleme bei Zoombildern**

Verwenden Sie Digimarc nicht auf Bildern, die gezoomt werden sollen. Die Leistung wird nicht akzeptabel sein. Erstellen Sie bei Bedarf einen eigenen Katalog für Bilder, die zum Zoomen verwendet werden sollen, und deaktivieren Sie Digimarc für diesen Katalog.
