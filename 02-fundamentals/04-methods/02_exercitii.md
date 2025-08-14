# 🧪 Metode — Exerciții simple (detaliate)

Instrucțiuni:

- Un fișier `.java` per exercițiu, clasa publică omonimă, `main` minim pentru apeluri/demonstrații.
- Respectă exact formatul de output.

Checklist general:

- Numele metodelor și tipurile parametrilor/returnărilor să fie exact ca în cerință.
- Testează metodele cu 2-3 seturi de date (inclusiv limite) pentru a verifica logica.

---

## 16) Exercitiul16_PrintCard

Obiectiv: metodă `void` pentru afișare formatată.

Cerințe:

- Scrie metoda `static void printCard(String nume, int puncte)`.
- Afișează EXACT:

```
👤 Nume: <nume>
⭐ Puncte: <puncte>
```

- În `main`, apelează `printCard("Ana", 120)`.

Commit: `feat: add exercitiul 16 - metoda printCard`

De ce:

- Separi logica de afișare într-o funcție reutilizabilă; eviți duplicarea în `main`.

---

## 17) Exercitiul17_CalcPuncte

Obiectiv: metodă cu return `int`.

Cerințe:

- Scrie `static int calculeazaBonus(int puncte)` astfel:
  - dacă `puncte >= 100` => returnează `20`, altfel `0`.
- În `main`, tipărește: `"Bonus: " + calculeazaBonus(120)` => `Bonus: 20`.

Commit: `feat: add exercitiul 17 - metoda calculeazaBonus`

Observație:

- În `if/else`, întoarce direct valori (`return 20;` / `return 0;`) pentru simplitate.

---

## 18) Exercitiul18_ValidareCard

Obiectiv: metodă booleană.

Cerințe:

- Scrie `static boolean esteValid(boolean activ, int zile)` => `true` dacă `activ` și `zile > 0`.
- În `main`, afișează EXACT: `"Valid: " + esteValid(true, 5)` => `Valid: true`.

Commit: `feat: add exercitiul 18 - metoda esteValid`

Clarificare:

- Tipul returnat este `boolean`, deci metoda nu printează; doar decide `true/false`.

---

## 19) Exercitiul19_Conversie

Obiectiv: metodă cu parametri multipli și calcule `double`.

Cerințe:

- `static double convertToMoney(int puncte, double valPunct)` => `puncte * valPunct`.
- În `main`, formatează cu 2 zecimale: `System.out.printf("%.2f", convertToMoney(125, 0.05));` => `6.25`.

Commit: `feat: add exercitiul 19 - metoda convertToMoney`

Pitfall:

- Evită împărțirea întreg la întreg; aici multiplicăm `int` cu `double` și rezultatul e `double` (corect pentru bani).

---

## 20) Exercitiul20_Overload

Obiectiv: overloading pe `printCard`.

Cerințe:

- Variante:
  - `static void printCard(String nume, int puncte)`
  - `static void printCard(String nume, int puncte, double valPunct)` care afișează și valoarea în lei (2 zecimale)
- Output pentru apelurile din `main`:

```
Ana: 120p
Ana: 120p (6.00 lei)
```

Commit: `feat: add exercitiul 20 - overload printCard`

Explicație:

- Overloading permite același nume de metodă cu semnături diferite; alege varianta în funcție de parametri.
