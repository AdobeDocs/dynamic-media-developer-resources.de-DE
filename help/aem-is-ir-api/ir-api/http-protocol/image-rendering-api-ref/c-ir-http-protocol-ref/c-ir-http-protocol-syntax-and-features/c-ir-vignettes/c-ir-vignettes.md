---
title: Vignetten
description: Vignetten sind Bilder, die mit Dynamic Media Image Authoring zur Verwendung mit dem Bild-Rendering erstellt wurden.
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

Vignetten sind Bilder, die mit Dynamic Media Image Authoring zur Verwendung mit dem Bild-Rendering erstellt wurden.

IR unterstützt zwei grundlegende Arten von Vignetten: *2D* und *3D*. Raumszenen sind typischerweise 3D-Vignetten, die Reflexionen rendern können, während die meisten anderen Szenen, wie Kleidung oder Polsterung, normalerweise 2D-Vignetten sind, die keine Reflexions-Rendering-Fähigkeit haben.

Vignetten enthalten eine *Ansicht* und eine Hierarchie von *Objekten*.

Die Ansicht ist der Container für das Hauptbild, gemeinsame Beleuchtungskarten, gemeinsame Reflexionskarten und andere Daten, die mit dem gesamten Bild verknüpft sind.

Die Objekthierarchie besteht aus *Objektgruppen*, *Standardobjekten* und *Überschneidungsobjekten*.

Jedes Standardobjekt steuert einen Bereich des Ansichtsbilds, der mit einer Graustufen-*(Maske)* wird. Die Masken von Standardobjekten überschneiden sich nie. Standardobjekte können nicht direkt ausgeblendet werden, sie können jedoch teilweise oder vollständig von Überlappungsobjekten abgedeckt werden. Die meisten oder alle Objekte in einer typischen Vignette sind Standardobjekte.

Überlappen Sie Objekte, die sich über dem Ansichtsbild und untereinander befinden. Die Reihenfolge der Überschneidung wird durch einen z-Wert definiert, der dem Objekt zugewiesen wird. Überlappungsobjekte sind nützlich, wenn Teile einer Szene dynamisch ein- oder ausgeblendet werden müssen.

Es werden verschiedene Objekttypen unterstützt (Standard und Überschneidung), von denen jedes einen eigenen Zweck hat:

* **Planare Objekte** (in 3D-Vignetten) und **flache Objekte** (in 2D-Vignetten) akzeptieren wiederholbare Texturmaterialien. Sie werden in der Regel für Böden, Arbeitsplatten und andere flache Oberflächen verwendet, die nur eine perspektivische Zuordnung erfordern.
* **Fließlinienobjekte** zeichnen glatt geformte gekrümmte Oberflächen wie Polsterungen ab und werden gelegentlich auch für Bekleidungsobjekte verwendet. Sie können sowohl in 2D- als auch in 3D-Vignetten verwendet werden und, falls vollständig verfasst, am Reflexions-Rendering teilnehmen.
* **Nicht texturierbare Objekte** erlauben nur Farbwechsel. Sie sind sowohl in 2D- als auch in 3D-Vignetten erlaubt. Sie sind entweder von Natur aus nicht texturierbar oder sie können ein ebenes oder Fließlinienobjekt mit einem speziellen „Keine Textur“-Flag sein. Diese Methode ist in 3D-Vignetten nützlich, um Objekten die Teilnahme am Reflexions-Rendering zu ermöglichen, auch wenn das Objekt nur einfarbige Materialien akzeptiert.
* **Skizzenobjekte** eignen sich am besten für Textobjekte mit Falten und Fältchen, z. B. Kleidungsstücke. Wie Flowline-Objekte können sie in 2D- und 3D-Vignetten verwendet werden, obwohl die Anwendung in 3D-Vignetten begrenzt ist.
* **Wandobjekte** ähneln planaren Objekten und werden nur in 3D-Vignetten unterstützt. Sie verfügen über spezielle Layoutinformationen, die den Einsatz von zwei verschiedenen Wandverkleidungen (oben und unten) und bis zu drei Wandrandmaterialien ermöglichen. Bei ordnungsgemäßer Erstellung fließen Materialien, die auf Wände aufgetragen werden, genau und nahtlos zwischen benachbarten Wänden, für realistische Tapeten-/Wandrahmenanwendungen. Wandobjekte unterstützen keine Texturrotation.
* **Schrankobjekte** sind nur in 3D-Vignetten zulässig. Sie werden verwendet, um Küchen- und Badeschränke mit komplexen Layout-Anforderungen zu erstellen. Cabinet-Objekte akzeptieren wiederholbare Texturen und speziell erstellte *Cabinet-Style-Dateien* mit in der Größe veränderbaren Cabinet-Panel-Bildern.

Zusätzlich zu den einfachen Objekttypen werden zwei spezielle Arten von Überschneidungsobjekten unterstützt:

* **Statische Überlappungsobjekte** sind Objekte, die keine Materialien akzeptieren. Sie sind sowohl in 2D- als auch in 3D-Vignetten erlaubt. Sie eignen sich für entfernbares Zubehör in einer Raumszene, für Schlagschatten hinter gerenderbaren Überlappungsobjekten und ähnliche Anwendungen.
* **Fensterabdeckungs-Rahmenobjekte** bieten Platzierungsinformationen zum Anwenden von Fensterabdeckungs-Stildateien, die unabhängig von der Vignette erstellt wurden und mit Vignetten geteilt werden können.

Objekte werden in &quot;*&quot; erfasst* ähnlich einem Dateisystem. Die Gruppierung basiert normalerweise auf der Struktur der physischen Objekte, die sie repräsentieren (z. B. kann eine Gruppe „Alle Schränke“ „Basis-Schränke“ und „Wand-Schränke“ enthalten). Eine beliebige Anzahl von Gruppenebenen ist zulässig. Die Gruppierung unterstützt die Anwendung von Materialien auf mehrere ähnliche Objekte.

* [Szenenkoordinaten](c-ir-scene-coordinates.md)
* [Materialauflösung](c-ir-material-resolution.md)
