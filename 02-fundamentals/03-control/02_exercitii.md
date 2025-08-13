# 🧪 Structuri de Control — Exerciții simple (detaliate)

Instrucțiuni:

- Un fișier `.java` per exercițiu, o clasă publică cu `main`.
- Respectă exact formatele de output.
- Fă commit după ce rulezi corect.

---

## 11) Exercitiul11_StatusCard

Obiectiv: `if/else` simplu.

Variabile:

- `boolean activ = true;`
- `int zileRamase = 12;`

Reguli:

- Dacă `activ == true` și `zileRamase > 0` => "Activ".
- Altfel, "Expirat".

Output exact (cu valorile de mai sus):

```
📇 STATUS CARD
Activ: true, Zile ramase: 12
Rezultat: Activ
```

Commit: `feat: add exercitiul 11 - status card (if/else)`

---

## 12) Exercitiul12_NivelCard

Obiectiv: `if / else if / else` pe praguri.

Variabile:

- `int puncte = 740;`

Reguli:

- `< 100` => "Bronze"
- `100..499` => "Silver"
- `500..999` => "Gold"
- `>= 1000` => "Platinum"

Output:

```
🎖️ NIVEL CARD
Puncte: 740
Nivel: Gold
```

Commit: `feat: add exercitiul 12 - nivel card (if/elseif)`

---

## 13) Exercitiul13_TipCardSwitch

Obiectiv: `switch` pe `String`.

Variabile:

- `String tip = "hotel";`

Reguli (mesaj):

- `cinema` => "Beneficiu: reducere popcorn"
- `hotel` => "Beneficiu: late checkout"
- `retail` => "Beneficiu: voucher magazin"
- altfel => "Beneficiu: standard"

Output:

```
🎫 TIP CARD
hotel
Beneficiu: late checkout
```

Commit: `feat: add exercitiul 13 - tip card (switch)`

---

## 14) Exercitiul14_AcumularePuncte

Obiectiv: `for` și sumă incrementală.

Variabile:

- `int puncteZilnice = 12;`
- `int zile = 7;`

Calcule:

- Suma totală pe `zile` zile.

Output:

```
📈 ACUMULARE PUNCTE
Zile: 7, Puncte/zi: 12
Total: 84
```

Commit: `feat: add exercitiul 14 - acumulare puncte (for)`

---

## 15) Exercitiul15_CautareCard

Obiectiv: `while` + `break`.

Date:

- `boolean[] active = {false, false, true, false};`

Sarcină:

- Găsește indexul primului `true` și oprește imediat căutarea.

Output:

```
🔍 CAUTARE CARD
Primul activ la index: 2
```

Commit: `feat: add exercitiul 15 - cautare card (while)`
