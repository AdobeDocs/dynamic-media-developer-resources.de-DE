---
title: Vignetten
description: Vignetten sind Bilder, die mit Dynamic Media Image Authoring für die Verwendung mit Image Rendering erstellt wurden.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5e1be99c-58c0-4e3c-bc57-7be5fa25ccef
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '622'
ht-degree: 0%

---

# Vignetten{#vignettes}

Vignetten sind Bilder, die mit Dynamic Media Image Authoring für die Verwendung mit Image Rendering erstellt wurden.

IR unterstützt zwei grundlegende Vignettentypen: *2D* und *3 D*. Raumszenen sind in der Regel 3D-Vignetten, die Reflexionen rendern können, während die meisten anderen Szenen, wie Kleidung oder Polster, normalerweise 2D-Vignetten sind, die nicht über Reflektion-Rendering-Fähigkeiten verfügen.

Vignetten enthalten eine *Ansicht* und eine Hierarchie *Objekte*.

Die Ansicht ist der Container für das Hauptbild, gemeinsame Beleuchtungskarten, gemeinsame Reflektionskarten und andere Daten, die mit dem gesamten Bild verknüpft sind.

Die Objekthierarchie besteht aus *Objektgruppen*, *Standardobjekte* und *überlappende Objekte*.

Jedes Standardobjekt steuert einen Bereich des Ansichtsbilds, der in Graustufen definiert ist *mask*. Die Masken von Standardobjekten überschneiden sich nie. Standardobjekte können nicht direkt ausgeblendet werden, sie können jedoch teilweise oder vollständig durch überlappende Objekte überdeckt werden. Die meisten oder alle Objekte in einer typischen Vignette sind Standardobjekte.

Überlagern Sie die Objektebene über dem Ansichtsbild untereinander. Die Reihenfolge der Überschneidung wird durch einen z-Wert definiert, der dem Objekt zugewiesen ist. Überlagerungsobjekte sind nützlich, wenn Teile einer Szene dynamisch ein- oder ausgeblendet werden müssen.

Es werden verschiedene Arten von Objekten unterstützt (sowohl Standard- als auch Überlagerungsobjekte), von denen jede einen eigenen Zweck hat:

* **Planobjekte** (in 3D-Vignetten) und **Flachobjekte** (in 2D-Vignetten) wiederholbare Texturmaterialien akzeptieren. Sie werden in der Regel für Fußböden, Decken und andere flache Oberflächen verwendet, für die nur eine Perspektivzuordnung erforderlich ist.
* **Flowline-Objekte** flach geformte, gekrümmte Oberflächen wie Polstermöbel und gelegentlich auch für Bekleidungsobjekte verwendet werden. Sie können sowohl in 2D- als auch in 3D-Vignetten verwendet werden und, wenn sie vollständig erstellt sind, an Reflektion-Rendering teilnehmen.
* **Nicht texturierbare Objekte** lassen nur Farbänderungen zu. Sie sind sowohl in 2D- als auch in 3D-Vignetten zulässig. Sie sind von Natur aus nicht texturierbar, oder sie können ein planares oder flockenes Objekt mit einer speziellen Markierung &quot;Keine Textur&quot; sein. Diese Methode ist in 3D-Vignetten nützlich, um Objekten die Möglichkeit zu geben, an der Reflektion teilzunehmen, obwohl das Objekt nur Materialien mit fester Farbe akzeptiert.
* **Objekte zeichnen** werden am besten für Textobjekte mit Falten und Falten wie Bekleidungsartikeln verwendet. Wie Flowline-Objekte können sie in 2D- und 3D-Vignetten verwendet werden, obwohl die Anwendung in 3D-Vignetten eingeschränkt ist.
* **Pinnwandobjekte** ähneln flachen Objekten und werden nur in 3D-Vignetten unterstützt. Sie verfügen über spezielle Layoutinformationen, die die Anwendung von zwei verschiedenen Wandveredelungen (oben und unten) und bis zu drei Wandbegrenzungsmaterialien ermöglichen. Bei ordnungsgemäßer Ausführung fließen die auf Wände angewendeten Materialien genau und nahtlos zwischen benachbarten Wänden, um realistische Hintergrundbilder/Wandrahmen zu erhalten. Pinnwandobjekte unterstützen keine Texturrotation.
* **Kabinenobjekte** sind nur in 3D-Vignetten zulässig. Sie werden verwendet, um Küchen- und Badschränke mit komplexen Layoutanforderungen zu erstellen. Kabinettobjekte akzeptieren wiederholbare Texturen und speziell verfasste Objekte *Kabinenstil-Dateien* enthält skalierbare Schachtelbilder.

Neben den grundlegenden Objekttypen werden zwei spezielle Arten von überlappenden Objekten unterstützt:

* **Statische überlappende Objekte** sind Objekte, die keine Materialien annehmen. Sie sind sowohl in 2D- als auch in 3D-Vignetten zulässig. Sie eignen sich für entfernbares Zubehör in einer Raumszene, für Ablegen von Schatten hinter renderbaren Überschneidungsobjekten und ähnliche Anwendungen.
* **Fenster für Rahmenobjekte** Informationen zur Platzierung für die Anwendung von Stildateien im Fensterbereich, die unabhängig von der Vignette erstellt werden und von Vignetten gemeinsam genutzt werden können.

Objekte werden in *Objektgruppen*, ähnlich einem Dateisystem. Die Gruppierung basiert normalerweise auf der Struktur der physischen Objekte, die sie darstellen (z. B. könnte eine Gruppe &quot;Alle Kabinette&quot; &#39;Grundschränke&#39; und &#39;Wandschränke&#39; enthalten). Jede Anzahl von Gruppenebenen ist zulässig. Die Gruppierung unterstützt die Anwendung von Materialien auf mehrere gleichartige Objekte.

* [Scene-Koordinaten](c-ir-scene-coordinates.md)
* [Materialauflösung](c-ir-material-resolution.md)
