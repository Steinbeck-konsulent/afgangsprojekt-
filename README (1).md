# 📝 Diplomopgave-hjælper

Et gratis, browser-baseret skriveværktøj til studerende på **Diplom i Ledelse** (og lignende diplomuddannelser).

Bygget af en studerende, til studerende — fordi det er svært at holde overblik over en 50-siders akademisk opgave.

---

## ✨ Hvad kan det?

- **Venstre side:** Dispositionen nedbrudt afsnit for afsnit (med sideangivelser fra studieordningen)
- **Midten:** Dit eget skriveområde med ordtæller og normalsider
- **Højre side:** Teori- og husketips der skifter per afsnit (kan skjules)
- **Afkrydsningsliste:** "Husk at få med"-punkter for hvert afsnit — sæt kryds når du har husket det
- **Fremgangsbjælke:** Vis hvor langt du er (op til 50 normalsider)
- **Auto-gem:** Alt gemmes automatisk i din browsers localStorage — ingen konto, ingen server

---

## ⚠️ Vigtige forbehold

> **Dette værktøj er udarbejdet med udgangspunkt i Diplom i Ledelse (UCL, studieordning 2024).**
>
> Du er selv ansvarlig for at sikre at krav til omfang, struktur og bedømmelse svarer til din uddannelsesinstitution og er opdaterede. Tjek altid din gældende studieordning.

Krav der kan variere fra institution til institution:
- Antal normalsider (her: 40–50 for individuel)
- Krav til litteraturliste og referencestyle (her: APA)
- Regler for brug af AI i opgaver
- Strukturen på det mundtlige forsvar

---

## 🚀 Sådan kommer du i gang

**Ingen installation nødvendig.** Bare åbn filen i din browser:

1. Download eller klon dette repository
2. Åbn `index.html` i din browser (Chrome, Firefox, Safari eller Edge)
3. Klik på et afsnit i menuen til venstre
4. Begynd at skrive

Dine noter gemmes automatisk i din browser.

---

## 🔧 Tilpas til dit eget projekt

Værktøjet er designet til at tilpasses. I `index.html` finder du to steder du kan redigere:

### 1. Tilpas afsnittene (`SECTIONS`)
Hvert afsnit har:
- `checks`: hvad der skal huskes i dette afsnit
- `hints`: tips og råd i højre side
- `redThread`: den røde tråd (vises som placeholder i skrivefeltet)
- `gap`: advarsel hvis noget mangler
- `theories`: hvilke teorier der vises (se næste punkt)

### 2. Tilføj dine egne teorier (`THEORIES`)
```javascript
const THEORIES = {
  minteori: {
    name: "Forfatter (årstal)",
    color: "theory",        // "theory", "method" eller "red-thread"
    subtitle: "Kort beskrivelse",
    use: "Brug til: ...",
    points: ["Punkt 1", "Punkt 2"]
  }
};
```
Tilknyt derefter teorien til et afsnit:
```javascript
theories: ["minteori"]
```

---

## 💾 Om datalagring

Dine noter gemmes **udelukkende i din egen browsers localStorage**. De forlader aldrig din computer og deles ikke med nogen. Rydder du din browsers data, mister du dine noter — så kopier gerne dine udkast ind i dit Word-dokument løbende.

---

## 📄 Licens

MIT — brug det frit, del det gerne og tilpas det til din uddannelse.

---

## 💡 Idéer til videreudvikling

- [ ] Eksport af noter til .txt eller .docx
- [ ] Understøttelse af gruppeaflevering (flere forfattere)
- [ ] Valgfri studieordning (UCL, VIA, AU...)
- [ ] Mørkt tema
- [ ] Mobilvenligt layout

Har du idéer eller finder du en fejl? Åbn gerne et issue eller send en pull request.
