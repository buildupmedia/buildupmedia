# Quick Start Guide

## 🚀 Schnellstart für Entwickler

### 1. Projekt klonen
```bash
git clone https://github.com/buildupmedia/buildupmedia.git
cd buildupmedia
```

### 2. VS Code öffnen
```bash
code .
```

### 3. Empfohlene Extensions installieren
VS Code sollte automatisch fragen, ob du die empfohlenen Extensions installieren möchtest:
- Live Server
- GitHub Copilot
- GitHub Copilot Chat
- Prettier
- Auto Rename Tag

### 4. Website lokal öffnen

**Option A: Live Server (empfohlen)**
1. Rechtsklick auf `index.html`
2. "Open with Live Server"
3. Browser öffnet automatisch http://localhost:8000

**Option B: Python**
```bash
python -m http.server 8000
```

**Option C: Node.js**
```bash
npx http-server -p 8000
```

## 📁 Projektstruktur

```
buildupmedia/
├── index.html              # 🏠 Haupt-Landing-Page
├── README.md              # 📖 Projekt-Dokumentation
├── TROUBLESHOOTING.md     # 🔧 Hilfe bei Problemen
├── .gitignore            # 🚫 Git-Ignores
├── .vscode/              # ⚙️ VS Code Einstellungen
│   ├── settings.json
│   └── extensions.json
├── assets/               # 🎨 Bilder und Medien
│   └── logo-info.txt
└── clients/              # 👥 Kunden-Websites
    └── karo-friseur/
        └── index.html    # Karo's Barbershop
```

## 🎯 Häufige Aufgaben

### Neue Kunden-Website hinzufügen
```bash
# 1. Neuen Ordner erstellen
mkdir -p clients/neuer-kunde

# 2. index.html erstellen
touch clients/neuer-kunde/index.html

# 3. Bearbeiten und committen
git add clients/neuer-kunde/
git commit -m "Add neuer-kunde website"
git push
```

### Änderungen an der Haupt-Page
```bash
# 1. index.html bearbeiten
code index.html

# 2. Im Browser testen (Live Server)
# 3. Committen
git add index.html
git commit -m "Update main page: [Beschreibung]"
git push
```

### GitHub Copilot verwenden

**Code-Vorschläge erhalten:**
- Einfach anfangen zu tippen
- Copilot zeigt Vorschläge in Grau
- `Tab` drücken um zu akzeptieren
- `Esc` um abzulehnen

**Copilot Chat nutzen:**
- `Cmd/Ctrl + Shift + I` für Chat öffnen
- Fragen stellen wie:
  - "Wie füge ich eine neue Sektion hinzu?"
  - "Optimiere diese CSS für Mobile"
  - "Erkläre diesen Code"

**Kommentare für bessere Vorschläge:**
```html
<!-- TODO: Füge hier eine Kontaktform ein mit Name, Email, Nachricht -->
<!-- Copilot wird automatisch HTML dafür generieren -->
```

## 🎨 Design-System

### Farben (BuildUp Media)
```css
--primary: #4f8cff      /* Blau */
--accent: #7cffc1       /* Grün */
--bg: #0b0d10          /* Dunkel */
--text: #ffffff        /* Weiß */
```

### Typografie
```css
font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto
```

### Effekte
- Glassmorphism: `backdrop-filter: blur(20px)`
- Gradient-Animationen
- Smooth Transitions: `transition: all 0.3s ease`

## 📞 Kontakt-Informationen

Immer diese Kontaktdaten verwenden:

- **WhatsApp:** +43 660 825 6468
- **Email:** BuildUpMedia2026@gmail.com
- **Instagram:** @buildupmedia2026
- **TikTok:** @buildupmedia

## ⚡ Performance-Tipps

1. **Bilder optimieren**
   - Nutze WebP Format wo möglich
   - Komprimiere Bilder vor dem Upload
   - Verwende lazy loading

2. **CSS inline halten**
   - Für kleine Projekte wie dieses
   - Reduziert HTTP-Requests
   - Schnellere Ladezeiten

3. **Externe Links**
   - Immer `target="_blank"` verwenden
   - Für Social Media Links

## 🐛 Probleme?

Siehe [TROUBLESHOOTING.md](TROUBLESHOOTING.md) für:
- GitHub Copilot Issues
- VS Code Probleme
- Git/GitHub Probleme
- Live Server Issues

## 🔐 Sicherheit

- **Keine API Keys** in den Code committen
- **Keine Passwörter** im Repository
- `.gitignore` pflegen

## 📝 Git Workflow

```bash
# 1. Neuen Branch für Feature erstellen
git checkout -b feature/neue-funktion

# 2. Änderungen machen und testen
# ...

# 3. Committen
git add .
git commit -m "Add neue-funktion: Beschreibung"

# 4. Pushen
git push origin feature/neue-funktion

# 5. Pull Request auf GitHub erstellen
```

## ✅ Checkliste vor dem Pushen

- [ ] Website im Browser getestet
- [ ] Alle Links funktionieren
- [ ] Mobile Ansicht überprüft
- [ ] Keine Tippfehler
- [ ] Keine Konsolen-Fehler
- [ ] Git Commit Message ist klar

## 🎓 Lernressourcen

- **HTML/CSS:** https://developer.mozilla.org/
- **Git:** https://git-scm.com/doc
- **GitHub Copilot:** https://docs.github.com/en/copilot
- **VS Code:** https://code.visualstudio.com/docs

---

**Viel Erfolg! 🚀**

Bei Fragen: BuildUpMedia2026@gmail.com
