# 🧪 Clase și Obiecte — Exerciții simple (detaliate)

Instrucțiuni:

- Un fișier `.java` per exercițiu, o clasă publică și `main` pentru demonstrație.
- Respectă exact numele câmpurilor, constructorilor și formatul de output.

Cum validezi soluția (general):

- Rularea trebuie să producă EXACT textele cerute (spații/emoji incluse).
- Folosește nume de variabile/câmpuri/metode identice cu cerința.
- Pentru fiecare exercițiu, testează și cu alte valori pentru a te asigura că logica nu e „hard-codată”.

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

De ce acest exercițiu:

- Înțelegi diferența dintre tipuri primitive și tipuri de referință (obiecte) și vezi cum se instanțiază cu `new`.

Greșeli frecvente:

- A uita să folosești `new` la creare -> variabila rămâne `null` și apare `NullPointerException` la acces.
- A confunda numele câmpurilor (ex.: `house` în loc de `casa`). Respectă exact cerința.

---

## 22) Exercitiul22_Constructor

Obiectiv: adaugă constructor pentru inițializare rapidă.

Cerințe:

- În `CardHarry`, adaugă constructor: `CardHarry(String nume, String casa, int puncte)` care setează câmpurile.
- În `main`, creează `CardHarry c = new CardHarry("Ron", "Gryffindor", 90);`
- Afișează EXACT: `Ron | Gryffindor | 90p`

Commit: `feat: add exercitiul 22 - constructor CardHarry`

Explicații:

- Constructorul îți permite să creezi obiecte într-o singură linie, garantând că toate câmpurile sunt setate de la început.
- Dacă adaugi un constructor cu parametri, constructorul fără argumente implicit NU mai este generat.

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

Capcane:

- Nu seta `puncte` direct în `main` pentru a simula operațiile; logica de modificare trebuie să fie în metodele clasei.
- Evită valori magice: transmite parametrul `p` din `main`, nu scrie `puncte += 20;` direct în metodă.

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

Tips & Tricks:

- Poți folosi `System.out.println("👤 Nume: " + nume);` etc. pentru lizibilitate.
- Dacă vrei reutilizare, extrage formatarea într-o metodă `toString()` și apelează `System.out.println(toString());` în `afisare()`.

---

## 25) Exercitiul25_ColecțieObiecte

Obiectiv: lucrează cu un array de obiecte și o buclă simplă de afișare.

Cerințe:

- Creează un array `CardHarry[] arr = new CardHarry[3];` cu 3 instanțe inițializate prin constructor.
- Parcurge cu `for` și printează pentru fiecare: `<nume> - <puncte>p` (o linie per obiect).

Commit: `feat: add exercitiul 25 - colectie carduri (array + for)`

De ce e util:

- Vezi cum se folosesc colecțiile de obiecte și cum se accesează câmpurile fiecărei instanțe într-o buclă.
- Atenție la `NullPointerException`: asigură-te că fiecare element din array e instanțiat prin constructor înainte de a-l folosi.
