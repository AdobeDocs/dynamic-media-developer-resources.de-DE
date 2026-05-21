---
title: Vorab-Bearbeitung von Anfragen
description: Das Bild-Rendering bietet einen einfachen Anforderungs-Präprozessor, der auf Übereinstimmungs- und Ersetzungsregeln für reguläre Ausdrücke basiert.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 79a358db-0fd6-4327-a305-b0b38ad62050
TQID: 'https://experienceleague.adobe.com/zs4izZzuO7u6wYOPmdd8AT7r4q-cUFXWUlB1MW6aV0Y'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 220
ht-degree: 0%

---

# Vorab-Bearbeitung von Anfragen{#request-pre-processing}

Das Bild-Rendering bietet einen einfachen Anforderungs-Präprozessor, der auf Übereinstimmungs- und Ersetzungsregeln für reguläre Ausdrücke basiert.

Regelkollektionen (Regelsätze) können an jeden Materialkatalog angehängt werden, auch an den Standardkatalog. Regeln werden mit XML-formatierten Dateien angegeben.

Regeln für die Anfragevorverarbeitung können den Pfad und die Abfrageanteile von Anfragen ändern, bevor sie vom Bild-Rendering-Parser verarbeitet werden. Zu diesem Konzept gehört die Bearbeitung des Pfads, das Hinzufügen von Befehlen, das Ändern von Befehlswerten und das Anwenden von Vorlagen oder Makros. Regeln können auch verwendet werden, um bestimmte Funktionen zu konfigurieren und zu überschreiben, die normalerweise nur mit Katalogattributen gesteuert werden, z. B. die Festlegung der standardmäßigen Größe des Antwortbildes oder die Beschränkung des HTTP-Service auf bestimmte Client-IP-Adressen.

Regeln zur Anfragevorverarbeitung eignen sich für verschiedene Anwendungen, von denen einige unten aufgeführt sind:

* Implementieren Sie *Mechanismus &quot;* Pfade“, der die Neuzuordnung des Anfragepfads zu Datei-, FTP- und HTTP-Pfaden ermöglicht.
* Deaktivieren der Verwendung von CPU-intensiven Befehlen, um Servermissbrauch zu verhindern.
* Steuern der Bildqualitätseinstellungen (z. B. JPEG-Qualität oder Scharfzeichnung) je nach Anfragepfad oder Bildname.

Ausführliche Informationen zum Erstellen, Verwenden und Verwalten von Regelsätzen finden Sie in der Referenz zu Regelsätzen .

Siehe auch Regelsatzreferenz, Attribut::RuleSetFile
