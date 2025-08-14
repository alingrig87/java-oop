# 🧱 Proiectel — Chitanță card smoothie bar (numai variabile)

Obiectiv: Creează un program care tipărește o chitanță textuală pentru un card de fidelitate la un bar de smoothie, folosind DOAR variabile și operații de concatenare/aritmetică simplă (fără condiții, fără bucle, fără metode auxiliare).

De ce acest proiect:

- Te disciplinează să modelezi date simple cu variabile corecte (`String`, `int`, `double`) și să formatezi output-ul clar.

Cerințe:

1. Fișier/clasă `Proiectel_Variabile_Smoothie` cu `main`.
2. Declară variabilele exact:
   - `String numeClient` (ex.: "Alex Pop")
   - `String cardId` (ex.: "SM-2024-001")
   - `String produs1`, `double pret1`, `int cant1`
   - `String produs2`, `double pret2`, `int cant2`
   - `double valoarePunct = 0.5; // lei/punct`
3. Calcule:
   - `double subtotal = pret1 * cant1 + pret2 * cant2;`
   - `int puncteCastigate = (int) (subtotal / 10); // 1p la 10 lei`
   - `double valoarePuncte = puncteCastigate * valoarePunct;`
4. Afișează EXACT (exemplu de format; valorile pot varia):

```
🥤 SMOOTHIE BAR — CHITANȚĂ
Client: Alex Pop | Card: SM-2024-001
-----------------------------------
1) Mango Boost x2 @ 14.50 = 29.00
2) Berry Mix  x1 @ 16.00 = 16.00
-----------------------------------
Subtotal: 45.00 lei
Puncte: 4 (valoare: 2.00 lei)
Mulțumim și poftă bună!
```

5. Nu folosi condiții/bucle. Calculează și formatează simplu (poți folosi `printf` pentru 2 zecimale).
6. Commit:

- `git add Proiectel_Variabile_Smoothie.java`
- `git commit -m "feat: add proiectel variabile - chitanta smoothie bar"`

Pași recomandați:

1. Creează fișierul/clasa cu `main`.
2. Declară variabilele în ordinea din cerință, cu valori de test.
3. Calculează subtotalul, punctele și valoarea punctelor exact în variabile separate (nu face calcule direct în `println`).
4. Folosește `System.out.printf` pentru sume la 2 zecimale (mai lizibil și precis pentru chitanțe).
5. Afișează liniile EXACT ca în exemplu; verifică alinierea vizuală.

Verificări:

- Subtotalul să reflecte cantitate x preț pentru fiecare produs.
- Punctele sunt întregi (casting explicit la `int`).
- Formatul liniilor respectă spațiile dintre elemente.

Greșeli frecvente:

- Să uiți conversia la `int` pentru puncte — rezultă puncte cu zecimale.
- Să amesteci `+` pentru concatenare cu `+` pentru adunare; încadrează calculele între paranteze.
