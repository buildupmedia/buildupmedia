# Troubleshooting Guide - Agent & VS Code Issues

## Problem: "Agent auf VS kann nix mehr machen wie gestern" 

Diese Anleitung hilft bei Problemen mit GitHub Copilot Agent und VS Code.

## 🔧 Schnelle Lösungen

### 1. GitHub Copilot funktioniert nicht

**Problem:** Copilot gibt keine Vorschläge mehr oder reagiert nicht.

**Lösung:**
```bash
# In VS Code:
1. Drücke Cmd/Ctrl + Shift + P
2. Suche nach "GitHub Copilot: Sign Out"
3. Melde dich ab und wieder an
4. Oder: "Developer: Reload Window"
```

**Alternative:**
- Überprüfe deine GitHub Copilot Lizenz unter: https://github.com/settings/copilot
- Stelle sicher, dass die Copilot Extension aktiv ist (grünes Icon unten rechts)

### 2. VS Code Extension Installation

**Erforderliche Extensions:**
```json
- Live Server (ritwickdey.liveserver)
- GitHub Copilot (GitHub.copilot)
- GitHub Copilot Chat (GitHub.copilot-chat)
```

**Installation:**
1. Öffne VS Code
2. Gehe zu Extensions (Cmd/Ctrl + Shift + X)
3. VS Code sollte automatisch vorschlagen, die empfohlenen Extensions zu installieren
4. Oder installiere sie manuell

### 3. Live Server startet nicht

**Problem:** Website lässt sich nicht lokal öffnen.

**Lösung 1 - Live Server:**
```bash
1. Installiere "Live Server" Extension
2. Rechtsklick auf index.html
3. "Open with Live Server"
```

**Lösung 2 - Python:**
```bash
cd /pfad/zum/projekt
python -m http.server 8000
# Öffne: http://localhost:8000
```

**Lösung 3 - Node.js:**
```bash
npx http-server -p 8000
# Öffne: http://localhost:8000
```

### 4. Git/GitHub Probleme

**Problem:** Änderungen können nicht committed/gepushed werden.

**Lösung:**
```bash
# Überprüfe Git Status
git status

# Stelle sicher, dass du auf dem richtigen Branch bist
git branch

# Füge Änderungen hinzu
git add .

# Committe mit Nachricht
git commit -m "Deine Änderung beschreiben"

# Pushe zum Remote Repository
git push
```

### 5. Permission/Authentifizierung Probleme

**Problem:** Git fragt nach Authentifizierung oder verweigert Push.

**Lösung:**
```bash
# Überprüfe Remote URL
git remote -v

# Stelle sicher, dass du eingeloggt bist
# Für GitHub CLI:
gh auth login

# Oder verwende Personal Access Token
# Erstelle Token unter: https://github.com/settings/tokens
```

### 6. Copilot Agent reagiert langsam oder gar nicht

**Ursachen:**
- Netzwerkprobleme
- GitHub Copilot Service Ausfall
- Rate Limiting
- Abgelaufene Session

**Lösungen:**
```bash
# 1. Überprüfe Copilot Status
# Gehe zu: https://www.githubstatus.com/

# 2. Lade VS Code neu
Cmd/Ctrl + Shift + P → "Developer: Reload Window"

# 3. Überprüfe Internetverbindung
ping github.com

# 4. Überprüfe Copilot Logs
Cmd/Ctrl + Shift + P → "GitHub Copilot: Show Output"
```

### 7. VS Code Settings zurücksetzen

**Problem:** VS Code verhält sich seltsam.

**Lösung:**
```bash
# Settings zurücksetzen (Vorsicht: löscht deine Einstellungen!)
# Auf macOS:
rm -rf ~/Library/Application\ Support/Code/

# Auf Windows:
# Lösche: %APPDATA%\Code

# Auf Linux:
rm -rf ~/.config/Code/
```

## ✅ Checkliste zur Problemlösung

- [ ] GitHub Copilot Lizenz ist aktiv
- [ ] Copilot Extension ist installiert und aktiviert
- [ ] VS Code ist auf dem neuesten Stand
- [ ] Git ist korrekt konfiguriert
- [ ] Internetverbindung funktioniert
- [ ] Keine Proxy/Firewall blockiert GitHub
- [ ] VS Code wurde neugestartet

## 📞 Support

Falls die Probleme weiterhin bestehen:

1. **Überprüfe GitHub Status:** https://www.githubstatus.com/
2. **GitHub Copilot Docs:** https://docs.github.com/en/copilot
3. **VS Code Issues:** https://github.com/microsoft/vscode/issues

## 🚀 Best Practices

### Für optimale Agent-Performance:

1. **Klare Kommentare schreiben:**
   ```html
   <!-- TODO: Füge eine neue Sektion für Testimonials hinzu -->
   ```

2. **Dateien klein halten:**
   - Große Dateien splitten
   - Komponenten auslagern

3. **Regelmäßig speichern:**
   - Copilot arbeitet besser mit gespeicherten Dateien

4. **Kontext geben:**
   - Relevante Dateien geöffnet halten
   - Klare Dateinamen verwenden

## 🔍 Debugging

### Copilot Debug-Modus aktivieren:

```json
// In VS Code settings.json
{
  "github.copilot.advanced": {
    "debug.showScores": true,
    "debug.overrideEngine": "gpt-4"
  }
}
```

### Logs überprüfen:

```bash
# VS Code Output Panel öffnen
Cmd/Ctrl + Shift + U

# Wähle "GitHub Copilot" aus dem Dropdown
```

## 📝 Häufige Fehler

### "Copilot kann nicht verwendet werden"
→ Überprüfe deine Lizenz und logge dich neu ein

### "No suggestions"
→ Warte ein paar Sekunden, Copilot braucht Zeit

### "Rate limit exceeded"
→ Warte 10-15 Minuten und versuche es erneut

### "Extension not responding"
→ Lade VS Code neu (Cmd/Ctrl + R)

## 🎯 Projekt-spezifische Hinweise

**Für dieses BuildUp Media Projekt:**

- Hauptdatei: `index.html`
- Kunden-Projekte: `clients/` Ordner
- Assets: `assets/` Ordner
- Keine Build-Tools erforderlich
- Reine HTML/CSS/JavaScript Website

**Zum Testen:**
1. Öffne `index.html` direkt im Browser, oder
2. Verwende Live Server Extension, oder
3. Starte Python/Node Server

---

*Letzte Aktualisierung: 17. Februar 2026*
