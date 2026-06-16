# ⚡ Rask Start (30 sekunder)

## 1. Kjør lokalt
```
1. Last ned index.html
2. Dobbeltklikk
3. Ferdig! 🎉
```

## 2. Eller GitHub Pages

### Setup GitHub
```bash
git init
git add .
git commit -m "Init: SpareBank 1 Lottery"
git remote add origin https://github.com/DIN-BRUKERNAVN/Vinlotteri.git
git push -u origin main
```

### Aktiver Pages
1. Settings → Pages
2. Source: main → /root
3. **URL:** https://DIN-BRUKERNAVN.github.io/Vinlotteri/

---

## 3. Første bruk

```
1. Legg til deltakere
   ├─ Manuelt: Navn + e-post + antall lodd
   └─ Eller: Importer example_deltakere.xlsx

2. Skriv antall priser (f.eks. "3")

3. Klikk "Start trekningssesjon"

4. Klikk "Trekk neste vinner" × 3
   └─ Hjulet spinner → vinner vises

5. Klikk "💾 Lagre vinnere"
   └─ Lagret i historikk!

6. Klikk "Last ned historikk"
   └─ Excel-fil lastes ned
```

---

## Eksempel Excel-fil

Filen `example_deltakere.xlsx` viser riktig format:
- Kolonne A: Navn
- Kolonne B: E-post
- Kolonne C: Antall lodd

---

## Datalagring

✅ Alt lagres lokalt i nettleseren (localStorage)
✅ Ingen server nødvendig
✅ Sikkerhetskopi: Eksporter til Excel regelmessig

---

## Lykke til! 🎰
