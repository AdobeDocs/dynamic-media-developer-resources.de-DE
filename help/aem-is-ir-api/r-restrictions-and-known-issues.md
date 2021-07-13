---
description: Es gibt einige Einschränkungen und bekannte Probleme, die bei der Verwendung von Dynamic Media Image Serving berücksichtigt werden sollten.
solution: Experience Manager
title: Einschränkungen und bekannte Probleme
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fd32456b-9d99-4e82-a61c-2fc4d7030630
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '1235'
ht-degree: 0%

---

# Einschränkungen und bekannte Probleme{#restrictions-and-known-issues}

Es gibt einige Einschränkungen und bekannte Probleme, die bei der Verwendung von Dynamic Media Image Serving berücksichtigt werden sollten.

## Dokumentationsfehler {#section-b1579410b11e41e488c7de9ecc7e8d5c}

* Die Zeilenanzahl überschreitet nicht das Maximum der Einstellung `\copyfitmaxlines` und die Anzahl der expliziten Zeilen in der Texteingabe.
* Übereinstimmende geschweifte Klammern und Klammern sind in Bildsets erforderlich. Wenn geschweifte Klammern und Klammern nicht übereinstimmen, müssen sie URL-kodiert sein.
* Der Warnhinweis zur globalen serverseitigen Antwortzeit enthält Fehlerantworten.
* Der Befehl `id=` ist derzeit erforderlich, wenn der Befehl `rect=` mit einer Bild- oder Maskenanforderung verwendet wird.

## Bekannte Unterschiede zwischen textPs= und text= {#section-16ede4c13a7648feb0d2fc93341fd4aa}

* Synthetisch kursiv werden weniger geslandet als bei Verwendung von `text=`.
* Unterstreichen ist etwas niedriger und dünner als bei Verwendung von `text=`.
* `\expnd` und  `\expndtw` verwendet mit hohen negativen Werten führen dazu, dass bei Verwendung von  `text=`aufeinander folgende Zeichen gesetzt werden.

* `\charscaley` unterscheidet sich von der Verwendung,  `text=` wirkt sich jedoch nicht auf die Zeilenhöhe aus.

* Wenn die letzte Textzeile nicht passt, wird die gesamte Zeile abgelegt, anstatt als Cutoff angezeigt zu werden.
* `\slmult` und  `\sl` verhalten sich anders als MS Word und  `text=`, sie treten einfach für die aktuellen und nachfolgenden Absätze in Kraft.

* `\sb` gilt für den ersten Absatz sowohl für MS Word als auch  `text=`, Adobe InDesign und Photoshop tun dies nicht.

* `\sa` gilt für den letzten Absatz sowohl für MS Word als auch  `text=`, Adobe InDesign und Photoshop tun dies nicht.

## Abwärtskompatibilität {#section-a76842f751944f4fb664af296d064122}

* Das Escapen des Unterstrichzeichens ( `\_`) in einer RTF-Zeichenfolge funktioniert nicht mit allen Schriftarten, die `textPs=` verwenden

* Unterstützt nicht von Groß-/Kleinschreibung abhängige Makrobearbeitung.
* Der Catalog-Cache wurde von 60 auf 10 Sekunden reduziert.
* Die Umleitungsfunktion für Fehler leitet jetzt nur Anforderungen weiter, die auf beschädigte Bilder, Schriftarten, Farbprofile und Bilder verweisen, die in einem Katalog veröffentlicht, aber nicht auf der Festplatte gefunden werden.
* `posN=`,  `anchor=`,  `anchorN=`,  `origin=` und geben  `originN=` jetzt einen Parsing-Fehler zurück, wenn einer der Modifikatorwerte größer als 2147483648 ist.

* Die Kodierung verschachtelter Anforderungen wird nicht unterstützt. Übergang zum neuen Verhalten und Dekodierung verschachtelter Anforderungswerte in URL-Anforderungen auf Ihrer Site und in Unternehmenskatalogen.
* DefaultImage wendet bei Verwendung von `req=tmb` jetzt Attribute für Miniaturansichten an.
* In früheren Versionen mit `flip=` wurde das Bild nie neu positioniert, unabhängig davon, welcher Ankerpunkt verwendet wurde.

## Einschränkungen für Bibliotheken von Drittanbietern {#section-79768b96bf634e44ab672c5b893f343d}

Die Digimarc-Bibliothek weigert sich, ein Digimarc-Wasserzeichen auf ein Bild anzuwenden, wenn bereits eines erkannt wurde. Wenn an einem Primärbild ausreichend bearbeitet wird, kann die Digimarc-Bibliothek weiterhin erkennen, dass das Wasserzeichen angewendet wurde. Diese Informationen können jedoch möglicherweise nicht gelesen werden. Dies führt zu einem neuen Bild, bei dem die ursprünglichen Digimarc-Informationen, die auf das Originalbild angewendet wurden, nicht abgerufen werden können. Image Serving kann jetzt das im Firmenkatalog definierte Digimarc-Wasserzeichen anwenden.

## Einschränkungen für Image Serving und Image Rendering {#section-f836cb40ae2d4f32a9cf7ebda4d91bae}

* Image Serving und Image Rendering nutzen möglicherweise nicht alle CPUs, wenn mehr als 4 CPUs verfügbar sind. Simulieren Sie Ihren Traffic auf diesen Computern, um zu sehen, wie vorteilhaft es mit mehr als 4 CPUs ist.
* Remote-URLs, die eine Umleitung zurückgeben (HTTP-Status 301, 302 oder 303), werden abgelehnt.
* Bei der Konfiguration von `errorRedirect.rootUrl` muss die in dieser Eigenschaft definierte IP-Adresse im ruleSet `<addressfilter>` -Tag-Wert auf diesem Server enthalten sein.

   *Beispiel*:

   Server A hat `errorRedirect.rootUrl=10.10.10.10` definiert.

   Server B mit der IP-Adresse 10.10.10.10 legt den Tag-Wert `<addressfilter>` in der ruleSet-Datei so fest, dass er seine IP-Adresse enthält (10.10.10.10).

* Punkttext und Textpfad mit Positionierung können Beschneiden aufweisen.
* `text=` gilt nur  `\sa` und  `\sb` für den gesamten Textblock und nicht pro Absatz.

* Wenn Sie ein in der URL definiertes Unternehmen und ein anderes für den Modifikator `src=` oder `mask=` definiertes Unternehmen verwenden, müssen Sie dem für `src=` oder `mask=` definierten Unternehmen einen Schrägstrich voranstellen, damit dieses Anforderungsformular funktioniert.

   *Beispiel*:

   `/is/image/MyCompany?src=/YourCompany/MyImage` .

   Statt: `/is/image/MyCompany?src=YourCompany/MyImage` .

* Nicht-Pyramided-Tiff- oder Vignettenanforderungen erzeugen eine ähnliche Fehlermeldung wie

   *&quot;Bild  `C:\Program Files\Scene7\ImageRendering\resources\MyVignette.vnt` hat keinen gültigen DSF und Bereich von 2,25MPixel überschreitet maximal 2MPixel&quot;* .

   Best Practice ist die Verwendung von Pyramidenzecken und Vignetten. Wenn Sie nicht-pyramidenförmige Zecken oder Vignetten benötigen, befolgen Sie die unten stehenden Anweisungen, um die Größenbeschränkung zu erhöhen.

   *Problemumgehung*:

   Erhöhen Sie für das Rendern von nicht pyramidierten Vignetten den Eigenschaftswert für IrMaxNonPyrVignetteSize in der Konfigurationsdatei [!DNL install_root/ImageServing/bin/ImageServerRegistry.xml].

   Erhöhen Sie für nicht pyramidenförmige TIFF-Dateien für Image Serving den Eigenschaftswert für `MaxNonDsfSize` in der Konfigurationsdatei [!DNL install_root/ImageServing/bin/ImageServerRegistry.xml].

* Adobe Photoshop CS3 speichert keine PSD-Dateien mit Ebenen standardmäßig als Composite-Bild.

   *Symptome*:

   Die PSD-Datei mit Adobe Photoshop CS3-Ebenen wird schwarz mit dem Text &quot;Diese Photoshop-Datei mit Ebenen wurde nicht mit einem zusammengesetzten Bild gespeichert&quot;angezeigt. für das Image Serving-Antwortbild oder in IPS.

   *Behelfslösung*:

   Speichern Sie die Adobe Photoshop CS3-Datei mit eingeschalteter Option zur Maximierung der Kompatibilität.

* Wenn Sie einem CMYK-/JPEG-Antwortbild ein ICC-Profil zuweisen, werden die Farben in einigen Browsern invertiert.*Problemumgehung*:

   Ändern Sie das Antwortbildformat mithilfe von `fmt=`.

* Die Größe der HTTP-Antwort-Bilddaten nach der Komprimierung, einschließlich des Datei-Headers, ist auf 16 MB beschränkt.
* &quot; ...&quot; ist in keinem Pfadelement in HTTP-Anforderungen zulässig.
* Die Deinstallation kann vom Benutzer erstellte oder geänderte Datei aus *[!DNL install_root]* oder einem beliebigen Unterordner entfernen. Kopieren Sie diese Dateien vor der Deinstallation an einen anderen Speicherort.

## Einschränkungen, die nur für das Image Serving gelten {#section-b08ad535e4454265b8157dec244c4faf}

* Vordergrundfarben im RTF-Befehl ( `\cf`) werden für FotoFont-Text nicht unterstützt.
* Die fett, kursiv und fett/kursiv synchronisierte Formatierung wird als Fehler für FotoFont-Text zurückgewiesen.
* Vertikaler Textfluss wird für FotoFont-Text nicht unterstützt.
* PNG-Bilder mit 16bpc werden für FotoFont-Text nicht unterstützt.
* Farbkorrekturen für PNG-Bilder mit eingebetteten Farbprofilen verwenden hartcodierte Optionen. Rendering Intent ist relativ farbmetrisch und die Blackpoint-Kompensation ist für FotoFont-Text aktiviert.
* Die dateibasierte Suche wird nicht unterstützt, wenn die Übersetzung des Gebietsschemas in der Datei [!DNL ini] des Unternehmens aktiviert ist.
* Image Serving schreibt nicht geschlossene Photoshop-Pfade nicht richtig.
* Image Serving unterstützt derzeit nicht die Verarbeitung von TIFF-Dateien, die mit Adobe Media Encoder 4.0.1 oder früher exportiert wurden. Adobe Media Encoder ist in Premiere Pro CS4, After Effects CS4 und Creative Suite 4 Production Premium enthalten.
* Die Verwendung von `text=` mit selbstdimensionierenden Ebenen unterstützt keine RTF-Zeichenfolgen, die mehr als eine Einstellung für die Zeilenausrichtung verwenden.

   *Beispiel*

   RTF-Zeichenfolgen können für eine selbstskalierende Textebene nicht die linke und die rechte Zeilenausrichtung verwenden.

* SVG verfügt über eine eigene Eigenschaft für den Schriftartensuchpfad referenzierter Schriftarten, die nicht in die SVG-Datei eingebettet sind.

   *Symptome*

   Gerenderte SVG-Bilder, die Schriftdefinitionen enthalten, verwenden die falsche Schriftart.

   *Behelfslösung*

   Legen Sie die Eigenschaft `svgProvider.fontRoot=` in [!DNL install_root/ImageServing/conf/PlatformServer.conf] fest.

* Zuschneiden verwendet derzeit `bgColor=` anstelle von `color=`, um einen neuen erweiterten Bereich auszufüllen.

* Die Farbkonvertierung ist möglicherweise nicht korrekt, wenn `bgColor=` nicht mit dem Basisfarbraum mit Farbprofilen übereinstimmt.
* Externe Ebeneneffekte werden nicht gerendert, wenn die Ebene keine Masken- oder Alphakatdaten aufweist.

## Einschränkungen, die nur für das Bild-Rendering gelten {#section-4c6949e797174607a3d1ab4d3d4a725a}

* Dekore und Wandmaterialien sind nicht abnehmbar.
* Die Größe der Texturen ist relativ zur Größe der Vignettenansicht begrenzt. In seltenen Fällen kann die Standardgrenze von 425 % der Ansichtsgröße eine Anwendung beeinträchtigen, die sehr große, nicht wiederholbare Texturen verwendet. Wenn es nicht möglich ist, die Anwendung oder den Inhalt innerhalb der vordefinierten Einschränkungen zu ändern, kann der Prozentsatz wie folgt erhöht werden. Öffnen Sie mithilfe eines Texteditors [!DNL install_root/ImageServing/conf/ImageServerRegistry.xml], suchen Sie `IrMaxTextureSizeFactor` und geben Sie einen neuen Prozentwert ein. Die Änderung wird sofort wirksam, ohne den Image-Server neu zu starten.

* Die JavaScript-Engines in Netscape- und Opera-Cache-Antwortdaten, selbst wenn der nocache-Header festgelegt ist. Dies behindert das ordnungsgemäße Funktionieren von stateful-Anfragen.

   *Behelfslösung*

   Hängen Sie einen Zeitstempel oder eine andere eindeutige Kennung an die Anforderungszeichenfolge an, z. B. `"&.ts=currentTime`.

## Einschränkungen nur für Dienstprogramme {#section-906a6b2378154b3da122b2332983f7a5}

`ImageConvert`stürzt manchmal mit einem Segmentierungsfehler ab, wenn mit einer  `control-c`gestoppt wird.
