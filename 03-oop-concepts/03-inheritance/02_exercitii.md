# 🧪 Moștenire — Exerciții simple (detaliate)

Instrucțiuni:

- Fiecare exercițiu poate fi în fișier separat; include un `main` de demonstrație.
- Respectă numele claselor/metodelor și output-urile.

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

---

## 34) Exercitiul34_SuperConstructor

Obiectiv: constructor copil care apelează `super`.

Cerințe:

- În `CardFidelitate`, adaugă constructor `CardFidelitate(int puncte)`.
- În `CardCinema`, adaugă constructor `CardCinema(String cinema, int puncte)` care apelează `super(puncte)`.
- În `main`, creează `new CardCinema("IMAX", 200)` și printează `Puncte: 200`.

Commit: `feat: add exercitiul 34 - super constructor`

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
