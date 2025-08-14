# 🧱 Proiectel — Biblioteca de utilitare pentru carduri (metode)

Obiectiv: Scrie o clasă utilitară cu metode `static` pentru operații comune asupra cardurilor, apoi demonstrează-le în `main`.

De ce acest proiect:

- Consolidezi lucrul cu metode `static`: semnături corecte, valori returnate, formatări și compunerea rezultatelor.

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

Pași recomandați (detaliat):

1. Creează fișierul `Proiectel_Metode_Utils.java`.
2. Definește clasa publică omonimă și, în interior, metodele `static` în ordinea listată.
3. La `calculeazaBonus`, implementează exact regula (>=100 => 20; altfel 0). Nu folosi valori magice în altă parte.
4. La `convertToMoney`, întoarce `puncte * valPunct` ca `double` (nu formata text aici).
5. La `formateazaCard`, construiește și returnează textul într-un singur `String`.
6. La `printRaport`, apelează celelalte metode pentru a evita dublarea logicii și formatează valoarea cu 2 zecimale.
7. În `main`, apelează în ordinea cerută și verifică că output-ul corespunde EXACT.

Acceptance criteria:

- Semnăturile metodelor (nume, parametri, tip retur) sunt EXACT cele din cerință.
- `printRaport` folosește celelalte metode (nu recalculează bonus/valoare manual).
- Output-ul final are exact 2 linii și respectă formatul (spații, diacritice, 2 zecimale).

Greșeli frecvente și remedii:

- Formatarea sumei cu concatenare în loc de `printf` — preferă `System.out.printf("%.2f", valoare)` sau `String.format`.
- Schimbarea semnăturii (ex.: `calculeazaBonus(double)` în loc de `int`) — poate complica apelurile și duce la rezultate eronate.
- Amestecarea responsabilităților — păstrează calculele în metodele lor, nu în `main`.

Teste recomandate:

- `puncte=99` => bonus 0; `puncte=100` => bonus 20.
- `valPunct` diferit (ex.: 0.05 vs 0.3) pentru a verifica formatul la 2 zecimale.
