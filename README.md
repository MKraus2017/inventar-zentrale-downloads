# Inventar Zentrale – Downloads

Inventar Zentrale verwaltet Mitarbeiter, Geräte, Softwarelizenzen, Verträge und Rechnungen auf einem Windows Server.

**[Aktuelle Version herunterladen](https://github.com/MKraus2017/inventar-zentrale-downloads/releases/latest)**

## Installation und Updates

- **Setup-ZIP mit Protokoll:** ZIP entpacken und `Start-Setup-mit-Protokoll.cmd` starten. Es enthält den MSI-Installer mit automatischer Erkennung einer vorhandenen Installation.
- **CORE-ZIP:** Paket für das mitgelieferte PowerShell-Updateverfahren und für den automatischen Updatekanal.
- **Bestehende Daten:** Die Installationsverfahren verwenden die vorhandene Datenablage und sichern vor einem Update. Die Anleitung und den Validierungsnachweis des jeweiligen Pakets beachten.

Ab Version 1.7.2 ist dieser öffentliche Kanal standardmäßig eingerichtet. Versionsprüfung und Download benötigen weder GitHub-Anmeldung noch Zugriffstoken. Die Anwendung prüft alle sechs Stunden; der Superadmin entscheidet über die Installation.

Für ältere Installationen den Kanal auf dem Inventar-Server in PowerShell als Administrator einrichten:

```powershell
powershell.exe -NoProfile -ExecutionPolicy Bypass -File "C:\Program Files\InventarZentrale\Configure-GitHubUpdates.ps1" -Repository "MKraus2017/inventar-zentrale-downloads"
```

Danach den Browser neu laden und **Einstellungen & AD → Updates → Jetzt prüfen** wählen. Das Konfigurationsskript startet den Dienst neu. Bei anderem Installationspfad den Skriptpfad und `-InstallPath` anpassen.

## Softwarelizenz

Die Software wird mit Standard- und Pro-Lizenzen aktiviert. Der öffentliche Download hebt die Lizenzpflicht für Bearbeitung und Updateinstallation nicht auf. Nach Ablauf folgen 30 Tage Toleranz. Danach bleiben Anmeldung, Lesen, Export und Datensicherung möglich.

Dieses Repository verteilt fertige, neutrale Kundenpakete und Anleitungen. Anbieterportal, private Signierschlüssel und Kundenbestände werden hier nicht veröffentlicht. Die Releasebeschreibungen und `VALIDATION.json` dokumentieren Änderungen und Prüfungen.
