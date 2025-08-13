# 🧪 Metode — Exerciții simple (detaliate)

Instrucțiuni:

- Un fișier `.java` per exercițiu, clasa publică omonimă, `main` minim pentru apeluri/demonstrații.
- Respectă exact formatul de output.

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

---

## 17) Exercitiul17_CalcPuncte

Obiectiv: metodă cu return `int`.

Cerințe:

- Scrie `static int calculeazaBonus(int puncte)` astfel:
  - dacă `puncte >= 100` => returnează `20`, altfel `0`.
- În `main`, tipărește: `"Bonus: " + calculeazaBonus(120)` => `Bonus: 20`.

Commit: `feat: add exercitiul 17 - metoda calculeazaBonus`

---

## 18) Exercitiul18_ValidareCard

Obiectiv: metodă booleană.

Cerințe:

- Scrie `static boolean esteValid(boolean activ, int zile)` => `true` dacă `activ` și `zile > 0`.
- În `main`, afișează EXACT: `"Valid: " + esteValid(true, 5)` => `Valid: true`.

Commit: `feat: add exercitiul 18 - metoda esteValid`

---

## 19) Exercitiul19_Conversie

Obiectiv: metodă cu parametri multipli și calcule `double`.

Cerințe:

- `static double convertToMoney(int puncte, double valPunct)` => `puncte * valPunct`.
- În `main`, formatează cu 2 zecimale: `System.out.printf("%.2f", convertToMoney(125, 0.05));` => `6.25`.

Commit: `feat: add exercitiul 19 - metoda convertToMoney`

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
