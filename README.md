# 🎰 SpareBank 1 Vinlotteri

En elegant og pålitelig lotterimaskin for trekning av vinnere med korrekt sannsynlighetsfordeling basert på antall lodd.

**✨ Designet med SpareBank 1 FFE design system**

---

## 📋 Innholdsfortegnelse

1. [Funksjoner](#-funksjoner)
2. [Rask start](#-rask-start)
3. [Deltakere](#-deltakere)
4. [Trekninger](#-trekninger)
5. [Historikk](#-historikk)
6. [Tekniske detaljer](#-tekniske-detaljer)

---

## ✨ Funksjoner

### 🎲 Trekninger
- **Slot Machine animasjon** med farger som spinner
- **Korrekt sannsynlighet** basert på antall lodd
- **Maks 2 seire per person** per trekningsesjon
- **Live sannsynlighets-display** som oppdateres etter hver trekning

### 👥 Deltakere
- Legg til navn, e-post og antall lodd
- Importer/eksporter fra Excel
- Vis sannsynlighet i % for hver deltaker
- Enkel sletting av deltakere

### 📊 Historikk
- Automatisk registrering av alle trekninger
- Eksporter til Excel-fil
- Importer gammel historikk
- Merge eller erstatt ved import
- Statistikk per person
- Slett all historikk med sikker confirmation

### 💾 Data
- Alt lagres lokalt i nettleseren (localStorage)
- Ingen servere, ingen loggføring
- Du kontrollerer all data

---

## 🚀 Rask start

### Online (GitHub Pages)
```
1. Åpne: https://brukernavn.github.io/Vinlotteri/
2. Appen laster automatisk
3. Start med "Legg til deltaker"
```

### Lokalt (din datamaskin)
```
1. Last ned index.html
2. Dobbeltklikk på filen
3. Appen åpnes i nettleseren
4. Alt fungerer offline! ✅
```

---

## 👥 Deltakere

### Legg til manuelt

**Steg:**
1. Gå til "Deltakere" fanen
2. Fyll inn:
   - **Navn** - Deltakerens navn
   - **E-post** - Valgfritt
   - **Antall lodd** - Hvor mange lodd de har
3. Klikk "Legg til"

**Eksempel:**
```
Navn: Frank Hansen
E-post: frank@example.com
Antall lodd: 90
```

### Importer fra Excel

**Forberedelse - lag Excel-fil:**

| Navn | E-post | Antall lodd |
|---|---|---|
| Frank Hansen | frank@example.com | 90 |
| Kari Dahl | kari@example.com | 10 |
| Ole Petter | ole@example.com | 50 |

**Import:**
1. Klikk "Importer fra fil"
2. Velg Excel-filen (.xlsx eller .xls)
3. Deltakerne legges til automatisk

**Kolonnenavnene må være nøyaktig:**
- `Navn`
- `E-post`
- `Antall lodd`

---

## 🎲 Trekninger

### Start ny trekningsesjon

**Steg:**
1. Gå til "Trekning" fanen
2. Fyll inn "Antall trekninger" - hvor mange vinnere du vil ha
3. Klikk "Start trekningsesjon"

**Eksempel:**
```
Deltakere: Frank (90 lodd), Kari (10 lodd)
Antall trekninger: 3
```

### Kjør trekning

**For hver trekning:**
1. Klikk "Trekk neste vinner"
2. Slot machine spinner 2 sekunder
3. Vinnernavn vises i maskinen
4. Vinner legges automatisk i lista

**Sannsynlighet:** Basert på antall lodd
```
Frank: 90/100 = 90% sjanse
Kari: 10/100 = 10% sjanse
```

### Regler

- **Maks 2 seire per person** per sesjon
- Etter 2. seier: 0% sjanse (utestengt)
- Resten av loddene fordeles på andre

**Eksempel:**
```
Trekning 1: Frank vinner (90%)
Trekning 2: Frank vinner igjen (89% - ett lodd mindre)
Trekning 3: Frank er utestengt (0%) - kun Kari kan vinne
```

### Lagre eller avbryt

**Når ferdig:**
- ✅ **Lagre vinnere** - Lagrer til historikk
- ❌ **Avbryt** - Sletter, ingen lagring
- 🔄 **Ny sesjon** - Starter ny trekning

---

## 📊 Historikk

### Vis historikk

**Fanen "Historikk"** viser alle tidligere trekninger:
- Dato og tid
- Posisjon (1., 2., osv)
- Vinnernavn
- E-post
- Antall lodd

### Eksporter til Excel

**Steg:**
1. Gå til "Historikk" fanen
2. Klikk "📥 Last ned historikk (Excel)"
3. Excel-fil lastes ned: `lotteri_historikk.xlsx`

**Innholdet:**
```
| Dato | Prisnummer | Vinner | E-post | Antall lodd |
|---|---|---|---|---|
| 17.06.2026 13:45 | 1 | Frank | frank@... | 90 |
```

### Importer historikk

**Fra gammel Excel-fil:**
1. Klikk "📤 Importer historikk (Excel)"
2. Velg Excel-filen
3. Velg handling:
   - **Merge** = Legg til nye trekninger
   - **Erstatt** = Slett gamle, bruk kun nye
4. Historikk gjenopprettes ✅

**Excel-format må ha:**
- `Dato` kolonne
- `Vinner` kolonne
- Andre kolonner: `Prisnummer`, `E-post`, `Antall lodd`

### Statistikk

**Fanen "Statistikk"** viser:
- Antall seiere per person
- Seiere i gjeldende sesjon
- Historiske tall

### Slett all historikk

**Steg:**
1. Klikk "🗑️ Slett all historikk"
2. Confirmation dialog dukker opp
3. Klikk OK for å slette
4. ⚠️ **DETTE KAN IKKE ANGRES!**

**Tips:** Eksporter til Excel først som sikkerhetskopi! 📥

---

## 💾 Data & Sikkerhet

### Hvor lagres data?

**Alt lagres lokalt i nettleseren:**
```
localStorage:
  - vinlotteri_participants (deltakere)
  - vinlotteri_history (historikk)
```

**Fordelene:**
- ✅ Ingen server - fullt privat
- ✅ Fungerer offline
- ✅ Ingen loggføring
- ✅ Du kontrollerer alt

### Sikkerhetskopi

**Anbefalt workflow:**
```
1. Gjør trekninger
2. Lagre sesjon
3. Eksporter historikk (Excel)
4. Lagre Excel-fil på datamaskinen
5. Kan nå slette alt fra appen hvis du vil
6. Importer senere hvis nødvendig
```

### Data som slettes

**"Slett all historikk" sletter KUN:**
- Trekningshistorikk

**BEVARES:**
- Deltakerlisten
- Data fra andre apper/nettsteder

---

## 🔧 Tekniske detaljer

### Krav
- Moderne nettleser (Chrome, Firefox, Safari, Edge)
- JavaScript aktivert
- Internett (første gang) - fungerer offline etterpå

### Biblioteker
- **SheetJS** - Excel import/export
- **FileSaver** - Fil-download
- **SpareBank 1 FFE Design System** - Styling

### Nettleser-kompatibilitet
- ✅ Chrome 90+
- ✅ Firefox 88+
- ✅ Safari 14+
- ✅ Edge 90+

### Filer
```
index.html          Hele appen (alt-i-en fil)
README.md          Denne dokumentasjonen
```

---

## ❓ Vanlige spørsmål

### Hva hvis jeg lukker nettleseren?
**Data bevares!** Alt lagres i localStorage.

### Kan jeg bruke appen offline?
**JA!** Etter første lasting fungerer den helt offline.

### Hvor mange deltakere kan jeg ha?
**Ubegrenset!** Avhenger av nettleserminne (typisk 1000+).

### Hvordan sikrer jeg data?
**Eksporter til Excel!** Gjør det før du sletter noe.

### Kan jeg dele appen med andre?
**JA!** Lag en GitHub Pages eller del HTML-filen.

### Hva hvis jeg gjør en feil?
**Importer historikk fra Excel-backup!** 📥

---

## 📞 Support

Hvis noe ikke fungerer:
1. Åpne Developer Console (F12)
2. Gå til "Console" tab
3. Se på feilmeldingene
4. Prøv å laste siden på nytt

---

## 📝 Versjon

**Vinlotteri v1.0**
- Slot machine animasjon
- Korrekt sannsynlighet
- Excel import/export
- Historikk-styring

---

## 🎨 Design

Designet med **SpareBank 1 FFE design system**:
- Farge: Navy (#002776), Blå (#005aa4)
- Typografi: Source Sans 3
- Komponenter: Buttons, Cards, Forms

---

Lykke til med trekningen! 🎉
