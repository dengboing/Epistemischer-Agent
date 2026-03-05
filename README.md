# Epistemischer Assistent

**Werkzeug für kritisches Denken** — basierend auf Kants „Sapere Aude" und Freires kritischer Pädagogik.

Von [Dirk Hermann](https://dirkdenkt.de)

---

## Deployment auf GitHub Pages

### Schritt 1: Repository erstellen

1. GitHub.com öffnen → **New repository**
2. Name: `epistemischer-assistent`
3. Visibility: **Public** (für GitHub Pages kostenlos)
4. **Create repository** klicken

### Schritt 2: Dateien hochladen

```bash
git clone https://github.com/DEIN-USERNAME/epistemischer-assistent.git
cd epistemischer-assistent

# Alle Dateien aus diesem Paket in den Ordner kopieren
# (oder per Drag & Drop auf GitHub hochladen)

git add .
git commit -m "Initial deployment"
git push origin main
```

### Schritt 3: GitHub Pages aktivieren

1. Repository → **Settings** → **Pages**
2. Source: **GitHub Actions**
3. Speichern

### Schritt 4: Warten & öffnen

Nach ca. 2 Minuten ist die App verfügbar unter:
```
https://DEIN-USERNAME.github.io/epistemischer-assistent/
```

---

## Lokale Entwicklung

```bash
npm install
npm run dev
```

App läuft dann auf `http://localhost:5173`

---

## WICHTIG: vite.config.js anpassen

Wenn dein Repository **nicht** `epistemischer-assistent` heißt, passe die `base`-URL in `vite.config.js` an:

```javascript
export default defineConfig({
  base: '/DEIN-REPO-NAME/',  // ← hier anpassen
})
```

---

## API-Key (optional)

Im Demo-Modus läuft die App ohne API-Key mit simulierten Antworten.

Für Live-Antworten (echter Claude):
1. [Anthropic Console](https://console.anthropic.com) → API Keys → Create Key
2. App öffnen → "API-Key eingeben" → Key eingeben → Live-Modus aktivieren

Der Key wird nur lokal im Browser gespeichert (localStorage).

---

## Technologie

- React 18 + Vite
- GitHub Actions (CI/CD)
- GitHub Pages (Hosting)
- Anthropic API (optional)

---

## Lizenz

Persönliches Projekt. Keine kommerzielle Nutzung ohne Genehmigung.
