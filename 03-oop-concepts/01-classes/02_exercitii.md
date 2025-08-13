# 🧪 Clase și Obiecte — Exerciții simple (detaliate)

Instrucțiuni:

- Un fișier `.java` per exercițiu, o clasă publică și `main` pentru demonstrație.
- Respectă exact numele câmpurilor, constructorilor și formatul de output.

---

## 21) Exercitiul21_ClasaCardHarry

Obiectiv: definește o clasă cu 3 câmpuri și creează 2 obiecte.

Cerințe:

- Clasă `CardHarry` cu câmpurile `String nume`, `String casa`, `int puncte` (toate `public` la acest exercițiu pentru simplitate).
- În `main`, creează:
  - `CardHarry c1 = new CardHarry();` apoi setează: `c1.nume = "Harry"; c1.casa = "Gryffindor"; c1.puncte = 150;`
  - `CardHarry c2 = new CardHarry();` cu valori proprii.
- Afișează EXACT:

```
Card1 -> Harry | Gryffindor | 150p
Card2 -> <nume> | <casa> | <puncte>p
```

Commit: `feat: add exercitiul 21 - clasa CardHarry (fields si obiecte)`

---

## 22) Exercitiul22_Constructor

Obiectiv: adaugă constructor pentru inițializare rapidă.

Cerințe:

- În `CardHarry`, adaugă constructor: `CardHarry(String nume, String casa, int puncte)` care setează câmpurile.
- În `main`, creează `CardHarry c = new CardHarry("Ron", "Gryffindor", 90);`
- Afișează EXACT: `Ron | Gryffindor | 90p`

Commit: `feat: add exercitiul 22 - constructor CardHarry`

---

## 23) Exercitiul23_MetodeOperatii

Obiectiv: adaugă metode care modifică starea.

Cerințe:

- În `CardHarry`, adaugă:
  - `void adaugaPuncte(int p)` => crește `puncte` cu `p`
  - `void scadePuncte(int p)` => scade `puncte` cu `p`
- În `main`, pornește de la `CardHarry("Hermione","Gryffindor",100)` și aplică: `adaugaPuncte(30)`, `scadePuncte(10)`.
- Afișează: `Hermione | Gryffindor | 120p`

Commit: `feat: add exercitiul 23 - metode operatii`

---

## 24) Exercitiul24_Afisare

Obiectiv: metodă de afișare formatată.

Cerințe:

- În `CardHarry`, adaugă `void afisare()` care printează EXACT:

```
👤 Nume: <nume>
🏰 Casa: <casa>
⭐ Puncte: <puncte>
```

- În `main`, apelează `afisare()` pe un obiect.

Commit: `feat: add exercitiul 24 - metoda afisare`

---

## 25) Exercitiul25_ColecțieObiecte

Obiectiv: lucrează cu un array de obiecte și o buclă simplă de afișare.

Cerințe:

- Creează un array `CardHarry[] arr = new CardHarry[3];` cu 3 instanțe inițializate prin constructor.
- Parcurge cu `for` și printează pentru fiecare: `<nume> - <puncte>p` (o linie per obiect).

Commit: `feat: add exercitiul 25 - colectie carduri (array + for)`
