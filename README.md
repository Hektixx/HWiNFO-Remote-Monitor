# HWiNFO Remote Monitor

Android-Dashboard und MyRSM mit 100-ms-Abfragen und GitHub-Releases als Update-Quelle.

## Downloads

[Neueste Version und Komplettpaket](https://github.com/Hektixx/HWiNFO-Remote-Monitor/releases/latest)

- Komplettpaket herunterladen, entpacken und `START.cmd` oeffnen.
- `Updates-einrichten.cmd` aktiviert die Windows-Pruefung bei Anmeldung und taeglich um 18:00 Uhr.
- Die APK auf dem Telefon installieren. Unter Verbindung > App-Updates ist dieses Repository bereits eingetragen.

## Updates

Die Android-App prueft beim Oeffnen hoechstens einmal taeglich auf Updates, laedt neue APKs herunter und prueft SHA-256, Paketname, Version und Signatur. Android verlangt eine Installationsbestaetigung.

Der Windows-Updater laedt passende MyRSM-Pakete automatisch. Der Diensttausch wird mit Administratorbestaetigung gestartet und erstellt vorher eine Sicherung. Der 100-ms-Patch bleibt erhalten.

HWiNFO wird nicht im Paket weiterverteilt. Der Paketstarter verlinkt den [offiziellen Download](https://www.hwinfo.com/download/). Eingebaute automatische HWiNFO-Updates erfordern Pro; die Free-Version begrenzt Shared Memory auf 12 Stunden. [Herstellerangaben](https://www.hwinfo.com/licenses/)

## Quellen und kuenftige Releases

Die passenden Android-, MyRSM- und Qt-Quellen liegen im Komplettpaket beziehungsweise als Release-Assets vor. Die Testdaten im Android-Quellarchiv sind synthetisch. Private Sensorprotokolle und Signierschluessel werden nicht veroeffentlicht. MyRSM basiert auf [qdel/myrsm](https://github.com/qdel/myrsm), GPLv3.

Pro Release muessen `update.json`, `HWiNFO-Remote-Monitor.apk` und `MyRSM-100ms-Windows-x64.zip` hochgeladen werden. `Release-vorbereiten.ps1` erzeugt das Manifest mit den Pruefsummen. Die Android-versionCode muss steigen; der private Signierschluessel muss derselbe bleiben. Neue Programmversionen muessen gebaut und veroeffentlicht werden, bevor die Updater sie verteilen koennen.

Das Windows-Installationsskript ist fuer die vorhandene MyRSM-Dienstinstallation und die 413/24-Sensor-Konfiguration des urspruenglichen PCs vorbereitet. Kein universeller Erstinstaller.

100 ms bezeichnet den Abfrage- und Sendetakt. Die echte Sensorfrische bestimmt HWiNFO.
