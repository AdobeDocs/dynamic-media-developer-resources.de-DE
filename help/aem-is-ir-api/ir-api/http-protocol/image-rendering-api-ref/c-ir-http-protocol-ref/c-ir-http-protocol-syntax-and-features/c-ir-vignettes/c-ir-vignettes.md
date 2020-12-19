---
description: Vignetten sind Bilder, die mit Scene7 Image Authoring zur Verwendung mit Image Rendering erstellt wurden.
seo-description: Vignetten sind Bilder, die mit Scene7 Image Authoring zur Verwendung mit Image Rendering erstellt wurden.
seo-title: Vignetten
solution: Experience Manager
title: Vignetten
topic: Scene7 Image Serving - Image Rendering API
uuid: 31d6b2b7-57c4-4fef-a498-c357c3724356
translation-type: tm+mt
source-git-commit: 7721cccf3f779f258adcdcf886f7e01111e92be0
workflow-type: tm+mt
source-wordcount: '639'
ht-degree: 0%

---


# Vignetten{#vignettes}

Vignetten sind Bilder, die mit Scene7 Image Authoring zur Verwendung mit Image Rendering erstellt wurden.

IR unterstützt zwei grundlegende Vignettentypen: *2D* und *3D*. Raumszenen sind in der Regel 3D-Vignetten, die Reflexionen wiedergeben können, während die meisten anderen Szenen, wie Bekleidung oder Polsterie, normalerweise 2D-Vignetten sind, die keine Reflektionsrendering-Funktion haben.

Vignetten enthalten eine *Ansicht* und eine Hierarchie von *Objekten*.

Die Ansicht ist der Container für das Hauptbild, freigegebene Beleuchtungskarten, freigegebene Reflektionskarten und andere mit dem gesamten Bild verknüpfte Daten.

Die Objekthierarchie besteht aus *Objektgruppen*, *Standardobjekten* und *überlappenden Objekten*.

Jedes Standardobjekt steuert einen Bereich des Ansicht-Images, der mit einer Graustufenmaske *maskiert* definiert wird. Die Masken von Standardobjekten überlappen sich nie. Standardobjekte können nicht direkt ausgeblendet werden, sie können jedoch teilweise oder vollständig durch überlappende Objekte überdeckt werden. Die meisten oder alle Objekte in einer typischen Vignette sind Standardobjekte.

Überlagern Sie die Objektebene über dem Ansicht-Bild und einander. Die Reihenfolge der Überschneidung wird durch einen dem Objekt zugewiesenen z-Wert definiert. Überschneidungsobjekte sind nützlich, wenn Teile einer Szene dynamisch ein- oder ausgeblendet werden müssen.

Es werden verschiedene Typen von Objekten unterstützt (sowohl Standard- als auch Überlagerungen), von denen jedes einen eigenen Zweck hat:

* **Planare Objekte**  (in 3D-Vignetten) und  **Flachobjekte**  (in 2D-Vignetten) akzeptieren wiederholbare Texturmaterialien. Sie werden in der Regel für Fußböden, Decken und andere flache Oberflächen verwendet, für die nur eine perspektivische Zuordnung erforderlich ist.

* **Fließende** Objekte passen glatt geformte, gekrümmte Oberflächen wie Polsterungen an und werden gelegentlich auch für Bekleidungsobjekte verwendet. Sie können sowohl in 2D- als auch in 3D-Vignetten verwendet werden und, wenn sie vollständig verfasst sind, an der Reflektion teilnehmen.
* **Nicht-texturierbare** Objekte lassen nur Farbänderungen zu. Sie sind in 2D- und 3D-Vignetten zulässig. Sie sind entweder grundsätzlich nicht texturierbar, oder sie können ein planares oder flockenes Objekt mit einem speziellen Flag &quot;Keine Textur&quot;sein. Dies ist in 3D-Vignetten nützlich, um Objekten die Teilnahme am Reflektionsrendering zu ermöglichen, auch wenn das Objekt nur feste Farbmaterialien akzeptiert.
* **Zeichenobjekte** eignen sich am besten für Textobjekte mit Falten und Falten, z. B. Kleidungsstücke. Wie Fließkommaobjekte können sie auch in 2D- und 3D-Vignetten verwendet werden, obwohl die Anwendung in 3D-Vignetten begrenzt ist.
* **Pinnwandobjekte** ähneln planaren Objekten und werden nur in 3D-Vignetten unterstützt. Sie verfügen über spezielle Layoutinformationen, die die Anwendung von zwei verschiedenen Wandveredelungen (oben und unten) und bis zu drei Wandbegrenzungsmaterialien ermöglichen. Bei ordnungsgemäßer Gestaltung fließen die an den Wänden verwendeten Materialien präzise und nahtlos zwischen den angrenzenden Wänden, um realistische Wandrahmen-/Wandbegrenzungen zu gewährleisten. Pinnwandobjekte unterstützen keine Texturdrehung.
* **Mögliche** Objekte sind nur in 3D-Vignetten zulässig. Sie werden zum Erstellen von Küchen- und Badschränken mit komplexen Layoutanforderungen verwendet. Cabinet-Objekte akzeptieren wiederholbare Texturen sowie speziell verfasste *Schrank-Stylesheets*, die skalierbare Schrank-Panel-Bilder enthalten.

Neben den grundlegenden Objektarten werden zwei spezielle Arten von überlappenden Objekten unterstützt:

* **Statische Überschneidungsobjekte** sind Objekte, die keine Materialien akzeptieren. Sie sind in 2D- und 3D-Vignetten zulässig. Sie sind nützlich für entfernbares Zubehör in einer Raumszene, für Schlagschatten hinter renderbaren überlappenden Objekten und ähnliche Anwendungen.
* **Fensterdeckende Rahmen-** Objekte enthalten Platzierungsinformationen zum Anwenden von Fensterverkleidungsstil-Dateien, die unabhängig von der Vignette verfasst werden und zwischen Vignetten freigegeben werden können.

Objekte werden ähnlich wie in einem Dateisystem in *Objektgruppen* erfasst. Die Gruppierung basiert normalerweise auf der Struktur der physischen Objekte, die sie darstellen (z.B. könnte eine Gruppe &quot;Alle Cabinets&quot; &#39;Grundschränke&#39; und &#39;Wandschränke&#39; enthalten). Es sind beliebig viele Gruppenebenen zulässig. Die Gruppierung unterstützt die Anwendung von Materialien auf mehrere gleichartige Objekte.

* [Scene-Koordinaten](c-ir-scene-coordinates.md)
* [Materialauflösung](c-ir-material-resolution.md)
