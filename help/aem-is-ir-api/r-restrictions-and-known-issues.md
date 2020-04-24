---
description: Es gibt einige Einschränkungen und bekannte Probleme, die bei der Verwendung von Scene7 Image Serving berücksichtigt werden sollten.
seo-description: Es gibt einige Einschränkungen und bekannte Probleme, die bei der Verwendung von Scene7 Image Serving berücksichtigt werden sollten.
seo-title: Einschränkungen und bekannte Probleme
solution: Experience Manager
title: Einschränkungen und bekannte Probleme
topic: Scene7 Image Serving - Image Rendering API
uuid: 9f9fad41-4828-4fba-8f5f-2c33e7811c71
translation-type: tm+mt
source-git-commit: a47f2b4ef8ebef0c8218dafa4678443aa61241f5

---


# Einschränkungen und bekannte Probleme{#restrictions-and-known-issues}

Es gibt einige Einschränkungen und bekannte Probleme, die bei der Verwendung von Scene7 Image Serving berücksichtigt werden sollten.

## Dokumentationsfehler {#section-b1579410b11e41e488c7de9ecc7e8d5c}

* Die Anzahl der Zeilen überschreitet nicht das Maximum der `\copyfitmaxlines` Einstellung und die Anzahl der expliziten Zeilen in der Texteingabe.
* Für Bildsätze sind passende geschweifte Klammern und Klammern erforderlich. Wenn geschweifte Klammern und Klammern nicht übereinstimmen, müssen sie URL-kodiert sein.
* Der serverseitige Warnhinweis zur globalen Antwortzeit enthält Fehlerantworten.
* Der `id=` Befehl ist derzeit erforderlich, wenn der `rect=` Befehl mit einer Bild- oder Maskenanforderung verwendet wird.

## Bekannte Unterschiede textPs= vs text= {#section-16ede4c13a7648feb0d2fc93341fd4aa}

* Synthetisches Kursivbild wird weniger geneigt als bei Verwendung `text=`.
* Unterstreichen ist etwas niedriger und dünner als bei Verwendung `text=`.
* `\expnd` und bei `\expndtw` Verwendung mit hohen Negativwerten dazu führen, dass Zeichen bei der Verwendung untereinander platziert werden `text=`.

* `\charscaley` wird anders skaliert als bei Verwendung, `text=` wirkt sich jedoch nicht auf die Zeilenhöhe aus.

* Wenn die letzte Textzeile nicht passt, wird die gesamte Zeile abgelegt, anstatt als Cut-off angezeigt zu werden.
* `\slmult` und `\sl` verhalten sich anders als MS Word und `text=`, sie treten einfach für die aktuellen und nachfolgenden Absätze in Kraft.

* `\sb` gilt für den ersten Absatz für MS Word und `text=`nicht für Adobe InDesign und Fotoshop.

* `\sa` gilt für den letzten Absatz für MS Word und `text=`nicht für Adobe InDesign und Fotoshop.

## Abwärtskompatibilität {#section-a76842f751944f4fb664af296d064122}

* Das Escapen des Unterstrichzeichens ( `\_`) in einer RTF-Zeichenfolge funktioniert nicht bei allen Schriftarten, die `textPs=`

* Bei der Unterstützung wird nicht zwischen Groß- und Kleinschreibung unterschieden.
* Der Katalogcache wurde von 60 auf 10 Sekunden verringert.
* Die Funktion zur Fehlerumleitung leitet jetzt nur Anforderungen um, die auf beschädigte Profile, Schriftarten, Farbbilder und  verweisen, die in einem Katalog veröffentlicht, aber nicht auf der Festplatte gefunden werden.
* `posN=`, `anchor=`, `anchorN=`, `origin=`und `originN=` geben nun einen Parsing-Fehler zurück, wenn einer der Modifikatorwerte größer als 2147483648 ist.

* Die Kodierung verschachtelter Anforderungen wird nicht unterstützt. Transition des neuen Verhaltens und Dekodierung verschachtelter Anforderungswerte, die in URL-Anforderungen auf Ihrer Site und in Ihren Firmen-Katalogen enthalten sind.
* DefaultImage wendet jetzt bei der Verwendung von `req=tmb`Miniaturattributen an.
* In früheren Versionen `flip=`wurde das Bild unabhängig vom Ankerpunkt nie neu positioniert.

## Beschränkungen für Bibliotheken von Drittanbietern {#section-79768b96bf634e44ab672c5b893f343d}

Die Digimarc-Bibliothek weigert sich, ein Digimarc-Wasserzeichen auf ein Bild anzuwenden, wenn eines bereits erkannt wurde. Wenn ein Masterbild ausreichend bearbeitet wird, kann die Digimarc-Bibliothek möglicherweise trotzdem erkennen, dass das Wasserzeichen angewendet wurde. Sie kann diese Informationen jedoch möglicherweise nicht lesen. Dies führt zu einem neuen Bild, bei dem die ursprünglichen Digimarc-Informationen, die auf das Originalbild angewendet wurden, nicht abgerufen werden können. Image Serving kann jetzt das im Katalog &quot;Firma&quot;definierte Digimarc-Wasserzeichen anwenden.

## Einschränkungen für Image Serving und Image Rendering {#section-f836cb40ae2d4f32a9cf7ebda4d91bae}

* Image Serving und Image Rendering nutzen möglicherweise nicht alle CPUs, wenn mehr als 4 CPUs verfügbar sind. Simulieren Sie Ihren Traffic auf diesen Computern, um zu sehen, wie vorteilhaft er mit mehr als 4 CPUs ist.
* Remote-URLs, die eine Umleitung zurückgeben (HTTP-Status 301, 302 oder 303), werden abgelehnt.
* Beim Konfigurieren `errorRedirect.rootUrl` der in dieser Eigenschaft definierten IP-Adresse muss der Regelsatz- `<addressfilter>` Tag-Wert auf diesem Server enthalten sein.

   *Beispiel*:

   Server A wurde definiert `errorRedirect.rootUrl=10.10.10.10` .

   Server B mit der IP-Adresse 10.10.10.10 legt den `<addressfilter>` Tag-Wert in der Regelsatzdatei so fest, dass er die IP-Adresse (10.10.10.10) enthält.

* Punkttext und Textpfad mit Positionierung können eine Beschneidung aufweisen.
* `text=` gilt nur `\sa` und `\sb` für den gesamten Textblock und nicht pro Absatz.

* Wenn Sie eine in der URL definierte Firma und eine andere für den Modifikator `src=` oder `mask=` Modifikator definierte Firma verwenden, müssen Sie der für `src=` oder `mask=` diese Anforderungsform definierten Firma einen Schrägstrich voranstellen.

   *Beispiel*:

   `/is/image/MyCompany?src=/YourCompany/MyImage` .

   Statt: `/is/image/MyCompany?src=YourCompany/MyImage` .

* Nicht-Pyramided Tiff- oder Vignettenanforderungen erzeugen eine ähnliche Fehlermeldung wie

   *&quot;Bild`C:\Program Files\Scene7\ImageRendering\resources\MyVignette.vnt`hat keinen gültigen DSF und Bereich von 2,25MPixel überschreitet max von 2MPixel&quot;* .

   Best Practice ist die Verwendung von Pyramided Tiffs und Vignetten. Wenn Sie nicht-pyramidierte Zecken oder Vignetten verwenden müssen, befolgen Sie die unten stehenden Anweisungen, um die Größenbeschränkung zu erhöhen.

   *Problemumgehung*:

   Erhöhen Sie für das Image Rendering nicht-pyramidierter Vignetten den Eigenschaftswert für IrMaxNonPyrVignetteSize in der Konfigurationsdatei [!DNL *[!DNL install_root]*/ImageServing/bin/ ImageServerRegistry.xml].

   Erhöhen Sie für Image Serving non-pyramided TIFFs den Eigenschaftswert `MaxNonDsfSize` in der Konfigurationsdatei [!DNL *[!DNL install_root]* /ImageServing/bin/ ImageServerRegistry.xml].

* Adobe Fotoshop CS3 speichert keine PSD-Dateien mit Ebenen standardmäßig als Composite-Bild.

   *Symptome*:

   Die PSD-Datei mit Ebenen in Adobe Fotoshop CS3 wird als schwarz mit dem Text &quot;Diese Fotoshop-Datei mit Ebenen wurde nicht mit einem Composite-Bild gespeichert&quot; angezeigt. für das Image Serving-Antwortbild oder in IPS.

   *Behelfslösung*:

   Speichern Sie die Adobe Fotoshop CS3-Datei mit aktivierter Maximierung der Kompatibilität.

* Wenn einem CMYK-/JPEG-Antwortbild ICC-Profil zugewiesen wird, werden in einigen Browsern Farben invertiert.*Problemumgehung*:

   Ändern des Antwortbildformats mithilfe von `fmt=`

* Die Größe der HTTP-Antwort-Bilddaten nach der Komprimierung, einschließlich des Dateiheaders, ist auf 16 MB beschränkt.
* &quot; ..&quot; ist in keinem Pfadelement in HTTP-Anforderungen zulässig.
* Bei der Deinstallation können vom Benutzer erstellte oder geänderte Dateien aus *[!DNL install_root]* oder einem beliebigen Unterordner entfernt werden. Kopieren Sie diese Dateien vor der Deinstallation an einen anderen Speicherort.

## Nur für Image Serving geltende Einschränkungen {#section-b08ad535e4454265b8157dec244c4faf}

* Vordergrundfarben im RTF-Befehl ( `\cf`) werden für FotoFont-Text nicht unterstützt.
* Die Synchronisierung fett, kursiv und fett/kursiv wird als Fehler für FotoFont-Text zurückgewiesen.
* Vertikaler Textfluss wird für FotoFont-Text nicht unterstützt.
* PNG-Bilder mit 16 bpc werden für FotoFont-Text nicht unterstützt.
* Farbkorrekturen für PNG-Profile mit eingebetteten Farbbildern verwenden hartcodierte Optionen. Render Intent ist relativ farbmetrisch und die Blackpoint-Kompensation ist für FotoFont-Text aktiviert.
* Dateibasierte Suche wird nicht unterstützt, wenn die Sprachübersetzung in der Firma [!DNL ini] aktiviert ist.
* Image Serving schreibt nicht geschlossene Fotoshop-Pfade nicht richtig.
* Image Serving unterstützt derzeit nicht die Verarbeitung von TIFF-Dateien, die mit Adobe Media Encoder 4.0.1 oder früher exportiert wurden. Adobe Media Encoder ist in Premiere Pro CS4, After Effects CS4 und Creative Suite 4 Production Premium enthalten.
* Bei der Verwendung `text=` mit Ebenen mit Selbstgrößenänderung werden keine RTF-Zeichenfolgen unterstützt, die für die Zeilenausrichtung mehr als eine Einstellung verwenden.

   *Beispiel*

   Die RTF-Zeichenfolge kann für eine selbstformatierende Textebene nicht sowohl die linke als auch die rechte Ausrichtung verwenden.

* SVG verfügt über eine eigene Eigenschaft für den Nachschlagepfad von referenzierten Schriftarten, die nicht in die SVG-Datei eingebettet sind.

   *Symptome*

   Gerenderte SVG-Bilder, die Schriftdefinitionen enthalten, verwenden die falsche Schriftart.

   *Behelfslösung*

   Legen Sie die Eigenschaft `svgProvider.fontRoot=` in [!DNL *[!DNL install_root]* /ImageServing/conf/PlatformServer.conf] fest.

* Die Option &quot;Beschneiden&quot;wird derzeit verwendet, `bgColor=` `color=` anstatt einen neuen erweiterten Bereich zu füllen.

* Die Farbkonvertierung ist ggf. nicht korrekt, wenn `bgColor=` sie nicht mit dem Farbraum übereinstimmt, in dem Profil verwendet werden.
* Effekte auf äußeren Ebenen werden nicht gerendert, wenn die Ebene keine Maske- oder Alpha-Daten hat.

## Nur für das Rendering von Bildern geltende Einschränkungen {#section-4c6949e797174607a3d1ab4d3d4a725a}

* Dekore und Wandmaterialien sind nicht abnehmbar.
* Die Größe der Texturen ist relativ zur Größe der Vignettengröße begrenzt. In seltenen Fällen kann die Standardgrenze von 425 % der Ansicht eine Anwendung beeinträchtigen, die sehr große, nicht wiederholbare Texturen verwendet. Wenn es nicht möglich ist, die Anwendung oder den Inhalt so zu ändern, dass er innerhalb der vordefinierten Einschränkungen funktioniert, kann der Prozentsatz wie folgt erhöht werden. Öffnen Sie mithilfe eines Texteditors [!DNL *[!DNL install_root]*/ImageServing/conf/ImageServerRegistry.xml], suchen Sie einen neuen Prozentwert `IrMaxTextureSizeFactor` und geben Sie ihn ein. Die Änderung wird sofort wirksam, ohne den Image-Server neu zu starten.

* Die JavaScript-Engines in Netscape- und Opera-Cache-Antwortdaten, selbst wenn der nocache-Header eingestellt ist. Dies beeinträchtigt das ordnungsgemäße Funktionieren von statusbezogenen Anfragen.

   *Behelfslösung*

   Hängen Sie einen Zeitstempel oder einen anderen eindeutigen Bezeichner an die Anforderungszeichenfolge an, z. B. `"&.ts=currentTime`.

## Beschränkungen, die nur für Versorgungseinrichtungen gelten {#section-906a6b2378154b3da122b2332983f7a5}

`ImageConvert`Abstürze mit einem Segmentierungsfehler beim Beenden mit einem `control-c`.
