# divera_macrodroid_standort
!WIP! Anleitung und Config zum übermitteln des Fahrzeugstandorts an Divera24/7

Diese Anleitung beschreibt wie man den Standort eines Androidtablets und somit z.B. eines Fahrzeuges regelmäßig an Divera 24/7 übertragen kann.
Grundlage dafür ist die App MacroDroid (https://play.google.com/store/apps/details?id=com.arlosoft.macrodroid) sowie in Ergänzung die App GPS Connected (https://play.google.com/store/apps/details?id=org.bruxo.gpsconnected). Warum diese benötigt wird erkläre ich später genauer.

Zuerst muss in der Weboberfläche von Divera ein Fahrzeug angelegt werden. Dazu klickt ihr unter Verwaltung-> Einstellungen-> Setup-> Fahrzeuge auf +Fahrzeug. Hier müsst ihr neben dem Fahrzeugtyp in langer und kurzer Schreibweise auch unbendingt einen Funkrufnamen eintragen. Dieser wird später zur Identifikation des Fahrzeugs genutzt und sollte deshalb auch keine Leerzeichen enthalten und möglichst kurz gehalten werden. Eine verkürzte Version der OPTA auf Block 4.1 und 4.3 (z.B. 19-48-3) wäre hier z.B. möglich. Den Funkrufnamen sowie den Accesskey eurer Einheit (zu finden unter Verwaltung-> Schnittstellen-> API) solltet ihr euch nun notieren oder in eine Textdatei kopieren.

Nun könnt ihr auf dem Tablet MacroDroid installieren. Dazu einfach dem Link oben zum Playstore folgen. Nach der Installation öffnet ihr die App und klickt euch kurz durchs Tutorial durch. Anschließend klickt ihr auf das Zahnrad um in die Einstellungen der App zu gelangen. Dort wählt ihr den obersten Punkt "Akkuoptimierung ignorieren" und stellt so sicher das Android die App nicht beendet wenn sie im Hintergrund läuft.
Jetzt könnt ihr die hier im Repository verfügbare Macro-Datei in MacroDroid importieren. Dazu die Datei auf euer Gerät herunterladen und auf der Startseite von MacroDroid auf Export/Import klicken. Hier unter Import-> Speicher die heruntergeladene Datei auswählen und bestätigen.
ACHTUNG!: In der Free Version von MacroDroid werden beim Import alle anderen Macros überschrieben. Dies sollte für die alleinige Verwendung mit Divera jedoch egal sein.
Nach dem Import müsst ihr das Macro mit euren Daten anpassen. Dazu unter dem Tab Makros das importierte Macro gedrückt halten und im auftauchenden Fenster auf editieren klicken.

Solltet ihr Tablets mit älteren Androidversionen unter 4.2 verwenden müsst ihr euch die apk-Datei über einen anderen apk-Hoster beziehen. Je nach dem Stand der Sicherheitsupdates auf eurem Gerät kann es dann jedoch sein, dass die Root Zertifikate auf eurem Gerät nicht mehr aktuell genug sind und bei dem Aufrufen der Divera Website Fehler auftreten. Deshalb nutzt am besten nur Androidversionen 6.0 und höher und erspart euch eine Menge Kopfschmerzen ;) 

