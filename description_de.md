## Automatisierter TUM eAccess
Mit dem Script werden lizensierte Seiten automatisch über den eAccess Proxy der [Universitätsbibliothek der TUM](https://www.ub.tum.de/eaccess) neu geladen, um Zugriff zu den von der Bibliothek der TUM lizenzierten Inhalten zu erhalten. Beim Zugriff auf einen eMedien-Anbieter werden Sie über den Proxy geleitet und per IP-Adresse als Mitglied der TU München erkannt. Sie können so das elektronische Medienangebot der Universitätsbibliothek nutzen, als wären Sie im Netz der TUM.

Das Script automatisiert die Funktion des Bookmarklets.

## Funktionen
* Weiterleitung auf die eAccess-Version von über eAccess erreichbaren Seiten (55+ Seiten). Dafür stehen 3 Modi zur Verfügung: Silent(default), mit Weiterleitung über eine HTML-Seite und ein Modus in dem der Nutzer vor jeder Weiterleitung gefragt wird.
* Die Weiterleitung auf bestimmten Seiten kann dauerhaft unterbunden werden
* Einstellungen sind auf den eAccess-Seiten zu finden [Link](https://eaccess.ub.tum.de)
* Markierung von Seiten im eAccess-Netzwerk mit Link zu den Einstellungen

## Bitte beachten Sie!
* Sie benötigen Anmeldedaten der Universitätsbibliothek der TUM (Technische Universität München). Alle Studierenden und Mitarbeiter/-innen der TU München sind zur Nutzung von eAccess berechtigt.
* Das Skript ist eine private Entwicklung und wird nicht von der Universitätsbibliothek oder der Technischen Universität selbst herrausgegeben. Das Skript wurde nicht von der TUM oder angeschlossenen Organisationen erstellt und wird von Ihnen auch nicht unterstützt.
* Innerhalb des Netzes der TU München können Sie mit Hilfe der automatischen Proxykonfiguration auf elektronische Medien zugreifen. Sie benötigen das Script nicht auf diesen Computern.
* Beachten Sie, dass der systematische Download von Daten über eAccess aus lizenzrechtlichen Gründen nicht gestattet ist!

## Sicherheit
Es werden JavaScript-Dokumente aus externen Quellen geladen:
* Das JavaScript-Framework jQuery Version 3.1.0 [view code](https://code.jquery.com/jquery-3.1.0.min.js)

Es werden folgende Berechtigungen von Ihrem Script-Manager benötigt:
* `GM_setValue` und `GM_getValue`
  * `eAccess_reloader_mode`: *Speichert Ihre Einstellungen zum Weiterleitungsmodus*
  * `eAccess_reloader_userexclude`: *Speichert Ihre hinzugefügte Außnahmen*
  * `last_domain`, `last_domain_hostname`: *Zum komfortablen Hinzufügen von Außnahmen wird die letzte Weiterleitung lokal protokolliert.*
  * `last_version`: *Protokolliert die Versionsnummer des Userscripts lokal, um den Nutzer für den Fall größerer Änderungen am Script einfach benachrichtigen zu können*

* `GM_registerMenuCommand`: *Erzeugt Menupunkte für Ihrem Userscript Manager.*
  * *Änderung der Außnahmen*
  * *Hinzufügen von Außnahmen*
  * *Entfernen von Außnahmen*
  * *Trotz Außnahme einmalig weiterleiten*

* `GM_addStyle`: *Hinzufügen von CSS Elementen für konsistentes Aussehen erzeugter Elemente*
