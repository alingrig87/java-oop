# 🧱 Proiectel — Registru simplu de carduri (clase și obiecte)

Obiectiv: Creează o aplicație minimă care gestionează 3 carduri de fidelitate pentru o sală de cinema. Doar clase și obiecte (fără moștenire/encapsulare strictă încă).

De ce acest proiect:

- Consolidezi noțiunile introduse la „Clase și Obiecte”: modelare stare + comportament, constructor, metode, mai multe instanțe.

Rezultatul așteptat (comportamental):

- Programul creează 3 carduri, modifică punctele în mod diferit și afișează detaliile fiecăruia în format identic, lizibil.

Cerințe:

1. Clasă `CardCinema` cu câmpuri publice: `String numeClient`, `String filmPreferat`, `int puncte`.
2. Constructor: `CardCinema(String numeClient, String filmPreferat, int puncte)`.
3. Metode:
   - `void adauga(int p)` — crește `puncte` cu `p`
   - `void afisare()` — EXACT:

```
🎬 Client: <numeClient>
🎞️ Film: <filmPreferat>
⭐ Puncte: <puncte>
```

4. În `main` (clasa `Proiectel_Clase_RegistruCinema`): creează 3 carduri, adaugă puncte diferit fiecăruia, apoi apelează `afisare()` pentru toate.
5. Commit:

- `git add Proiectel_Clase_RegistruCinema.java`
- `git commit -m "feat: add proiectel clase - registru carduri cinema"`

Pași recomandați (foarte detaliat):

1. Creează fișierul `Proiectel_Clase_RegistruCinema.java`.
2. În fișier, definește clasa publică `Proiectel_Clase_RegistruCinema` cu `public static void main(String[] args)`.
3. În același fișier (deasupra sau sub `main`), definește clasa `CardCinema` conform cerințelor.
4. În `main`, creează 3 obiecte cu constructorul (ex.: Ana/Star Wars/100, Radu/Inception/80, Mara/Titanic/120).
5. Apelează `adauga(...)` cu valori diferite (ex.: 20, 5, 15) pentru a simula utilizarea.
6. Apelează `afisare()` pentru fiecare obiect, pe linii separate, în ordinea creării.

Acceptance criteria (verificare):

- Câmpurile și semnăturile constructorului/metodelor corespund EXACT.
- Output-ul `afisare()` respectă formatul (emoji, spații, diacritice dacă sunt).
- Nu există cod duplicat pentru afișare (ai o singură metodă `afisare()` care se ocupă de format).

Greșeli frecvente și remedii:

- „Hardcodarea” punctelor noi direct în `afisare()` — mută logica în `adauga(int p)`.
- Instanțiere fără `new` (ex.: doar declarare) — rezultă `NullPointerException` la apelul metodei.
- Amestec de formate la afișare — păstrează un format unic, în metoda clasei.
