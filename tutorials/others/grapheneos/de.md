---
name: GrapheneOS
description: Graphene OS Anleitung
---

> "[GrapheneOS](https://grapheneos.org/) ist ein auf Privatsphäre und Sicherheit ausgerichtetes mobiles Betriebssystem mit Android-App-Kompatibilität, das als gemeinnütziges Open-Source-Projekt entwickelt wurde."

GrapheneOS, ursprünglich 2014 als 'CopperheadOS' gegründet, basiert auf dem traditionellen Android-Code (AOSP), wurde jedoch mit vielen Änderungen und Verbesserungen entwickelt, um die Privatsphäre und Sicherheit der Benutzer zu verbessern. GrapheneOS gibt dem Benutzer die Kontrolle über sein Telefon, nicht den großen Technologieunternehmen.

### Inhaltsverzeichnis:

- Einführung
- Vorbereitung
- Installation
- App-Alternativen
- Nachteile
- Nützliche Informationen

Anleitung von https://github.com/BitcoinQnA/Bitcoiner.Guide/blob/main/grapheneos.md

## Warum GrapheneOS verwenden?

Moderne Telefone sind $500-$1000 teure Geräte zur Verfolgung und Datenerfassung. Jeder Aspekt unseres Lebens läuft über sie, und leider werden viele dieser Daten in irgendeiner Form mit Dritten geteilt.
GrapheneOS wurde speziell entwickelt, um diese Datenweitergabe zu reduzieren und die Gerätesicherheit vor potenziellen Angriffsvektoren zu verbessern. Es gibt kein GrapheneOS-Konto. Sie benötigen keines, um Apps herunterzuladen oder mit dem Betriebssystem zu interagieren. Ganz einfach, Sie sind nicht das Produkt.

GrapheneOS bietet zusätzliche Sicherheit für Ihre Android-Erfahrung durch einige einfache Grundprinzipien.

1. **Reduzierung der Angriffsfläche** - Entfernen Sie unnötigen Code (oder Bloatware).
2. **Verhinderung von Schwachstellenexposition** - Ermöglichen Sie dem Benutzer genügend Granularität, um die Kompromisse auszuwählen, mit denen er sich wohl fühlt.
3. **Sandbox-Eindämmung** - GrapheneOS stärkt vorhandene Android-Sandboxes und schränkt die Kommunikationsfähigkeit jeder App mit dem Rest Ihres Telefons weiter ein.

Erfahren Sie mehr über die technischen Details des Funktionsumfangs von GrapheneOS [hier](https://grapheneos.org/features).

### Erleichterung des Übergangs

Wenn Sie seit Jahren im Google- oder Apple-Ökosystem verankert sind, kann der Gedanke, über Nacht auf all diese Bequemlichkeit zu verzichten, beängstigend sein. Aber mit einigen sorgfältig überlegten Entscheidungen zur App-Installation (später behandelt), kann ein Großteil dieser erwarteten Schwierigkeiten reduziert oder beseitigt werden.

So gut die Alternativen auch werden, der Gedanke an solch eine Veränderung kann immer noch abschreckend sein. Wenn Sie sich in dieser Situation befinden, ist mein bester Rat, Ihr neues GrapheneOS-Gerät eine Weile parallel zu Ihrem bestehenden Telefon zu verwenden. Von dort aus können Sie sich langsam von 2-3 Apps pro Woche entwöhnen, bis Sie nur noch zum GrapheneOS-Gerät greifen.

Wenn Sie diesen Ansatz wählen, seien Sie streng mit sich selbst und beenden Sie Ihre Abhängigkeit von den überwachten Alternativen so schnell wie möglich. Wir Menschen sind faul und wählen oft den Weg des geringsten Widerstands. Denken Sie daran, warum Sie den Wechsel überhaupt vorgenommen haben.

**Anstatt mit Ihren persönlichen Daten zu bezahlen, haben Sie sich dafür entschieden, mit Ihrer Zeit und manchmal mit Ihrem hart verdienten Geld zu bezahlen (je nach den installierten alternativen Apps).**

## Erste Schritte

GrapheneOS ist derzeit nur für _(ironischerweise)_ die [Google Pixel](https://grapheneos.org/faq#supported-devices)-Reihe von Telefonen verfügbar. Dies geschieht jedoch nicht ohne guten Grund. Pixel bieten die beste hardwarebasierte Sicherheit, um die Arbeit zur Stärkung des Betriebssystems zu ergänzen. Dazu gehören spezifische Komponentenisolationen und verifizierter Boot.

### Auswahl eines Geräts

Bei der Auswahl des Pixels, auf dem Sie GrapheneOS installieren möchten, stellen Sie sicher, dass Sie überprüfen, wie lange das Gerät standardmäßige [Sicherheitsupdates](https://support.google.com/pixelphone/answer/4457705?hl=de#zippy=%2Cpixel-xl-a-a-g-a-g) erhalten wird.
Zum Zeitpunkt des Schreibens ist das Pixel 6a das günstigste Modell mit guter langfristiger Unterstützung, garantiert bis Juli 2027. Wenn Sie sich für dieses Modell entscheiden, funktioniert das OEM-Entsperren nicht mit der Version des Standardbetriebssystems ab Werk. Sie müssen es auf die Version vom Juni 2022 oder später über ein Over-the-Air-Update aktualisieren. Nachdem Sie es aktualisiert haben, müssen Sie das Gerät auch auf die Werkseinstellungen zurücksetzen, um das OEM-Entsperren zu beheben. Alle anderen Modelle, die netzwerkfreigeschaltet sind, sind sofort für GrapheneOS einsatzbereit.

Bei der Auswahl eines Geräts sollten Sie auch sicherstellen, dass Sie eine netzwerkfreigeschaltete Version kaufen. Bestimmte Anbieter wie Verizon liefern ihre Geräte mit einem gesperrten Bootloader aus, was den folgenden Vorgang vollständig verhindert.

### Installation von GrapheneOS

Der GrapheneOS-Webinstaller (https://grapheneos.org/install/web) macht den gesamten Prozess zum Kinderspiel und kann von jedem in weniger als 10 Minuten abgeschlossen werden.
Die folgenden Anweisungen sind eine gekürzte Version des oben genannten Links.

Alles, was Sie benötigen, ist:

- Das Pixel
- Ein USB-Kabel, um das Telefon mit Ihrem Computer zu verbinden
- Einen Computer, auf dem ein Webbrowser ausgeführt wird (jeder Chromium-basierte Browser: Chrome, Edge, Brave, usw.)

1. Der erste Schritt besteht darin, zu **Einstellungen** > **Telefoninfo** zu gehen und mehrmals auf die Build-Nummer zu tippen, bis Sie sehen, dass **'Entwicklermodus'** aktiviert ist.
2. Gehen Sie als nächstes zu **Einstellungen** > **System** > **Entwickleroptionen** und aktivieren Sie **'OEM-Entsperrung'**.
3. Starten Sie das Gerät neu und halten Sie dabei die Lautstärke-Leiser-Taste gedrückt.
4. Verbinden Sie das Telefon mit Ihrem Laptop und wenn Sie zur Autorisierung aufgefordert werden, erlauben Sie die Verbindung.
5. Klicken Sie auf der Webinstaller-Seite auf 'Bootloader entsperren'.
6. Sie sehen dann eine Änderung der Telefonoptionen. Verwenden Sie die Lautstärketaste, um die Auswahl auf `entsperren` zu ändern, und verwenden Sie die Ein-/Aus-Taste, um zu bestätigen.
7. Klicken Sie als nächstes auf der Webinstaller-Seite auf 'Release herunterladen'.
8. Sobald der Download abgeschlossen ist, fahren Sie mit dem nächsten Schritt fort und klicken Sie auf 'Release flashen'. Dies dauert ein bis zwei Minuten und Sie müssen das Telefon überhaupt nicht berühren.
9. Gehen Sie abschließend zum nächsten Schritt des Webinstallers und klicken Sie auf **Bootloader sperren**. Sie müssen die Auswahl ändern und mit der Ein-/Aus-Taste bestätigen, wie Sie es zuvor im Prozess getan haben.
10. Wenn Sie das Wort `Start` sehen, bestätigen Sie dies mit der Ein-/Aus-Taste und das Gerät startet in Ihr neues Google-freies Betriebssystem.

![image](assets/2.webp)

GrapheneOS-Startbildschirm

_Nach dem ersten Start und der Einrichtung ist es ratsam, das OEM-Entsperren in den Einstellungen > System > Entwickleroptionen zu deaktivieren._

_Sie möchten möglicherweise auch den zusätzlichen, optionalen, aber empfohlenen Schritt unternehmen, die Installation über die Auditor-App zu überprüfen. Sie benötigen ein separates Android-Telefon mit der installierten App, um diesen Schritt abzuschließen. Anweisungen dazu finden Sie [hier](https://attestation.app/tutorial)._


![video](https://www.youtube.com/embed/L1KZWjZVnAw)

Video, das die oben beschriebenen einfachen Schritte erläutert

Wenn Ihnen diese einfachen Schritte zu kompliziert erscheinen, können Sie erwägen, ein Pixel mit vorinstallierter GrapheneOS-Software zu kaufen (https://ronindojo.io/en/roninmobile). Seien Sie sich jedoch bewusst, dass Sie einem Anbieter ein gewisses Maß an Vertrauen entgegenbringen.

### Vorinstallierte Apps

Jetzt, da Sie eingerichtet sind, werden Sie möglicherweise feststellen, wie minimalistisch GrapheneOS nach der ersten Installation aussieht. Standardmäßig sind folgende Apps installiert:

![image](assets/3.webp)

Standard-Apps
Die einzigen beiden Begriffe, die Ihnen möglicherweise nicht vertraut sind, sind "Auditor" und "Vanadium".
- Die [Auditor-App](https://play.google.com/store/apps/details?id=app.attestation.auditor) verwendet hardwarebasierte Sicherheitsfunktionen, um die Identität eines Geräts sowie die Authentizität und Integrität des Betriebssystems zu validieren. Sie überprüft, ob das Gerät das Standard-Betriebssystem mit gesperrtem Bootloader ausführt und ob keine Manipulationen am Betriebssystem vorgenommen wurden.
- [Vanadium](https://github.com/GrapheneOS/Vanadium) ist eine Variante des Chromium-Webbrowsers, die auf Datenschutz und Sicherheit optimiert ist.

## Anpassung

Telefon-Einstellungen sind eine persönliche Angelegenheit, aber hier sind einige der ersten Dinge, die ich ändere, wenn ich GrapheneOS installiere, um mich mehr wie zu Hause zu fühlen.

### Festlegen eines Hintergrundbilds und Aktualisieren des Designs

Gehen Sie zu Einstellungen > Hintergrundbild und Design. Von hier aus:

- Aktualisieren Sie die Hintergrundbilder für den Startbildschirm und den Sperrbildschirm mit Bildern, die aus dem Internet heruntergeladen wurden.
- Wählen Sie die Akzentfarben aus, die in der gesamten Benutzeroberfläche verwendet werden.
- Aktivieren Sie den Dunkelmodus.

### Batterieprozentsatz anzeigen

Gehen Sie zu **Einstellungen** > **Batterie** und aktivieren Sie dann **Batterieprozentsatz in der Statusleiste anzeigen**.

### Kontakte importieren

**Von einem anderen Android-Telefon** - Gehen Sie zur Kontakte-App und suchen Sie nach der Option "Exportieren als VCF".

**Von iOS** - Verwenden Sie eine App wie "Export Contact" und wählen Sie die Exportoption "vCard", um eine VCF-Datei zu exportieren.
Sobald Sie die VCF-Datei haben, können Sie sie mit einer externen Speicheroption wie einer microSD-Karte oder einem USB-Laufwerk auf Ihr GrapheneOS-Gerät übertragen. Wenn Sie keine dieser Optionen zur Hand haben, können Sie sich für den Austausch über eine der vielen unten aufgeführten Apps entscheiden.

![image](assets/4.webp)

Personalisierter Startbildschirm


## Alternative Apps

Um Ihr Telefon nützlich zu machen, möchten Sie einige Anwendungen installieren! Die folgenden Optionen sind entweder enthalten, weil ich sie persönlich alle verwendet habe oder weil sie starke Empfehlungen von der breiteren Datenschutzgemeinschaft erhalten. Es gibt viele andere großartige Alternativen, die hier nicht erwähnt werden, und [Awesome Privacy](https://awesome-privacy.xyz) bietet eine unglaublich umfangreiche Liste von datenschutzfreundlichen Anwendungen für alle Arten von Geräten.

Nur weil eine App Free and Open Source Software (FOSS) ist, bedeutet das nicht, dass sie frei von möglichen Datenschutzlecks ist. Verwenden Sie [Exodus](https://reports.exodus-privacy.eu.org/en/), um zu sehen, wie Ihre bevorzugten Apps in Bezug auf ihre Datenschutzprüfungen abschneiden.

### F-Droid

[F-Droid](https://f-droid.org/) ist ein installierbarer Katalog von FOSS-Anwendungen für Android. Der Client erleichtert das Durchsuchen, Installieren und Aktualisieren von Anwendungen auf Ihrem Gerät. Es ist erwähnenswert, dass Updates über F-Droid manchmal langsamer sein können als bei anderen App-Stores. Dies hängt hauptsächlich davon ab, ob die App im Haupt-F-Droid-Repository oder in einem benutzerdefinierten Repository gefunden wird.

Um F-Droid zu installieren, gehen Sie einfach über den Browser auf Ihrem GrapheneOS-Telefon zur Website und tippen Sie auf "Herunterladen". Dadurch wird eine `.apk`-Datei heruntergeladen. Sie werden dann gefragt, ob Sie die App installieren möchten.

Neben den Anwendungen, die im Standard-Repository von F-Droid zu finden sind, hosten viele Open-Source-Projekte auch ihr eigenes Repository, das in den Einstellungen der F-Droid-App hinzugefügt werden kann. Wenn dies der Fall ist, führt Sie das betreffende Projekt auf ihrer Website durch die sehr einfachen Schritte, die erforderlich sind, um dies zu erreichen.

![image](assets/5.webp)

F-Droid Startbildschirm

### Aurora Store
[Aurora Store](https://auroraoss.com/) ist eine FOSS-Version des Google Play Store. Aurora sieht dem traditionellen Play Store sehr ähnlich und ermöglicht es Ihnen, jede App herunterzuladen und zu aktualisieren, die Sie normalerweise über die Google-Option finden würden.
Das Killer-Feature von Aurora ist die anonyme Anmeldung. Das bedeutet, dass Sie alle Ihre Lieblings-Apps herunterladen können, die nicht über F-Droid oder direkt über APK verfügbar sind, ohne bei Ihrem Google-Konto angemeldet zu sein.

Bevor Sie dies als Standardinstallationsoption festlegen, denken Sie daran, dass viele der Anwendungen, von denen wir uns abwenden wollen, aus dem Play Store installiert wurden. Nur weil sie über Aurora zugänglich sind, ändert das nichts daran, dass einige möglicherweise Tracking-Funktionen enthalten. Es ist nicht immer möglich, aber wann immer Sie können, suchen Sie nach einer F-Droid-Alternative, bevor Sie über Aurora herunterladen.

Um Aurora zu installieren, suchen Sie einfach nach 'Aurora Store' in F-Droid.

Aurora hat auch einige potenzielle Angriffsvektoren, da die "anonymen Konten" tatsächlich von Aurora erstellt und kontrolliert werden. Sie könnten theoretisch bösartige Updates bereitstellen oder Apps auf Ihr Telefon pushen, obwohl Sie immer noch die Installationsaufforderung auf dem Gerät akzeptieren müssten. Aurora hat manchmal auch Probleme damit, dass Apps aufgrund von Regionen- und Gerätefehlern nicht angezeigt werden. Dies kann in der Regel mit den unten stehenden Schritten behoben werden.

**Top-Tipp** - Manchmal tritt im Aurora Store eine Rate-Limitierung auf, die Ihre Fähigkeit zur Suche und Installation von Apps einschränkt. Um dies zu umgehen, gehen Sie zu **Einstellungen** > **Apps** > **Aurora** > **Standardmäßig öffnen** und fügen Sie die Domain `play.google.com` hinzu. Jetzt wird immer, wenn Sie zu einer Website eines Produkts oder Dienstes navigieren, das den Link 'Über den Play Store herunterladen' enthält, das Antippen dieses Links die App in Aurora öffnen, damit Sie sie herunterladen können.


![image](assets/6.webp)

Startbildschirm des Aurora Store

### APK-Download

Apps auf Android können auch über eine `.apk`-Datei heruntergeladen und installiert werden. Dies ist eine großartige Alternative, die keine Drittanbieter-App-Stores erfordert. Laden Sie einfach die Datei direkt von der Website oder dem GitHub-Repository des Projekts oder Dienstes herunter.

Der Nachteil dieses Ansatzes ist, dass Sie keine automatischen Updates erhalten. Sie müssen also die Kommunikationskanäle des Dienstes überwachen, um über neue Versionen informiert zu werden. Es gibt jedoch ein großartiges Projekt namens Obtainium, das dieses Problem lösen soll. [Obtainium](https://github.com/ImranR98/Obtainium) ermöglicht es Ihnen, Open-Source-Apps direkt von deren Release-Seiten zu installieren und zu aktualisieren und Benachrichtigungen zu erhalten, wenn neue Versionen verfügbar sind.

![image](assets/7.webp)

Vorschau von Obtainium

### Web-Apps

Für Zeiten, in denen Sie einen Dienst nur selten nutzen möchten und keine native Anwendung herunterladen möchten, können Sie einfach auf die Webversion zugreifen. Viele Websites bieten heutzutage auch Progressive Web App (PWA)-Unterstützung an. Dabei können Sie eine bestimmte Website (z. B. Twitter.com) auf dem Startbildschirm Ihres Telefons als Lesezeichen speichern. Wenn Sie dann auf das Symbol tippen, öffnet es sich als Vollbildanwendung ohne die üblichen Ablenkungen, die mit der typischen Browser-Erfahrung einhergehen. Ein Beispiel dafür, wie dies aussieht, finden Sie unten.

Um dies in Vanadium, dem nativen Browser von GrapheneOS, zu erreichen, navigieren Sie einfach zur gewünschten Website, tippen Sie auf die drei vertikalen Punkte in der oberen rechten Ecke des Bildschirms und tippen Sie dann auf **'Zum Startbildschirm hinzufügen'**.

Der einzige Nachteil dieses Ansatzes ist, dass es sich hierbei nur um eine als Lesezeichen gespeicherte Webseite handelt und Sie keine Benachrichtigungen erhalten. Einige mögen das jedoch als positiv betrachten!

![image](assets/8.webp)

Twitter PWA

### Webbrowser
Mit der vorgefertigten Option Vanadium kann man eigentlich nichts falsch machen. Die App verhält sich genauso wie jeder andere mobile Browser, den ich ausprobiert habe, und ich hatte noch nie Kompatibilitätsprobleme.
Wenn Sie auf Tor native `.onion`-Websites zugreifen müssen, können Sie den Tor Browser APK direkt von ihrer [Website](https://www.torproject.org/download/#android) oder über F-Droid herunterladen.

### VPNs

Um Ihre Online-Aktivitäten vor neugierigen Internetdienstanbietern (ISPs) zu schützen, ist eine Virtual Private Network (VPN)-App eine gute Option. Ein VPN leitet Ihren Internetverkehr in einen verschlüsselten Tunnel zu einer gemeinsam genutzten IP-Adresse, die vom VPN-Dienstanbieter kontrolliert wird, um sicherzustellen, dass Ihre Geräteaktivität nicht mit Ihnen in Verbindung gebracht werden kann.

Die folgenden 3 angesehenen Optionen ermöglichen es Ihnen, den Service mit Bitcoin zu bezahlen und keine persönlichen Informationen anzugeben. Alle 3 Optionen sind über F-Droid verfügbar.

- [Mullvad](https://f-droid.org/packages/net.mullvad.mullvadvpn/)
- [Proton](https://f-droid.org/en/packages/ch.protonvpn.android/)
- [iVPN](https://f-droid.org/en/packages/net.ivpn.client/)

### Messaging

In den letzten Jahren sind verschlüsselte Messaging-Lösungen zahlreich geworden. Das Problem bleibt jedoch bestehen: Sie können die beste und privateste Option auf Ihrem Telefon installiert haben, aber wenn Sie keine Kontakte haben, die sie verwenden, wozu dient das dann?

Die meisten Menschen, die kein Interesse am Datenschutz haben, verwenden wahrscheinlich WhatsApp oder iMessage. Ersteres kann über den Aurora Store heruntergeladen werden, aber letzteres funktioniert nicht auf GrapheneOS (offensichtlich!).

- [Signal](https://signal.org/) ist einer der beliebteren Messenger mit Ende-zu-Ende-Verschlüsselung (E2EE) und verfügt über eine beeindruckende Erfolgsbilanz und einen umfangreichen Funktionsumfang. Signal erfordert eine Telefonnummer zur Anmeldung, daher sollten Sie sich, wenn Sie mit Personen chatten möchten, die Ihre Telefonnummer nicht kennen sollten, vielleicht einige der Alternativen ansehen. Signal muss über den Aurora Store heruntergeladen werden.
- [Simplex](https://f-droid.org/en/packages/chat.simplex.app/) ist ein recht neuer E2EE-Messenger. Er hat keine Benutzer-ID, erfordert keine Telefonnummer oder persönliche Informationen. Andere finden Sie, indem sie Ihren persönlichen QR-Code scannen oder Ihren eindeutigen Link besuchen. Simplex ermöglicht es fortgeschrittenen Benutzern auch, ihren eigenen Server zu betreiben, um die Abhängigkeit von zentralisierten Einrichtungen weiter zu reduzieren. Simplex hat keinen Desktop-Client und ist daher möglicherweise nicht geeignet, wenn Mehrgeräteunterstützung ganz oben auf Ihrer Prioritätenliste steht. Simplex für Android ist über F-Droid verfügbar.
- [Threema](https://threema.ch/en/faq/libre_installation) bietet ein ähnliches Erlebnis wie Simplex, ist aber schon länger auf dem Markt und wirkt daher etwas ausgereifter. Threema ist nicht kostenlos, eine lebenslange Lizenz kostet 4,99 US-Dollar und kann mit Bitcoin gekauft werden. Threema bietet einen Web-Client und native Desktop-Anwendungen. Die Android-Anwendung ist über F-Droid verfügbar.
- [Telegram FOSS](https://f-droid.org/en/packages/org.telegram.messenger/) ist eine inoffizielle FOSS-Fork der offiziellen Telegram-App für Android. Telegram hat E2EE-"Geheime Chats", aber die Standardeinstellung ist nicht privat. Telegram FOSS kann von F-Droid heruntergeladen werden.

![image](assets/9.webp)
Links: Threema
Rechts: Simplex

### Medien

- [Spotube](https://f-droid.org/packages/oss.krtirtho.spotube/) ist ein plattformübergreifender Spotify-Client, der kein Premium-Konto erfordert. Spotube ist über F-Droid verfügbar.
- [Nextcloud] (https://f-droid.org/en/packages/com.nextcloud.client/) ist eine selbst gehostete Produktivitätsplattform, mit der Sie Ihre Dateien, Kalender, Kontakte und vieles mehr speichern, synchronisieren und gemeinsam nutzen können. Nextcloud ist über F-Droid verfügbar.
- [Joplin](https://f-droid.org/en/packages/net.cozic.joplin/) ist eine App für Notizen und Aufgaben, die eine große Anzahl von Notizen in Notizbüchern verwalten kann. Joplin ist über F-Droid verfügbar.
- Mit [LibreOffice Viewer](https://f-droid.org/en/packages/org.documentfoundation.libreoffice/) können Sie alle Arten von Dokumenten, einschließlich Word-, Excel- und PowerPoint-Dateien, anzeigen und bearbeiten. LibreOffice Viewer ist über F-Droid verfügbar.

![Bild](assets/17.webp)

Links: Nextcloud
Rechts: Joplin

### Messaging

- [Signal](https://signal.org/) ist eine private Messaging-App, die eine Ende-zu-Ende-Verschlüsselung verwendet, um Ihre Unterhaltungen sicher zu halten. Signal kann als direkte APK oder über Aurora heruntergeladen werden.
- [Element](https://f-droid.org/en/packages/im.vector.app/) (früher bekannt als Riot) ist eine dezentrale Messaging-App, mit der Sie sicher mit anderen chatten, telefonieren und zusammenarbeiten können. Element ist über F-Droid verfügbar.
- [Telegram](https://telegram.org/) ist eine Cloud-basierte Messaging-App, die sich auf Geschwindigkeit und Sicherheit konzentriert. Telegram kann als direkte APK oder über Aurora heruntergeladen werden.

![image](assets/19.webp)

Left: Signal
Right: Element
- [KDE Connect](https://f-droid.org/packages/org.kde.kdeconnect_tp/) verbindet alle Ihre Geräte miteinander, um miteinander zu kommunizieren, wenn sie mit Ihrem Heimnetzwerk verbunden sind. Senden Sie ganz einfach Dateien, Fotos und Zwischenablagendaten über alle Ihre Geräte (sogar auf iOS!). KDE Connect kann von F-Droid heruntergeladen werden.
- [Notesnook](https://f-droid.org/en/packages/com.streetwriters.notesnook/) ist eine E2EE-Notizanwendung zum Synchronisieren Ihrer Gedanken und To-Do-Listen auf allen Ihren Geräten. Ihr kostenloser Plan sollte die meisten persönlichen Anwendungsfälle abdecken. Notesnook ist auf F-Droid verfügbar.
- [Standard Notes](https://f-droid.org/en/packages/com.standardnotes/) ist sehr ähnlich wie Notesnook, erfordert jedoch einen kostenpflichtigen Plan, um den Funktionsumfang zu erreichen. Standard Notes ist über F-Droid verfügbar.
- [Anysoft Keyboard](https://f-droid.org/packages/com.menny.android.anysoftkeyboard/) ist eine Tastatur-App, mit der Sie praktisch alles anpassen können, was Sie sich beim Tippen auf Ihrem Telefon vorstellen können. Sie kann über F-Droid heruntergeladen werden.
- [GBoard](https://play.google.com/store/apps/details?id=com.google.android.inputmethod.latin&hl=en&gl=US) ist die Standard-Tastatur-App von Google. Meiner Erfahrung nach bietet sie das beste Schreib- und Wischerlebnis. Wenn Sie diese App herunterladen, stellen Sie sicher, dass Sie alle netzwerkbezogenen Berechtigungen vollständig deaktivieren. Sie kann über Aurora heruntergeladen werden.

![image](assets/17.webp)

Links: Notesnook
Rechts: KDE Connect

### Lifestyle

- [Geometric Weather](https://f-droid.org/en/packages/wangdaye.com.geometricweather/) ist eine wunderschön gestaltete Open-Source-Wetter-App, die über F-Droid verfügbar ist. Sie unterstützt auch verschiedene Größen von Widgets, sodass Sie das Wetter in Ihrem gewählten Standort direkt von Ihrem Startbildschirm aus sehen können.
- [Translate You](https://f-droid.org/packages/com.bnyro.translate/) ist eine Open-Source- und datenschutzorientierte Übersetzungs-App, die mehr als 200 Sprachen unterstützt. Translate You ist über F-Droid verfügbar.
- [Proton Calendar](https://proton.me/calendar/download) ist ein einfach zu bedienender E2EE-Kalender, der nahtlos mit Ihren Proton-E-Mail-Konten interagiert. Proton Calendar kann als APK oder über den Aurora Store heruntergeladen werden.
- [PassAndroid](https://f-droid.org/en/packages/org.ligi.passandroid/) ist eine App zum Anzeigen und Speichern von Bordkarten, Gutscheinen, Kinokarten und Mitgliedskarten usw. Laden Sie einfach die entsprechende `pkpass`- oder `espass`-Datei herunter und öffnen Sie sie mit der App. PassAndroid ist über F-Droid verfügbar.

![image](assets/19.webp)
Links: Geometric Weather
Rechts: Proton Calendar

### Sicherheit/Datenschutz

- [Bitwarden](https://mobileapp.bitwarden.com/fdroid/) bietet eine kostenlose und E2EE-Plattformübergreifende Passwort-Manager-Lösung für alle Ihre Geräte. Ihr kostenpflichtiger Service ermöglicht es Ihnen, 2FA-Codes in die App zu integrieren. Der Serverteil von Bitwarden kann selbst gehostet werden und die Android-App ist über F-Droid verfügbar.
- [Proton Pass](https://proton.me/pass/download) bietet einen ähnlichen kostenlosen Service wie Bitwarden, aber [Proton Unlimited](https://proton.me/pricing)-Kunden haben Zugriff auf zusätzliche erweiterte Funktionen. Proton Pass ist als APK oder über Aurora verfügbar.
- [FreeOTP](https://f-droid.org/packages/org.fedorahosted.freeotp/) ist eine Zwei-Faktor-Authentifizierungsanwendung für Systeme, die Einmalpasswortprotokolle verwenden. Tokens können einfach durch Scannen eines QR-Codes hinzugefügt werden. FreeOTP ist über F-Droid verfügbar.
- [Aegis](https://f-droid.org/de/packages/com.beemdevelopment.aegis/) ist eine kostenlose, sichere und Open Source-App für Android, mit der Sie Ihre 2-Faktor-Authentifizierungstoken für Ihre Online-Dienste verwalten können. Aegis ist über F-Droid verfügbar.
- [Cryptomator](https://f-droid.org/de/packages/org.cryptomator.lite/) ist ein kostenpflichtiger plattformübergreifender Dienst, der Ihre Daten lokal verschlüsselt, damit Sie sie sicher in Ihren bevorzugten Cloud-Dienst hochladen können. Cryptomator kann über F-Droid heruntergeladen werden.

![Bild](assets/21.webp)
Links: Proton Pass
Rechts: Bitwarden

### Cloud-Lösungen

- [Proton Drive](https://proton.me/drive/download) ist eine kostenpflichtige E2EE-Cloud-Lösung zum Sichern und Speichern aller Ihrer Dateien. Zum Zeitpunkt der Erstellung dieses Textes haben sie gerade einen Windows-Desktop-Client angekündigt, aber Mac- und Linux-Benutzer müssen vorerst weiterhin die Webversion verwenden, um von ihren Computern aus zu synchronisieren. Der Android-Client ist als APK oder über Aurora verfügbar.
- [Skiff](https://skiff.com/download) bietet ebenfalls kostenpflichtigen E2EE-Cloud-Speicher und Datei-Kollaborationstools an. Sie bieten einen Mac- und Windows-Desktop-Client (sowie eine Web-App) an, und ihre Android-Clients müssen von Aurora heruntergeladen werden.
- [Nextcloud](https://f-droid.org/de/packages/com.nextcloud.client/) bietet eine voll ausgestattete Cloud-basierte Lösung für Zusammenarbeit, Geräteübergreifende Synchronisierung und Dateispeicherung. Fortgeschrittene Benutzer können wählen, ihre kostenlose und Open Source-Software auf beliebiger Hardware selbst zu hosten. Die Android-Clients können über F-Droid heruntergeladen werden.
- [Cryptpad](https://cryptpad.fr/) bietet eine kostenlose, webbasierte, E2EE-Alternative zu Google Docs.

![Bild](assets/23.webp)

Proton Drive

## Die Nachteile

Die Open Source- und datenschutzfreundlichen Alternativen zu den Anwendungen der Technologiekonzerne, an die Sie sich gewöhnt haben, sind zahlreich, und einige von ihnen sind oft besser als die geschlossenen, mit Spyware belasteten Alternativen.

Wenn Sie jedoch zu GrapheneOS wechseln, müssen Sie auf einige Annehmlichkeiten verzichten, für die es keine Alternativen gibt. Dazu gehören:

- **Apple CarPlay/Android Auto** - Sie müssen sich auf gute alte Bluetooth-, USB- oder Aux-Verbindungen beschränken.
- **Apple/Google Pay** - Die meisten Menschen tragen sowieso ihr Portemonnaie bei sich!
- **Banking-Apps** - Es ist nicht so, dass diese überhaupt nicht funktionieren. Einige funktionieren tatsächlich einwandfrei. Andere funktionieren nur mit aktivierten Google Play-Diensten (lesen Sie mehr dazu unten), und wieder andere funktionieren überhaupt nicht. Lesen Sie den Bericht Ihrer Bank [hier](https://privsec.dev/posts/android/banking-applications-compatibility-with-grapheneos/), um den aktuellen Stand der Dinge zu erfahren. Keine Sorge, wenn Ihre Bank auf der Liste der nicht funktionierenden Apps steht, Sie können einfach die URL als Web-App auf Ihrem Startbildschirm speichern.
- **Push-Benachrichtigungen** - Die meisten Anwendungen, die Ihnen Updates senden, wenn Sie keine bestimmte App verwenden, tun dies über Google Play-Dienste. Diese sind standardmäßig nicht mit GrapheneOS installiert, daher kann es sein, dass Sie nicht sofort benachrichtigt werden, wenn Ihnen ein Freund eine E-Mail sendet. Die gute Nachricht ist, dass einige der oben genannten Apps ihre eigene Hintergrundverbindung implementiert haben, um regelmäßig nach Updates zu suchen und Ihnen bei Bedarf eine Benachrichtigung zu geben.

### Sandboxed Google Play
GrapheneOS bietet eine Kompatibilitätsschicht, die die Möglichkeit bietet, die offiziellen Versionen von Google Play in der Standard-App-Sandbox zu installieren und zu verwenden. Google Play erhält auf GrapheneOS keinerlei speziellen Zugriff oder Privilegien im Gegensatz zur Umgehung der App-Sandbox und dem Erhalt eines massiven Zugriffs mit hohen Privilegien.

Wenn Sie feststellen, dass Sie einfach nicht ohne Push-Benachrichtigungen für Ihre Lieblings-App leben können oder eine bestimmte "Must-Have"-App ohne Play-Dienste nutzlos ist, ermöglicht es Ihnen GrapheneOS, diese Dienste in einer vollständig abgeschotteten Umgebung zu installieren. Nach der Installation benötigen diese Dienste kein Google-Konto, um zu funktionieren, und die Berechtigungen jedes Dienstes können streng kontrolliert werden.

Bevor Sie sich beeilen, diese am ersten Tag zu installieren, rate ich Ihnen, zu sehen, wie weit Sie ohne sie kommen. Sie werden wahrscheinlich überrascht sein, wie viele Apps normal funktionieren, auch ohne sie.

Wenn Sie sie dennoch installieren möchten, tippen Sie einfach auf die vorinstallierte "Apps"-Anwendung, gefolgt von "Google Play-Dienste". Erwägen Sie, sie zusammen mit den weniger privaten Apps, auf die Sie nicht verzichten können, in einem vollständig separaten Benutzerprofil zu installieren, um eine zusätzliche Ebene der Trennung vom Rest Ihres Telefons zu bieten.

![image](assets/24.webp)

Installationsbildschirm für Play-Dienste

### Profile

GrapheneOS ermöglicht es Ihnen, eine separate Telefonerfahrung innerhalb Ihres Telefons zu haben. Zusätzliche Profile können ihre eigenen Apps und Dienste installieren und haben keinen Zugriff auf Dateien oder Daten des Eigentümerkontos.
Wenn Sie nur ein oder zwei dieser "Must-Have"-Apps haben, die Play-Dienste erfordern, aber nur sehr selten verwendet werden, kann es eine gute Idee sein, sie zusammen mit Play-Diensten in einem separaten Profil zu installieren, um eventuelle Datenschutzimplikationen weiter zu verstärken, die im Eigentümerprofil verbleiben.

Sie können mehr über diesen Anwendungsfall [hier](https://discuss.grapheneos.org/d/168-ideas-for-user-profiles/2) lesen.

Wenn Sie sich entscheiden, ein separates Profil entsprechend Ihrem Anwendungsfall hinzuzufügen, könnte die App [Insular](https://f-droid.org/en/packages/com.oasisfeng.island.fdroid/) nützlich für Sie sein. Insular ermöglicht es Ihnen, ganz einfach eine Ihrer vorhandenen Apps in das neue Profil zu klonen, ohne den herkömmlichen Installationsweg zu gehen, der zuvor in diesem Leitfaden behandelt wurde. Insular ermöglicht es Ihnen auch, schnell eine beliebige dieser Apps zu "einfrieren", um alle Hintergrunddienste dieser App vollständig zu deaktivieren.

![image](assets/24.webp)

Bildschirm zur Verwaltung von Benutzerprofilen

### e-SIMs

Wenn Sie Ihre Telefonprivatsphäre auf die nächste Stufe heben möchten und einen Mobilfunkdienst haben möchten, der von Ihrer realen Identität getrennt ist, könnte eine eSIM das Richtige für Sie sein. Eine eSIM ist eine virtuelle SIM-Karte, die Sie online kaufen und über einen QR-Code zu Ihrem Telefon hinzufügen können. Unternehmen, die solche Dienste anbieten und anonym mit Bitcoin bezahlt werden können, sind [Silent.Link](https://silent.link/) und [Bitrefill](https://www.bitrefill.com/gb/en/esims/).

eSIMs sollten nicht als Allheilmittel für die Telefonprivatsphäre betrachtet werden. Sie können ein nützliches Werkzeug sein, wenn sie in den richtigen Händen sind, aber bitte informieren Sie sich über die [Kompromisse](https://grapheneos.org/faq#cellular-tracking) bei der Verwendung eines beliebigen Mobilfunkdienstes, wenn Ihre Absicht darin besteht, komplett "off grid" zu gehen.

Für die Bereitstellung von eSIMs in GrapheneOS müssen die sandboxierten Play-Dienste installiert sein.

## Backups

Nachdem Sie Ihr neues Pixel-Telefon ohne Google eingerichtet haben, ist es eine gute Idee, eine Sicherungskopie zu erstellen. Diese Sicherungskopie ermöglicht es Ihnen, das Telefon im Falle eines Verlusts oder Diebstahls auf einen identischen Zustand wiederherzustellen.
Sie können wählen, die Sicherungsdatei auf einem externen Speichermedium oder in einer selbst gehosteten Cloud-Lösung wie Nextcloud zu speichern, obwohl einige Benutzer unterschiedliche Erfolgsniveaus mit der letzteren Option berichten.
Um Ihre erste Sicherung zu erstellen:

1. Gehen Sie zu **Einstellungen** > **System** > **Sicherung** und notieren Sie Ihren 12-Wort-Wiederherstellungscode. Dieser Code wird benötigt, um die Sicherungsdatei zu einem späteren Zeitpunkt zu entschlüsseln. Verlieren Sie den Code, verlieren Sie den Zugriff auf Ihre Telefon-Sicherung.
2. Wählen Sie als nächstes Ihren Speicherort aus. Ich würde eine externe USB-Festplatte oder eine industrielle microSD-Karte empfehlen.
3. Wählen Sie die zu sichernden Daten aus. Wenn Sie genügend Platz auf Ihrem angegebenen Speichermedium haben, empfehle ich, alles auszuwählen.
4. Tippen Sie auf die drei Punkte oben rechts und wählen Sie **Jetzt sichern**.

![Bild](assets/26.webp)

Sicherungsbildschirm

Denken Sie daran, dass es sinnvoll ist, diesen Schritt regelmäßig abzuschließen, wenn Sie Offline-Sicherungen auf externen Speichermedien erstellen, um sicherzustellen, dass keine kürzlich wichtigen Aktualisierungen auf Ihrem Telefon verloren gehen, falls das Schlimmste passieren sollte.

![Video](https://www.youtube.com/embed/eyWmcItzisk)

Video zur Sicherungsprozess

## Fazit

In den letzten Jahren hat sich die GrapheneOS-Software erheblich weiterentwickelt. Sie ist stabiler und kompatibler als je zuvor. In Kombination mit dem blühenden Open-Source- und datenschutzorientierten App-Ökosystem ist GrapheneOS eine wirklich praktikable Alternative zu Standard-Android oder iOS, selbst für "normale" Menschen wie Sie!

Datenlecks und umfassende Überwachung sind in der heutigen Welt so alltäglich geworden, dass sie kaum noch Schlagzeilen machen. Es liegt an Ihnen, sich selbst zu schützen. Es wird Anpassungen und Opfer auf dem Weg geben, aber Ihre Exposition gegenüber solchen Verletzungen zu reduzieren, ist bei weitem nicht so schwierig, wie Sie denken.

Ich hoffe, dieser Leitfaden hilft Ihnen auf Ihrem Weg ein Stück weiter. Wenn Ihnen dieser Leitfaden nützlich war und Sie meine Arbeit unterstützen möchten, erwägen Sie bitte eine [Spende](/tips).

Wenn Sie bereits ein GrapheneOS-Benutzer sind oder aufgrund dieses Leitfadens einer werden, erwägen Sie eine [Spende](https://grapheneos.org/donate), um ihre wichtige Arbeit zu unterstützen.

### Erfahren Sie mehr

GrapheneOS ist ein Kaninchenbau, in den jeder leicht Wochen investieren könnte. Es gibt so viel zu lernen und anzupassen, um die Erfahrung an Ihre Anforderungen und Bedrohungsmodelle anzupassen. Unten finden Sie einige Links, um Ihre Reise fortzusetzen:

- [GrapheneOS Offizieller Benutzerleitfaden](https://grapheneos.org/usage) - Offizielle Website
- [GrapheneOS Forum](https://discuss.grapheneos.org/) - Offizielle Website
- [GrapheneOS Einstellungen Meisterklasse](https://www.youtube.com/watch?app=desktop&v=GLJyD9MJgIQ) - Video von 'The Privacy Wayfinder'
- [GrapheneOS Allgemeiner Podcast](https://www.youtube.com/watch?app=desktop&v=UCPX0mFFRNA) - Podcast von 'Watchman Privacy'

Voller Kredit an: https://github.com/BitcoinQnA/Bitcoiner.Guide/blob/main/grapheneos.md
