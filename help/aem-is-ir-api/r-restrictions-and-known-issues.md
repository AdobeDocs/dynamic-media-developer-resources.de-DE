---
description: Es gibt einige Einschränkungen und bekannte Probleme, die bei der Verwendung von Dynamic Media-Bildbereitstellung berücksichtigt werden sollten.
solution: Experience Manager
title: Einschränkungen und bekannte Probleme
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fd32456b-9d99-4e82-a61c-2fc4d7030630
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '1233'
ht-degree: 0%

---

# Einschränkungen und bekannte Probleme{#restrictions-and-known-issues}

Es gibt einige Einschränkungen und bekannte Probleme, die bei der Verwendung von Dynamic Media-Bildbereitstellung berücksichtigt werden sollten.

## Dokumentationsfehler {#section-b1579410b11e41e488c7de9ecc7e8d5c}

* Die Anzahl der Zeilen überschreitet nicht den Maximalwert der `\copyfitmaxlines` und die Anzahl der expliziten Zeilen in der Texteingabe.
* In Bildsets sind übereinstimmende geschweifte Klammern und Klammern erforderlich. Wenn geschweifte Klammern und Klammern nicht übereinstimmen, müssen sie URL-kodiert werden.
* Die Warnung zur globalen Reaktionszeit auf Serverseite enthält Fehlerantworten.
* Der Befehl `id=` ist derzeit erforderlich, wenn der Befehl `rect=` mit einer Bild- oder Maskenanfrage verwendet wird.

## Bekannte Unterschiede textPs= vs text= {#section-16ede4c13a7648feb0d2fc93341fd4aa}

* Synthetische Kursivformatierung wird weniger geneigt als bei Verwendung von `text=`.
* Die Unterstreichung ist etwas geringer und dünner als bei der Verwendung von `text=`.
* `\expnd` und `\expndtw`, die mit hohen negativen Werten verwendet werden, führen dazu, dass Zeichen bei der Verwendung von `text=` vor einander platziert werden.

* `\charscaley` wird anders skaliert als bei Verwendung von `text=`, hat jedoch keinen Einfluss auf die Zeilenhöhe.

* Wenn die letzte Textzeile nicht passt, wird die gesamte Zeile eingefügt, anstatt als Abgeschnitten angezeigt zu werden.
* `\slmult` und `\sl` sich anders als MS Word und `text=` verhalten, werden sie einfach für den aktuellen und die nachfolgenden Absätze wirksam.

* `\sb` gilt für den ersten Absatz sowohl für MS Word als auch für `text=`, Adobe InDesign und [!DNL Photoshop] tun dies nicht.

* `\sa` gilt für den letzten Absatz sowohl für MS Word als auch für `text=`, Adobe InDesign und [!DNL Photoshop] tun dies nicht.

## Abwärtskompatibilität {#section-a76842f751944f4fb664af296d064122}

* Das Maskieren des Unterstrichs (`\_`) in einer RTF-Zeichenfolge funktioniert nicht bei allen Schriftarten, die `textPs=` verwenden

* Unterstützung der Makrobehandlung ohne Berücksichtigung der Groß-/Kleinschreibung.
* Der Katalog-Cache wurde von 60 auf 10 Sekunden reduziert.
* Die Fehlerumleitungsfunktion leitet jetzt nur noch Anfragen um, die auf beschädigte Bilder, Schriftarten, Farbprofile und Bilder verweisen, die in einem Katalog veröffentlicht, aber nicht auf der Festplatte gefunden wurden.
* `posN=`, `anchor=`, `anchorN=`, `origin=` und `originN=` geben jetzt einen Analysefehler zurück, wenn einer der Modifikatorwerte größer als 2147483648 ist.

* Die Codierung verschachtelter Anfragen wird nicht unterstützt. Wechseln Sie zum neuen Verhalten und heben Sie die Kodierung aller verschachtelten Anfragewerte auf, die in URL-Anfragen auf Ihrer Site und in Ihren Unternehmenskatalogen enthalten sind.
* DefaultImage wendet bei der Verwendung von `req=tmb` jetzt Attribute für Miniaturansichten an.
* In früheren Versionen mit `flip=` wurde das Bild unabhängig vom Ankerpunkt nie neu positioniert.

## Einschränkungen für Bibliotheken von Drittanbietern {#section-79768b96bf634e44ab672c5b893f343d}

Die Digimarc-Bibliothek weigert sich, ein Digimarc-Wasserzeichen auf ein Bild anzuwenden, wenn bereits ein solches erkannt wurde. Wenn ein Primärbild ausreichend bearbeitet wird, kann die Digimarc-Bibliothek möglicherweise weiterhin erkennen, dass das Wasserzeichen angewendet wurde. Sie kann diese Informationen jedoch möglicherweise nicht lesen. Dies führt zu einem neuen Bild, bei dem die ursprünglichen Digimarc-Informationen, die auf das Originalbild angewendet wurden, nicht abgerufen werden können. Image Serving kann jetzt das im Firmenkatalog definierte Digimarc-Wasserzeichen anwenden.

## Einschränkungen für die Bereitstellung von Bildern und das Rendern von Bildern {#section-f836cb40ae2d4f32a9cf7ebda4d91bae}

* Wenn mehr als vier CPUs verfügbar sind, nutzen Image Serving und Image Rendering möglicherweise nicht alle CPUs. Simulieren Sie Ihren Traffic auf diesen Computern, um zu sehen, wie vorteilhaft er mit mehr als 4 CPUs ist.
* Remote-URLs, die eine Umleitung zurückgeben (HTTP-Status 301, 302 oder 303), werden abgelehnt.
* Beim Konfigurieren von `errorRedirect.rootUrl` muss die in dieser Eigenschaft definierte IP-Adresse auf diesem Server in den `<addressfilter>`-Tag-Wert des Regelsatzes aufgenommen werden.

  *Beispiel*:

  Server A hat `errorRedirect.rootUrl=10.10.10.10` definiert.

  Server B mit der IP-Adresse 10.10.10.10 setzt den `<addressfilter>`-Tag-Wert in der Regelsatzdatei auf seine IP-Adresse (10.10.10.10).

* Punkttext und Textpfad mit Positionierung können einen Ausschnitt aufweisen.
* `text=` gilt nur für `\sa` und `\sb` für den gesamten Textblock und nicht pro Absatz.

* Wenn Sie ein in der URL definiertes Unternehmen und ein anderes für den Modifikator `src=` oder `mask=` definiertes Unternehmen verwenden, müssen Sie dem für `src=` oder `mask=` definierten Unternehmen einen Schrägstrich voranstellen, damit diese Form der Anforderung funktioniert.

  *Beispiel*:

  `/is/image/MyCompany?src=/YourCompany/MyImage` .

  anstelle von: `/is/image/MyCompany?src=YourCompany/MyImage` .

* Nicht pyramidenbasierte TIFF- oder Vignettenanfragen erzeugen eine ähnliche Fehlermeldung wie

  *„Das `C:\Program Files\Scene7\ImageRendering\resources\MyVignette.vnt` hat kein gültiges DSF und die Fläche von 2,25 MPixel überschreitet den Maximalwert von 2 MPixel“* .

  Es empfiehlt sich, pyramidenförmige Tiffs und Vignetten zu verwenden. Wenn Sie nicht-pyramidenförmige TIFFs oder Vignetten verwenden müssen, befolgen Sie die nachstehenden Anweisungen, um die Größenbeschränkung zu erhöhen.

  *Umgehen*:

  Erhöhen Sie für das Rendern von nicht pyramidenförmigen Vignetten im Bild den Eigenschaftswert für IrMaxNonPyrVignetteSize in der [!DNL install_root/ImageServing/bin/ImageServerRegistry.xml] Konfigurationsdatei.

  Erhöhen Sie für nicht pyramidenförmige TIFFs zur Bildbereitstellung den Eigenschaftswert für `MaxNonDsfSize` in der [!DNL install_root/ImageServing/bin/ImageServerRegistry.xml] Konfigurationsdatei.

* Adobe [!DNL Photoshop] CS3 speichert mehrschichtige PSD-Dateien nicht standardmäßig als zusammengesetztes Bild.

  *Symptome*:

  Die PSD-Datei mit Adobe [!DNL Photoshop] CS3-Schicht wird schwarz angezeigt, wobei der Text lautet: „Diese [!DNL Photoshop] wurde nicht mit einem zusammengesetzten Bild gespeichert.“ für das Image-Serving-Antwortbild oder in IPS.

  *Behelfslösung*:

  Speichern Sie die Adobe [!DNL Photoshop] CS3-Datei unter aktivierter Option „Kompatibilität maximieren“.

* Wenn Sie einem CMYK/JPEG-Antwortbild ein ICC-Profil zuweisen, werden die Farben in einigen Browsern invertiert.*Umgehen*:

  Ändern des Antwortbildformats mithilfe von `fmt=`

* Die Größe der HTTP-Antwortbilddaten nach der Komprimierung, einschließlich Dateikopfzeile, ist auf 16 MB beschränkt.
* &quot;…“ ist in keinem Pfadelement in HTTP-Anfragen zulässig.
* Bei der Deinstallation können vom Benutzer erstellte oder geänderte Dateien aus *[!DNL install_root]* oder einem beliebigen Unterordner entfernt werden. Kopieren Sie diese Dateien vor der Deinstallation an einen anderen Speicherort.

## Einschränkungen, die nur für die Bereitstellung von Bildern gelten {#section-b08ad535e4454265b8157dec244c4faf}

* Vordergrundfarben im RTF-Befehl ( `\cf`) werden für FotoFont-Text nicht unterstützt.
* Die Synthese von fett, kursiv und fett/kursiv wird als Fehler für FotoFont-Text zurückgewiesen.
* Der vertikale Textfluss wird für FotoFont-Text nicht unterstützt.
* 16bpc PNG-Bilder werden für FotoFont-Text nicht unterstützt.
* Farbkorrekturen für PNG-Bilder mit eingebetteten Farbprofilen verwenden hartcodierte Optionen. Die Render-Absicht ist relativ farbmetrisch, und die Blackpoint-Kompensation für FotoFont-Text ist aktiviert.
* Die dateibasierte Suche wird nicht unterstützt, wenn die Gebietsschema-Übersetzung in der [!DNL ini]-Datei des Unternehmens aktiviert ist.
* Die Bildbereitstellung schreibt nicht geschlossene [!DNL Photoshop] nicht korrekt.
* Die Bildbereitstellung unterstützt derzeit nicht die Verarbeitung von TIFF-Dateien, die mit Adobe Media Encoder 4.0.1 oder früher exportiert wurden. Adobe Media Encoder ist in Premiere Pro CS4, After Effects CS4 und Creative Suite 4 Production Premium enthalten.
* Die Verwendung von `text=` mit Ebenen mit Selbstgrößenanpassung unterstützt keine RTF-Zeichenfolgen, die mehr als eine Einstellung für die Zeilenausrichtung verwenden.

  *Beispiel*

  Die RTF-Zeichenfolge kann nicht sowohl die linke als auch die rechte Zeilenausrichtung für eine Textebene mit automatischer Größenanpassung verwenden.

* SVG verfügt über eine eigene Eigenschaft für den Schriftarten-Suchpfad referenzierter Schriftarten, die nicht in die SVG-Datei eingebettet sind.

  *Symptome*

  Gerenderte SVG-Bilder, die Schriftdefinitionen enthalten, verwenden die falsche Schriftart.

  *Problemumgehung*

  Legen Sie die Eigenschaft `svgProvider.fontRoot=` in [!DNL install_root/ImageServing/conf/PlatformServer.conf] fest.

* Das Zuschneiden verwendet derzeit `bgColor=` anstelle von `color=`, um einen neu erweiterten Bereich zu füllen.

* Die Farbkonvertierung ist möglicherweise nicht korrekt, wenn `bgColor=` nicht mit dem Grundfarbraum übereinstimmt, an dem Farbprofile beteiligt sind.
* Effekte auf der äußeren Ebene werden nicht gerendert, wenn die Ebene keine Maske oder Alphadaten hat.

## Einschränkungen, die nur für das Rendern von Bildern gelten {#section-4c6949e797174607a3d1ab4d3d4a725a}

* Abziehbilder und Wandmaterialien sind nicht entfernbar.
* Die Größe der Texturen ist im Verhältnis zur Größe der Vignettenansicht begrenzt. In seltenen Fällen kann die standardmäßige Begrenzung von 425 % der Ansichtsgröße bei Anwendungen, die sehr große, nicht wiederholbare Texturen verwenden, zu Problemen führen. Wenn es nicht möglich ist, die Anwendung oder die Inhalte so zu ändern, dass sie innerhalb der vordefinierten Einschränkungen funktionieren, kann der Prozentsatz wie folgt erhöht werden. Öffnen Sie [!DNL install_root/ImageServing/conf/ImageServerRegistry.xml] mit einem Texteditor, suchen Sie `IrMaxTextureSizeFactor` und geben Sie einen neuen Prozentwert ein. Die Änderung wird sofort wirksam, ohne den Bildserver neu zu starten.

* Die JavaScript-Engines in Netscape und Opera speichern die Antwortdaten, selbst wenn die nocache-Kopfzeile festgelegt ist. Dies beeinträchtigt das ordnungsgemäße Funktionieren von statusbehafteten Anfragen.

  *Problemumgehung*

  Hängen Sie einen Zeitstempel oder eine andere eindeutige Kennung an die Anfragezeichenfolge an, z. B. `"&.ts=currentTime`.

## Einschränkungen, die nur für Dienstprogramme gelten {#section-906a6b2378154b3da122b2332983f7a5}

`ImageConvert`stürzt manchmal mit einem Segmentierungsfehler ab, wenn er mit einem `control-c` angehalten wird.
