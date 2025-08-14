# 🧪 Variabile — Exerciții simple (detaliate)

Instrucțiuni generale:

- Fiecare exercițiu = un fișier `.java` cu o singură clasă publică și `main`.
- Respectă numele variabilelor și formatul de output cerut.
- După ce rulezi cu succes, fă commit.

Cum validezi:

- Output-ul TREBUIE să fie exact, inclusiv spații/emoji.
- Verifică tipurile potrivite: întregi pentru cantități, `double` pentru prețuri.
- Rulează de 2 ori cu alte valori pentru a evita hardcoding-ul.

---

## 1) Exercitiul01_CardHarryPotter

Obiectiv: Lucrezi cu `String` și afișare.

Pași:

1. Creează fișierul `Exercitiul01_CardHarryPotter.java` cu clasa `Exercitiul01_CardHarryPotter` și metoda `public static void main(String[] args)`.
2. Declară exact variabilele:
   - `String numeStudent = "Harry Potter";`
   - `String casaHogwarts = "Gryffindor";`
   - `String anScolar = "Anul 7";`
3. Afișează EXACT (liniile și spațiile):

```
🏰 CARD STUDENT HOGWARTS 🏰
===========================
Student: Harry Potter
Casa: Gryffindor
An școlar: Anul 7
Status: Activ
```

4. Commit:

- `git add Exercitiul01_CardHarryPotter.java`
- `git commit -m "feat: add exercitiul 01 - card Hogwarts (String + print)"`

Explicație și scop:

- Exersezi declararea de variabile `String` și concatenarea în `System.out.println`.
- Vezi diferența dintre text literal și valori din variabile.

---

## 2) Exercitiul02_CardMarvel

Obiectiv: Folosești `int` pentru valori întregi.

Pași:

1. Fișier/clasă `Exercitiul02_CardMarvel`.
2. Declară:
   - `String erou = "Iron Man";`
   - `int nivelPutere = 85; // 0..100`
   - `int varsta = 48;`
3. Afișează EXACT:

```
🎬 CARD MARVEL
Erou: Iron Man
Nivel putere: 85/100
Vârsta: 48
```

4. Commit: `feat: add exercitiul 02 - card Marvel (int)`

Greșeli frecvente:

- Folosirea ghilimelelor la valori numerice (`"85"` în loc de `85`). Nu o face; `int` nu folosește ghilimele.

---

## 3) Exercitiul03_CardNetflix

Obiectiv: `double` pentru ore și cost.

Pași:

1. Fișier/clasă `Exercitiul03_CardNetflix`.
2. Declară:
   - `String profil = "Family";`
   - `double oreVizionate = 36.5;`
   - `double costPeOra = 0.45;`
3. Calculează: `double costTotal = oreVizionate * costPeOra;`
4. Afișează EXACT (poți folosi `System.out.printf("%.2f", costTotal)` pentru 2 zecimale):

```
📺 CARD NETFLIX
Profil: Family
Ore vizionate: 36.5
Cost total: 16.42 $/lună
```

5. Commit: `feat: add exercitiul 03 - card Netflix (double)`

Tips:

- Pentru 2 zecimale, `System.out.printf("%.2f", costTotal);` este preferabil concatenării.

---

## 4) Exercitiul04_CardHotel

Obiectiv: `boolean` pentru status.

Pași:

1. Fișier/clasă `Exercitiul04_CardHotel`.
2. Declară:
   - `String nume = "Maria";`
   - `boolean activ = false;`
   - `int noptiRamase = 0;`
3. Afișează EXACT:

```
🏨 CARD HOTEL
Nume: Maria
Status: Inactiv
Nopți rămase: 0
```

4. Commit: `feat: add exercitiul 04 - card hotel (boolean)`

Explicație:

- `boolean` poate fi doar `true` sau `false`. Nu există „yes/no”. Transformă manual în textul dorit la afișare.

---

## 5) Exercitiul05_CardGaming

Obiectiv: combină tipuri (`String`, `int`, `double`, `boolean`).

Pași:

1. Fișier/clasă `Exercitiul05_CardGaming`.
2. Declară:
   - `String gamer = "ShadowFox";`
   - `int nivel = 27;`
   - `double xp = 812.75;`
   - `boolean premium = true;`
3. Afișează EXACT:

```
🕹️ CARD GAMING
Gamer: ShadowFox
Nivel: 27
XP: 812.75
Premium: true
```

4. Commit: `feat: add exercitiul 05 - card gaming (mix tipuri)`

Pitfall:

- Amestecarea tipurilor în calcule poate duce la conversii implicite. Când ai nevoie de fracții, asigură-te că folosești `double` (nu doar `int`).
