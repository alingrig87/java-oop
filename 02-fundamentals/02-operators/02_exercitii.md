# 🧪 Operatori — Exerciții simple (detaliate)

Instrucțiuni generale:

- Un fișier `.java` per exercițiu, cu clasa publică omonimă și `main`.
- Respectă exact numele variabilelor și formatul de output.
- Fă commit după ce rulezi corect.

Checklist general:

- Folosește tipurile potrivite pentru fiecare operație (ex.: `double` când e nevoie de zecimale).
- Testează cu date-limită (puncte 99/100/101) pentru a valida condițiile.

---

## 6) Exercitiul06_CalculPuncteCafea

Obiectiv: aritmetică și `+=`.

Variabile:

- `String numeClient = "Ana";`
- `int puncteInitiale = 12;`
- `int puncteAdaugateAstazi = 5;`
- `double valoarePunct = 0.3;`

Calcule:

- `int puncteTotale = puncteInitiale;`
- `puncteTotale += puncteAdaugateAstazi;`
- `double valoare = puncteTotale * valoarePunct;`

Output exact:

```
👤 Client: Ana
⭐ Puncte inițiale: 12
➕ Puncte adăugate azi: 5
✅ Puncte totale: 17
💰 Valoare totală: 5.1 lei
```

Commit: `feat: add exercitiul 06 - calcul puncte cafenea (aritmetici si +=)`

Explicația operațiilor:

- `+=` actualizează variabila la fața locului; evită duplicarea variabilelor temporare.

---

## 7) Exercitiul07_ComparareCarduri

Obiectiv: comparații `>` și `==`.

Variabile:

- `String cardA = "Card Marvel";`
- `String cardB = "Card Netflix";`
- `int puncteA = 120;`
- `int puncteB = 150;`

Calcule: `boolean aAreMaiMult = puncteA > puncteB;`, `boolean egale = puncteA == puncteB;`

Output exact:

```
🔸 Card A: Card Marvel (120p)
🔹 Card B: Card Netflix (150p)
A are mai mult? false
Au puncte egale? false
Card cu mai multe puncte: Card Netflix
```

Commit: `feat: add exercitiul 07 - comparare carduri (>, ==)`

Pitfall:

- Nu compara `String` cu `==` pentru egalitate de conținut; aici comparăm doar int-urile. Pentru `String`, folosește `equals`.

---

## 8) Exercitiul08_ValidariCard

Obiectiv: logici `&&`, `>=`, short-circuit.

Variabile:

- `boolean cardActiv = true;`
- `int puncte = 95;`
- `int pragBonus = 100;`
- `boolean areEmailConfirmat = false;`

Calcule: `boolean eligibil = cardActiv && areEmailConfirmat && (puncte >= pragBonus);`

Output exact:

```
Activ: true, Email confirmat: false, Puncte: 95/100
🎁 Bonus eligibil? false
```

Commit: `feat: add exercitiul 08 - validari card (&& si >=)`

De ce short-circuit:

- Dacă `cardActiv` este `false`, expresia se oprește și nu evaluează `puncte >= pragBonus`, ceea ce poate evita calcule inutile.

---

## 9) Exercitiul09_UpgradeNivel

Obiectiv: `++`, `+=`, `-=`.

Variabile:

- `String nume = "GamerX";`
- `int nivel = 4;`
- `int xp = 890;`
- `int pragNivel = 900;`
- `int xpZilnic = 75;`

Reguli: dacă `xp >= pragNivel` => `nivel++` și `xp -= pragNivel`; apoi `xp += xpZilnic`.

Output (cu datele date):

```
🎮 Jucator: GamerX
Nivel initial: 4, XP initial: 890
Dupa procesare -> Nivel: 4, XP: 965
```

Commit: `feat: add exercitiul 09 - upgrade nivel (++/--, atribuire compusa)`

Verifică:

- Pentru datele din cerință NU se atinge pragul și `nivel` rămâne 4; ajustează datele și testează și cazul în care se face upgrade.

---

## 10) Exercitiul10_BonusCombinat

Obiectiv: mix de operatori + ternar.

Variabile:

- `String tipCard = "cinema";`
- `int puncte = 320;`
- `boolean activ = true;`
- `int pragBonus = 300;`

Calcule:

- `int bonusBaza = (puncte >= pragBonus) ? 50 : 0;`
- `int bonusTip = ("cinema".equals(tipCard) ? 20 : ("hotel".equals(tipCard) ? 30 : 10));`
- `int bonusFinal = (activ && puncte >= pragBonus) ? (bonusBaza + bonusTip) : 0;`

Output:

```
Tip: cinema, Activ: true, Puncte: 320
Bonus baza: 50, Bonus tip: 20
🎁 Bonus final: 70
```

Commit: `feat: add exercitiul 10 - bonus combinat (mix + ternar)`

Clarificare:

- Folosește `"cinema".equals(tipCard)` pentru a evita `NullPointerException` dacă `tipCard` ar fi `null`.
