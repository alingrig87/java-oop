# 🧪 Moștenire — Exerciții simple (detaliate)

Instrucțiuni:

- Fiecare exercițiu poate fi în fișier separat; include un `main` de demonstrație.
- Respectă numele claselor/metodelor și output-urile.

Checklist general:

- Folosește `extends` corect și apelează `super(...)` când este nevoie (constructori).
- Acces la câmpuri: `protected` pentru uz în subclase, `private` pentru încapsulare strictă.
- Adaugă `@Override` pentru metode suprascrise – te ajută să detectezi greșeli de semnătură.

---

## 31) Exercitiul31_BazaCard

Obiectiv: creează clasa de bază pentru ierarhie.

Cerințe:

- Clasă `CardFidelitate` cu câmp `protected int puncte;`
- Metode: `public void adauga(int p)`, `public void scade(int p)`.
- În `main`, demonstrează: pornește de la 0, adaugă 50, scade 20; afișează EXACT:

```
Puncte: 30
```

Commit: `feat: add exercitiul 31 - baza CardFidelitate`

De ce:

- Creezi un punct comun pentru comportamente partajate (adauga/scade); subclasele moștenesc această logică.

---

## 32) Exercitiul32_DerivatCinema

Obiectiv: subclasă cu câmp specific.

Cerințe:

- `class CardCinema extends CardFidelitate` cu câmp `String cinema;`
- Constructor: `CardCinema(String cinema)`; metodă `void afisare()` care printează EXACT:

```
🎬 Cinema: <cinema> | Puncte: <puncte>
```

- În `main`, `adauga(120)` și `afisare()`.

Commit: `feat: add exercitiul 32 - CardCinema derivat`

Observație:

- Câmpul `puncte` este accesibil direct în subclasă fiind `protected`; alternativ poți oferi getter/setter în bază.

---

## 33) Exercitiul33_OverrideAfisare

Obiectiv: `@Override` pentru comportament specific copilului.

Cerințe:

- În `CardFidelitate`, adaugă `public String descriere()` => `"card generic"`.
- În `CardCinema`, suprascrie `public String descriere()` => `"card cinema: " + cinema`.
- În `main`, afișează EXACT:

```
card generic
card cinema: <cinema>
```

Commit: `feat: add exercitiul 33 - override afisare/descriere`

Explicație:

- Suprascrierea permite fiecărei subclase să aibă comportament specific păstrând aceeași interfață publică.

---

## 34) Exercitiul34_SuperConstructor

Obiectiv: constructor copil care apelează `super`.

Cerințe:

- În `CardFidelitate`, adaugă constructor `CardFidelitate(int puncte)`.
- În `CardCinema`, adaugă constructor `CardCinema(String cinema, int puncte)` care apelează `super(puncte)`.
- În `main`, creează `new CardCinema("IMAX", 200)` și printează `Puncte: 200`.

Commit: `feat: add exercitiul 34 - super constructor`

Pitfall:

- Dacă baza nu are constructor fără argumente, e obligatoriu să chemi `super(puncte)` în primul rând din constructorul copilului.

---

## 35) Exercitiul35_IerarhiePlina

Obiectiv: adaugă încă 2 subtipuri și afișează-le.

Cerințe:

- Creează `CardHotel extends CardFidelitate` (câmp `String hotel`), `CardRetail extends CardFidelitate` (câmp `String magazin`).
- Fiecare cu `afisare()` în format:

```
🏨 Hotel: <hotel> | Puncte: <puncte>
🛍️ Magazin: <magazin> | Puncte: <puncte>
```

- În `main`, creează câte un obiect din fiecare, setează puncte și afișează toate.

Commit: `feat: add exercitiul 35 - ierarhie carduri (cinema/hotel/retail)`

Tips:

- Ține metodele comune în bază. Specificul (hotel/cinema/retail) doar în subclase.
