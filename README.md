# divera_macrodroid_standort
Anleitung und Config zum übermitteln des Fahrzeugstandorts an Divera24/7

Diese Anleitung beschreibt wie man den Standort eines Androidtablets und somit z.B. eines Fahrzeuges regelmäßig an Divera 24/7 übertragen kann.
Grundlage dafür ist die App MacroDroid (https://play.google.com/store/apps/details?id=com.arlosoft.macrodroid) sowie in Ergänzung die App GPS Connected (https://play.google.com/store/apps/details?id=org.bruxo.gpsconnected). Warum diese benötigt wird erkläre ich später genauer.

Zuerst muss in der Weboberfläche von Divera ein Fahrzeug angelegt werden. Dazu klickt ihr unter Verwaltung-> Einstellungen-> Setup-> Fahrzeuge auf +Fahrzeug. Hier müsst ihr neben dem Fahrzeugtyp in langer und kurzer Schreibweise auch unbendingt einen Funkrufnamen eintragen. Dieser wird später zur Identifikation des Fahrzeugs genutzt und sollte deshalb auch keine Leerzeichen enthalten und möglichst kurz gehalten werden. Eine verkürzte Version der OPTA auf Block 4.1 und 4.3 (z.B. 19-48-3) wäre hier z.B. möglich. Den Funkrufnamen sowie den Accesskey eurer Einheit (zu finden unter Verwaltung-> Schnittstellen-> API) solltet ihr euch nun notieren oder in eine Textdatei kopieren.

Nun könnt ihr auf dem Tablet MacroDroid installieren. Dazu einfach dem Link oben zum Playstore folgen. Nach der Installation öffnet ihr die App und klickt euch kurz durchs Tutorial durch. Anschließend klickt ihr auf das Zahnrad um in die Einstellungen der App zu gelangen. Dort wählt ihr den obersten Punkt "Akkuoptimierung ignorieren" und stellt so sicher das Android die App nicht beendet wenn sie im Hintergrund läuft.
Jetzt könnt ihr die hier im Repository verfügbare Macro-Datei in MacroDroid importieren. Dazu die Datei auf euer Gerät herunterladen und auf der Startseite von MacroDroid auf Export/Import klicken. Hier unter Import-> Speicher die heruntergeladene Datei auswählen und bestätigen.

Nach dem Import müsst ihr das Macro mit euren Daten anpassen. Dazu unter dem Tab Makros das importierte Macro gedrückt halten und im auftauchenden Fenster auf editieren klicken. Nun auf auf "HTTP GET" drücken und "einrichten" auswählen. Im Textfeld müsst ihr nun in der vorhandenen URL euren Accesskey und den Funkrufnamen des Fahrzeugs einsetzten. Anschließend auf "OK" und den Pfeil oben links in der Ecke klicken. Dann auf "Speichern" drücken. Nun sendet MacroDroid den Standort alle 60 Sekunden an Divera.

Um zu garantieren, dass immer ein möglichst aktueller Standort an Divera versendet wird muss nun noch die App GPS Connected installiert werden. Nach dem öffnen der App müsst ihr einfach auf GPS Lock drücken und könnt die App dann wieder schließen. Dadurch wird dauerhaft der Standort ermittelt und nicht wie sonst bei Android üblich nur bei öffnen einer App der Standort abgerufen. Auch diese App müsst ihr in den Androideinstellungen vom Aukkusparmodus ausschließen.

FERTIG! Jetzt sollte das Tablet alle 60 Sekunden seinen Standort an Divera senden und das Fahrzeug auf der Karte im Monitor auftauchen.

Solltet ihr Tablets mit älteren Androidversionen unter 4.2 verwenden müsst ihr euch die apk-Datei über einen anderen apk-Hoster beziehen. Je nach dem Stand der Sicherheitsupdates auf eurem Gerät kann es dann jedoch sein, dass die Root Zertifikate auf eurem Gerät nicht mehr aktuell genug sind und bei dem Aufrufen der Divera Website Fehler auftreten. Deshalb nutzt am besten nur Androidversionen 6.0 und höher und erspart euch eine Menge Kopfschmerzen ;) 

