# BITS Behörden-IT-Sicherheitstraining


Stand: 01.10.2024

Ansprechpartner: Dr. Lutz Gollan, Landesbetrieb Verkehr, Hamburg
E-Mail: [g@backbeat.eu](mailto:g@backbeat.eu)

## 1. Überblick

Unter dem Titel „BITS Behörden-IT-Sicherheitstraining“ hat im Jahr 2006 eine Arbeitsgruppe des Arbeitskreises Informationstechnologie des Städte- und Gemeindebundes Nordrhein-Westfalen das für Unternehmen konzipierte Computersicherheitstraining „open beware!“ an die Anforderungen von Behörden und anderen Einrichtungen angepasst. Mittlerweile liegt die aktualisierte Version 6 vor. Seit 2006 wird BITS von der Kommunal Agentur NRW GmbH (https://www.kommunalagenturnrw.de) mit Unterstützung von Dr. Lutz Gollan, Landesbetrieb Verkehr, Hamburg, herausgegeben.

Der Quellcode für BITS ist unter https://github.com/BITS-Training/BITS-hugo kostenfrei verfügbar. Die URL für die Online-Version lautet https://www.bits-training.de. BITS steht unter Creative Commons-Lizenz BY-SA 4.0 und kann beliebig angepasst werden (siehe unten 7.).

## 2. Ziel

Durch das Training sollen die Mitarbeiterinnen und Mitarbeiter von Behörden und anderen Einrichtungen, die regelmäßig an IT-Arbeitsplätzen und insbesondere mit dem Internet beschäftigt sind, durch gezielte Information und Selbstlerneinheiten für die Sicherheitsaspekte der Computer- und Internetnutzung sensibilisiert werden.

Das Training ist kostenlos, anpassbar und vollständig browserbasiert nutzbar.

## 3. Installation und Anpassung

BITS wird in zwei Versionen angeboten: Eine Version für die Verwendung mit einem Webserver (Dateiname \*webroot\*) und eine Version für die Verwendung direkt aus dem Dateisystem (z.B. Fileserver, Dateifreigabe, USB-Stick) (Dateiname \*fileshare\*). Die Versionen werden auf der [Releases-Seite](https://github.com/BITS-Training/BITS-hugo/releases) des GitHub-Repositorys veröffentlicht.

Vor der Veröffentlichung sollten einige Dateien auf die eigenen Bedürfnisse angepasst und mit passenden Daten befüllt werden (siehe unten "Anpassung").

Im [BITS-Portal](https://www.bits-portal.eu) befinden sich mehrere leicht verständliche Tutorial-Videos, die alle erforderlichen Schritte umfassend darstellen.

### Installation

Die Release-ZIPs mit den HTML-Dateien sind zu entpacken und die benötigten Anpassungen vorzunehmen, anschließend snid alle Dateien in das Verzeichnis des Webservers oder in den Ordner für die Veröffentlichung zu kopieren.

Als Startseite kann direkt auf den Root-Ordner (Webserver-Version) bzw. auf die Seite index.html (Fileserver-Version) verlinkt werden.

### Anpassung

Technisch kann die Anpassung von BITS an die lokalen Anforderungen über das direkte Bearbeiten der statischen HTML-Seiten aus den Releases, oder, vorzugsweise, über die Änderung der Markdown-Textdateien, die im BITS-Repository liegen, erfolgen. Für den zweiten Weg empfiehlt sich die Nutzung des Open Source-Werkzeugs hugo in Verbindung mit der Versionsverwaltung Git, um die statischen Webseiten neu zu erstellen. Näheres ist in der [README.md-Datei](https://github.com/BITS-Training/BITS-hugo#readme) beschrieben.

* Die Datenschutzerklärung muss angepasst werden - und, wenn die eigene Version im Internet veröffentlicht werden soll, auch das Impressum. Diese Daten liegen im Repository unter \content\mehr und bei den Release-Versionen im Ordner \mehr (Fileserver-Version) oder in den entsprechenden Unterordnern datenschutz bzw. impressum (Webserver-Version). Falls man mit hugo arbeitet kann die Impressumsdatei einfach bei fehlendem Bedarf aus den Daten gelöscht werden.
* Vor der Freigabe für die Beschäftigten muss die Seite „Ansprechpersonen“ für die entsprechende Behörde oder Einrichtung angepasst werden. Dies ist die Datei "\mehr\ansprechpersonen\index.html". Im Repository liegt sie unter \content\ansprechpersonen.
* Anderslautende Dienstvereinbarungen oder -anweisungen könnten zu Änderungsbedarfen in den Lektionen "E-Mail" und "Vertrauliche Daten" sowie "KI" führen.
* Individuelle Verweise auf weitere Informationsquellen können in der Datei "\mehr\weitere-informationen\index.html" (Webserver) oder "\mehr\weitere-informationen.html" (File-Server) bzw. \content\mehr\Weitere-Informationen.md (Repository) verlinkt werden.
* Variablen wie z.B. die an einigen Stellen empfohlene Mindestpasswortlänge, werden über die Datei config/_default/config.toml gesteuert. Wie diese zu verwenden sind, wird in der Datei ReLearnTheme-HowTo.md im obersten Ordner erläutert. Dies erfordert im Nachgang ein Erzeugen der statischen HTML-Seiten über Hugo.
* Das BITS-Logo kann durch ein eigenes ersetzt werden: Einfach die Datei "\static\images\logo.png" (Repository) bzw. im Ordner \images (Fileserver-Version und Webserver-Version) oder überschreiben. Das Bild sollte 200px breit und 200px hoch sein.
* Farbliche Anpassungen der Links, der Suchbox etc. sind über die Dateien in \static\css im Repository bzw. \css in den Release-Versionen möglich.

## 4. Bedienung und technische Anforderungen

Die Bedienung von „BITS Behörden-IT-Sicherheitstraining“ erfolgt durch den Aufruf des Root-Ordners (Webserver-Version) oder der „index.html“-Datei (Fileserver-Version) im Browser durch die Beschäftigten. Anschließend können die weitestgehend barrierefreien Seiten durch die Maus oder durch die Pfeiltasten der Tastatur genutzt werden.

BITS unterstützt grundsätzlich jeden aktuellen Browser. JavaScript muss aktiviert sein, andernfalls kommt es bei der Navigation und bei den Wissenstests zu Problemen. Eine Soundkarte bzw. Lautsprecher sind zur Nutzung nicht erforderlich. Es ist auch eine Nutzung über mobile Endgeräte möglich. BITS wurde mit den Browsern MS Edge, Vivaldi, Firefox und Chrome sowie Safari getestet.

Im Hauptmenü stehen links unten drei Kontraststufen zur individuellen Auswahl bereit.

## 5. Statistische Auswertungen

BITS ist auf die Nutzung von [Matomo](https://matomo.org) und [Goatcounter](https://www.goatcounter.com) zu statistischen, anonymisierten Nutzungsauswertungen vorbereitet. Dies erfordert ein Erzeugen der statischen HTML-Seiten über Hugo. Die jeweilige Konfiguration der beiden Dienste ist in der Datei \config\_default\config.toml dokumentiert.

## 6. Gewinnspiel

Es besteht die Möglichkeit, dass bei den Quizzes am Ende der Lektionen bei Anklicken der richtigen Antwort Buchstaben eingeblendet werden. Wenn die entsprechenden Buchstaben durch die Beschäftigten innerhalb eines Gewinnspiels der Behörde oder Einrichtung an eine interne Stelle eingesendet werden und eine Losziehung erfolgt, kann so ein Anreiz zur Nutzung von BITS geschaffen werden.

Dazu muss in den Ordnern der Lektionen die jeweilige Datei "Quiz" mit einem Text-Editor geöffnet werden. Dort ist dann bei der jeweiligen Zeile "Richtige Antwort" der gewünschte Lösungsbuchstaben (ggf. auch ein Sonderzeichen wie Unterstrich oder Komma) zu hinterlegen, also z.B. "Richtige Antwort. Notieren Sie sich den Lösungsbuchstaben **B**".

Bei der Auswahl der Lösungsbuchstaben sollte man sich zuvor einen Lösungssatz überlegen, der aus 37 Lösungsbuchstaben besteht - dies ist die Anzahl der Fragen aller Quizzes. Diesen könnten dann die Nutzer:innen im Rahmen einer Awareness-Kampagne per E-Mail einsenden um einer Verlosung, z.B. von Kino-Gutscheinen, teilzunehmen.

## 7. BITS-Portal

Für Administratoren steht kostenfrei das BITS-Portal https://www.bits-portal.eu zur Verfügung. Dort werden neue Funktionen und Inhalte vorgestellt. Außerdem steht dort ein Newsletter zum Abonnieren bereit.


## 8. Rechtliches

Urheber von BITS ist Dr. Lutz Gollan vom Landesbetrieb Verkehr, Hamburg.

Die technische Realisierung erfolgt durch Andreas Hösl von der Chr. Mayr GmbH + Co. KG.

Das verwendete [hugo-Framework](https://gohugo.io/) steht unter der [Apache-Lizenz, v2.0](https://www.apache.org/licenses/LICENSE-2.0), das [Relearn-Theme](https://themes.gohugo.io/hugo-theme-relearn/) und das [Quiz](https://bonartm.github.io/hugo-quiz/) inkl. [quizdown-js](https://github.com/bonartm/quizdown-js) und die [jQuery-Bibliothek](https://jquery.com) unter der [MIT-Lizenz](https://opensource.org/licenses/MIT). Die Icons stammen von https://fontawesome.com und sind Open Source. Das Bild auf der 404-Fehlerseite ist open source: Photo by [Donald Giannatti](https://unsplash.com/@wizwow?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) on [Unsplash](https://unsplash.com/s/photos/deadend?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText).

BITS ist kostenlos und steht unter der Creative Commons (CC) Lizenz BY-SA (https://creativecommons.org/licenses/by-sa/4.0/deed.de).


Sie dürfen:

- Teilen:
  das Material in jedwedem Format oder Medium vervielfältigen und weiterverbreiten
- Bearbeiten:
  das Material remixen, verändern und darauf aufbauen und zwar für beliebige Zwecke, sogar kommerziell.


Der Lizenzgeber kann diese Freiheiten nicht widerrufen solange Sie sich an die Lizenzbedingungen halten:

- Namensnennung
  Sie müssen angemessene Urheber- und Rechteangaben machen, einen Link zur Lizenz (diese Seite) beifügen und angeben, ob Änderungen vorgenommen wurden. Diese Angaben dürfen in jeder angemessenen Art und Weise gemacht werden, allerdings nicht so, dass der Eindruck entsteht, der Lizenzgeber unterstütze gerade Sie oder Ihre Nutzung besonders.
- Weitergabe unter gleichen Bedingungen
  Wenn Sie das Material remixen, verändern oder anderweitig direkt darauf aufbauen, dürfen Sie Ihre Beiträge nur unter derselben Lizenz wie das Original verbreiten.
- Keine weiteren Einschränkungen
  Sie dürfen keine zusätzlichen Klauseln oder technische Verfahren einsetzen, die anderen rechtlich irgendetwas untersagen, was die Lizenz erlaubt.

Beim Kapitel "Cloud" hat Frau Heike Brzezina wertvolle Hinweise gegeben.

## 9. Feedback

### via E-Mail

Änderungs- oder Ergänzungswünsche nimmt Dr. Lutz Gollan ([g@backbeat.eu](mailto:g@backbeat.eu)) gerne entgegen. 

### via GitHub

Der Quellcode von [BITS](https://github.com/BITS-Training/BITS-hugo) ist auf GitHub öffentlich verfügbar. Mit [hugo](https://gohugo.io) kann man daraus die statischen Seiten bauen.

Anregungen, Wünsche und Bugs können einfach mit Hilfe von [Issues](https://github.com/BITS-Training/BITS-hugo/issues) mitgeteilt und besprochen werden. Und wer sich richtig mit Git und GitHub auskennt, kann auch das gesamte Repository forken und Anpassungen selbst vornehmen. Über einen Pull-Request würden wir uns dann sehr freuen.

### via IT-SiBe-Forum
Beschäftigte aus dem öffentlichen Dienst, die im Bereich der Informationssicherheit tätig sind, können sich im [IT-Sicherheitsbeauftragten-Forum](https://it-sibe-forum.de) und dem dortigen [Unterforum](https://it-sibe-forum.de/index.php?board=98.0) zu BITS austauschen.
