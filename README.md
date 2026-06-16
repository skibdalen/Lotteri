# 🎰 SpareBank 1 Lotteri - HTML Versjon

En moderne lotteri-applikasjon **100% kjørt i nettleseren** - ingen installasjon eller backend nødvendig!

![Lisens](https://img.shields.io/badge/Lisens-MIT-green?style=flat-square)
![HTML5](https://img.shields.io/badge/HTML5-100%25-E34C26?style=flat-square)
![Responsive](https://img.shields.io/badge/Responsive-Mobile%2B%2B-blue?style=flat-square)

---

## 🚀 Kjør nå

### **Lokalt (raskest)**
1. Last ned `index.html`
2. Dobbeltklikk på filen → åpnes i nettleseren
3. **Done!** Ingen installasjon needed

### **Fra GitHub Pages**
https://ditt-brukernavn.github.io/Vinlotteri/

(Erstatt `ditt-brukernavn` med din GitHub-bruker)

---

## ✨ Funksjoner

✅ **Sekvensielle trekninger** - trekk en vinner av gangen  
✅ **Animert lotterihjul** - visuelt tiltalende spinning  
✅ **Automatisk historikk** - alle trekninger lagres lokalt  
✅ **Statistikk** - se hvor ofte hver person vinner  
✅ **Excel-import/eksport** - les fra og eksporter til Excel  
✅ **SpareBank 1 design** - profesjonell UI  
✅ **Ingen backend** - rent JavaScript, 100% offline capable  
✅ **LocalStorage** - data lagres i nettleseren  

---

## 📖 Bruk

### 1. Legg til deltakere

**Alternativ A: Manuell**
- Skriv navn (påkrevd)
- E-post (valgfritt)
- Antall lodd (hvor mange ganger de kan vinne)
- Klikk "Legg til deltaker"

**Alternativ B: Importer Excel**
- Klikk "Importer" fanen
- Velg Excel-fil (må ha kolonnene: Navn, E-post, Antall lodd)
- Data importeres automatisk

### 2. Start trekningssesjon

1. Skriv antall priser (f.eks. "3")
2. Klikk "Start trekningssesjon"
3. Status vises: "0 / 3"

### 3. Trekk vinnere - en og en

```
Klikk "Trekk neste vinner"
    ↓
Hjulet spinner i 2 sekunder
    ↓
Vinner vises både på hjul + liste
    ↓
Status: "1 / 3"
    ↓
Gjenta til alle er trukket
```

### 4. Lagre resultatet

Når alle er trukket:
- Klikk "💾 Lagre vinnere"
- Lagres lokalt i nettleseren
- Oppdateres i historikk-fanen

### 5. Se historikk & statistikk

**Historikk-fanen:**
- Se alle tidligere trekninger med dato
- Hvem vant når

**Statistikk-fanen:**
- Hvor mange ganger hver person har vunnet
- Sortert etter gevinster

**Eksport:**
- Klikk "Last ned historikk (Excel)"
- Fil `lotteri_historikk.xlsx` lastes ned

---

## 💾 Datahåndtering

### Hvor lagres data?

**Deltakere:**
- Lagres i `localStorage` (nettleseren)
- Kan importeres/eksporteres som Excel

**Historikk:**
- Lagres i `localStorage` (nettleseren)
- Kan eksporteres som Excel
- **Slettes hvis du tømmer nettleserkake** (Clear Browser Data)

### Backup av data

```
1. Gå til "Trekkings-historikk"
2. Klikk "Last ned historikk (Excel)"
3. Fil lagres på PC
4. Sikkerhetskopi av all data!
```

---

## 🌐 GitHub Pages Setup

### 1. Lag repository på GitHub

```bash
# Lag repo på GitHub.com
# Navn: Vinlotteri
# Public
```

### 2. Pushe koden

```bash
cd Vinlotteri
git init
git add index.html README.md .gitignore
git commit -m "Init: SpareBank 1 Lottery HTML app"
git remote add origin https://github.com/DIN-BRUKERNAVN/Vinlotteri.git
git branch -M main
git push -u origin main
```

### 3. Aktiver GitHub Pages

1. Gå til Settings på GitHub-repo
2. Klikk "Pages" (venstre meny)
3. Source: `main` branch → `/root`
4. Save

**URL blir:** `https://DIN-BRUKERNAVN.github.io/Vinlotteri/`

---

## 🔒 Sikkerhet & Privacy

✅ **100% offline** - alt kjøres i nettleseren  
✅ **Ingen data sendes til server** - alt lagres lokalt  
✅ **Åpent kildekode** - kode kan inspekteres  
✅ **Ingen sporing** - ingen analytics eller cookies  

---

## 🛠 Teknisk Info

### Stack
- **Frontend:** HTML5 + CSS3 + Vanilla JavaScript
- **Excel:** SheetJS (xlsx library)
- **Data:** Browser localStorage
- **Hosting:** GitHub Pages (gratis!)

### Avhengigheter (fra CDN)
- SheetJS v0.18.5 (Excel-lesing/skriving)
- FileSaver.js (Download-funksjonalitet)
- Source Sans 3 font (Google Fonts)

### Nettleser-kompatibilitet
✅ Chrome/Chromium (✓✓✓)
✅ Firefox (✓✓✓)
✅ Safari (✓✓)
✅ Edge (✓✓✓)

---

## 📝 Filstruktur

```
Vinlotteri/
├── index.html          # Hele applikasjonen (en fil!)
├── README.md           # Denne filen
├── .gitignore         # Git rules
└── LICENSE            # MIT License
```

**Det er det!** Bare en HTML-fil + readme!

---

## ⚙️ Lokalt oppsett

### Windows
```
1. Last ned index.html
2. Dobbeltklikk
3. Vips! 🎉
```

### macOS / Linux
```
1. Last ned index.html
2. Åpne i nettleser (eller: open index.html)
3. Vips! 🎉
```

### Eller via GitHub
```bash
git clone https://github.com/DIN-BRUKERNAVN/Vinlotteri.git
cd Vinlotteri
# Åpne index.html i nettleseren
```

---

## 🐛 Feilsøking

**Problemet: Data forsvinner når jeg lukker nettleseren**
- Dette er normalt! localStorage er sessjonbasert
- Løsning: Eksporter til Excel regelmessig

**Problemet: Excel-import fungerer ikke**
- Sjekk at Excel-filen har riktig format
- Kolonnenavn må være: Navn, E-post, Antall lodd
- Eller: Bruk .xlsx format (ikke .xls)

**Problemet: Kan ikke åpne fra File:// (lokal)**
- Nettlesere blokkerer CORS for fil-protokollen
- Løsning: Bruk GitHub Pages eller lokal webserver
  ```bash
  # Python 3
  python -m http.server 8000
  # Så åpne http://localhost:8000/index.html
  ```

**Problemet: Kan ikke åpne fra GitHub Pages**
- Sjekk at Settings → Pages er aktivert
- URL: `https://brukernavn.github.io/Vinlotteri/`
- Wait 1-2 minutter etter første push

---

## 💡 Tips

### Bruk med hele gruppen
```
1. Del GitHub Pages link
2. Alle åpner samme URL
3. Hver PC har sin egen localStorage (uavhengig data)
4. Del resultater via eksportert Excel
```

### Backup-rutine
```
1. Hver dag: "Last ned historikk"
2. Lag mappe: Lotteri_Backups/
3. Gi navn: historikk_2025-01-15.xlsx
4. Data sikret! 💪
```

### Tilpass deltakere
```
Hver trekningssesjon:
1. Slett forrige deltakere ("Slett alle")
2. Importer ny Excel-fil
3. Eller legg til manuelt
4. Start trening
```

---

## 📊 Eksempel: Ledersamling

```
Scenario: 5 personer, 3 priser

1. Importer Excel med 5 deltakere
2. Skriv "3" (3 priser)
3. Klikk "Start trekningssesjon"
4. Trekk vinner 1 → Ole Petter 🎉
5. Trekk vinner 2 → Anna 🎉
6. Trekk vinner 3 → Kari 🎉
7. Klikk "Lagre vinnere"
8. Klikk "Last ned historikk"
9. Send Excel-fil til alle 📧
```

---

## 🎨 Anpass design

Vil du endre farger?

Åpne `index.html` og rediger disse linjene (toppen av `<style>`):

```css
--ffe-farge-fjell: #002776;      /* Primær blå */
--ffe-farge-vann: #005aa4;       /* Knapp blå */
--ffe-farge-skog: #00754e;       /* Grønn */
```

---

## 📄 Lisens

MIT License - Se LICENSE fil

---

## 🤝 Bidrag

Har du ideer? Lag en Pull Request!

---

## 📞 Support

**Spørsmål?**
1. Sjekk FAQ over
2. Åpne GitHub Issue
3. Sjekk browser console (F12) for feil

---

**Laget med ❤️ for SpareBank 1**

Gjør lotering gøy! 🎉
