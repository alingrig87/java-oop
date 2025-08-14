# 🧪 Încapsulare — Exerciții simple (ff detaliate)

Instrucțiuni generale:

- Un fișier `.java` per exercițiu, cu o singură clasă publică și `main` pentru demonstrație (dacă nu se specifică altfel).
- Toate câmpurile din clase trebuie să fie `private` (dacă nu se specifică altfel). Expune starea prin getteri/setteri/metode dedicate.
- Aplică aceleași reguli de validare în constructor și în setteri (nu rupe invarianta clasei).
- Respectă formatul de output EXACT. Testează de 2 ori: cu date „normale” și cu date-limită.
- După ce rulezi corect, fă commit cu mesajul indicat.

---

## 26) Exercitiul26_GetSet_Baza

Obiectiv: Încapsulează starea unui card de cinema cu câmpuri `private` și oferă un API minim prin getteri/setteri.

Ce înveți și de ce:

- De ce `private`: împiedică accesul direct la câmpuri și permite controlul asupra modificărilor.
- De ce get/set: creezi un punct unic unde poți valida/normaliza date acum sau în viitor.

Pași detaliați:

1. Creează fișierul `Exercitiul26_GetSet_Baza.java`.
2. Scrie clasa `CardCinemaSecure` cu câmpuri `private String numeClient; private int puncte;`.
3. Adaugă getteri/setteri simpli (fără validări încă): `getNumeClient()`, `setNumeClient(String)`, `getPuncte()`, `setPuncte(int)`.
4. În `main`, creează un obiect, setează valori și afișează: `<nume> | <puncte>p`.

Validare (checklist):

- Câmpurile sunt `private`.
- Nu există acces direct tip `obj.puncte = 10` în afara clasei; doar prin setteri.
- Output-ul este exact, fără spații/litere lipsă.

Greșeli frecvente și cum le eviți:

- Uitarea `private` pe câmpuri —> IDE-ul nu previne; verifică manual.
- Nume de metode incorecte (ex.: `getpuncte`) —> respectă camelCase: `getPuncte`.

Commit: `feat: add exercitiul 26 - incapsulare baza (get/set)`

---

## 27) Exercitiul27_Validari_Normalizari

Obiectiv: Adaugă validări/normalizări în constructor și setteri pentru a menține invarianta.

Reguli de business (invariantă):

- `numeClient` nu trebuie să fie `null` sau gol: se normalizează la `trim()`; dacă e gol => `"Anonim"`.
- `puncte` trebuie să fie în intervalul `[0, 100000]` (plafonare).

Pași:

1. Pornește de la clasa din ex. 26; redenumește fișierul `Exercitiul27_Validari_Normalizari.java` sau copiază clasa.
2. Adaugă constructor `CardCinemaSecure(String numeClient, int puncte)` care apelează setteri (nu seta direct câmpurile) pentru a reutiliza regulile.
3. În `setNumeClient`, aplică: `null` -> `""`, apoi `trim()`, apoi `empty ? "Anonim" : valoarea`.
4. În `setPuncte`, aplică clamp: `<0` -> `0`, `>100000` -> `100000`.
5. În `main`, testează 2 cazuri: (" ", -50) și ("Ana ", 120000). Afișează rezultatele.

De ce așa:

- Constructorul folosește setteri pentru a nu duplica logica de validare — un singur loc de adevăr.

Validare:

- Pentru (" ", -50) -> nume devine `Anonim`, puncte `0`.
- Pentru ("Ana ", 120000) -> nume `Ana`, puncte `100000`.

Commit: `feat: add exercitiul 27 - validari si normalizari (constructor + setteri)`

---

## 28) Exercitiul28_ProprietatiDerivate

Obiectiv: Expune comportamente derivate din stare fără a expune starea în sine.

Sarcină:

- Adaugă metoda `boolean isVip()` care revine `true` dacă `puncte >= 1000`.
- Adaugă metoda `String statut()` care revine EXACT: `"VIP"` dacă `isVip()`, altfel `"Standard"`.
- Adaugă metodă `void afisare()` cu 2 linii:

```
👤 Nume: <nume>
⭐ Puncte: <puncte> | Statut: <VIP/Standard>
```

Pași:

1. Continuă pe clasa `CardCinemaSecure` cu validările de la ex. 27.
2. Implementează `isVip()` și `statut()` folosind `getPuncte()` (nu citi câmpul direct din exterior).
3. În `main`, demonstrează cu două obiecte: ("Ana", 980) și ("Radu", 1200).

Greșeli frecvente:

- Logică duplicată în `statut()` în loc să folosească `isVip()`. Păstrează un singur loc pentru condiție.

Commit: `feat: add exercitiul 28 - proprietati derivate (isVip/statut)`

---

## 29) Exercitiul29_ClasaImutabila

Obiectiv: Modelează un card imutabil (fără setteri, câmpuri `final`).

Cerințe:

- Clasa `CardNetflixImmutable` cu `private final String profil; private final int minuteVizionate;`.
- Constructor validează/normalizează: `profil` ca în ex. 27; `minuteVizionate` >= 0.
- Fără setteri. Expune doar getteri.
- Pentru „modificări”, expune metode de tip `cuX`: `CardNetflixImmutable cuMinuteVizionate(int m)` care întoarce un nou obiect.

Pași:

1. Creează fișier `Exercitiul29_ClasaImutabila.java`.
2. Implementează clasa și un `main` care arată că obiectul original rămâne neschimbat după apelul `cuMinuteVizionate`.

De ce imutabilitate:

- Elimină clase de erori (stări intermediare invalide), ușurează reasoningul, e thread-safe by default.

Commit: `feat: add exercitiul 29 - clasa imutabila (cuX)`

---

## 30) Exercitiul30_DefensiveCopy

Obiectiv: Protejează câmpurile mutabile (liste) prin copii defensive la intrare și ieșire.

Cerințe:

- Clasa `CardCafeneaPerks` cu câmpuri `private final String nume; private final java.util.List<String> beneficii;`.
- Constructorul face copie la intrare: dacă lista e `null` -> listă goală; altfel `new ArrayList<>(lista)`.
- Getterul `getBeneficii()` întoarce o copie imuabilă: `Collections.unmodifiableList(new ArrayList<>(beneficii))`.
- Demonstrează în `main` că modificările asupra listei originale sau asupra celei returnate nu afectează starea internă.

Pitfall de evitat:

- A returna lista internă direct -> permite modificări externe și rupe încapsularea.

Commit: `feat: add exercitiul 30 - defensive copy pentru liste`
