# 🧱 Proiectel — Biblioteca de utilitare pentru carduri (metode)

Obiectiv: Scrie o clasă utilitară cu metode `static` pentru operații comune asupra cardurilor, apoi demonstrează-le în `main`.

Cerințe:

1. Fișier/clasă `Proiectel_Metode_Utils`.
2. Metode `static` cerute:
   - `int calculeazaBonus(int puncte)` — ca la Ex. 17 (>=100 => 20, altfel 0)
   - `double convertToMoney(int puncte, double valPunct)` — conversie simplă
   - `String formateazaCard(String nume, int puncte)` — returnează `"Nume: <nume> | Puncte: <puncte>"`
   - `void printRaport(String nume, int puncte, double valPunct)` — printează 2 linii:

```
Nume: <nume> | Puncte: <puncte>
Valoare: <suma_lei_cu_2_zecimale> lei | Bonus: <bonus>
```

3. În `main`:
   - Apelează metodele pentru `("Ana", 120, 0.05)` și afișează EXACT:

```
Nume: Ana | Puncte: 120
Valoare: 6.00 lei | Bonus: 20
```

4. Commit:

- `git add Proiectel_Metode_Utils.java`
- `git commit -m "feat: add proiectel metode - utils carduri"`
