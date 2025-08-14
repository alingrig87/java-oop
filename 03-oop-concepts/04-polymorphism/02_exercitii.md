# 🧪 Polimorfism — Exerciții simple (detaliate)

Instrucțiuni:

- Fiecare exercițiu include un `main` de demonstrație.
- Respectă numele claselor/metodelor și output-urile cerute.

Checklist general:

- Polimorfismul se vede când folosești tipul părinte (clasă abstractă/interfață) pentru variabile/colecții.
- `@Override` pe metodele suprascrise în subclase îți validează semnătura.
- Pentru interfețe, clasele trebuie să implementeze TOATE metodele declarate.

---

## 36) Exercitiul36_ClasaAbstracta

Obiectiv: creează o bază abstractă pentru carduri.

Cerințe:

- `abstract class Card { abstract String afisare(); }`
- Subclasă `CardCinema` care implementează `afisare()` și întoarce EXACT: `"Card Cinema"`.
- În `main`, `Card c = new CardCinema(); System.out.println(c.afisare());`
- Output:

```
Card Cinema
```

Commit: `feat: add exercitiul 36 - clasa abstracta Card`

De ce abstract:

- Clasa de bază definește „ce”, iar subclasele definesc „cum”. Nu poți instanția clasa abstractă direct.

---

## 37) Exercitiul37_PolimorfismSimplu

Obiectiv: liste cu tip părinte și instanțe mixte.

Cerințe:

- Adaugă `CardHotel` care întoarce `"Card Hotel"` la `afisare()`.
- În `main`, creează `Card[] arr = { new CardCinema(), new CardHotel() };` și parcurge cu `for`, tipărind `afisare()` pentru fiecare.
- Output (pe 2 linii):

```
Card Cinema
Card Hotel
```

Commit: `feat: add exercitiul 37 - polimorfism simplu (array baza)`

Observație:

- Iterezi peste `Card[]` și se apelează implementarea corectă a lui `afisare()` la runtime (dispatch dinamic).

---

## 38) Exercitiul38_InterfaceRecompensa

Obiectiv: interfață implementată în 2 tipuri diferite.

Cerințe:

- `interface Recompensabil { int calculeazaBonus(int puncte); }`
- Implementări: `BonusStandard`, `BonusVip` (ca în teorie, sau echivalent).
- În `main`, pentru `puncte = 120`, afișează EXACT:

```
Standard: 20
VIP: 24
```

Commit: `feat: add exercitiul 38 - interfata Recompensabil (2 implementari)`

Tips:

- Interfața definește doar contractul; logica efectivă e în clasele care „implements”.

---

## 39) Exercitiul39_CastingSigur

Obiectiv: `instanceof` + downcasting.

Cerințe:

- Pornește de la `Card c = new CardCinema();`
- Verifică `instanceof CardCinema` și după cast apelează o metodă specifică `playTrailer()` care printează EXACT: `"Trailer..."`.
- Output:

```
Trailer...
```

Commit: `feat: add exercitiul 39 - instanceof + downcast`

Pitfall:

- Downcasting fără `instanceof` poate arunca `ClassCastException`. Verifică înainte.

---

## 40) Exercitiul40_DispatchDinamic

Obiectiv: demonstrează metoda corectă la runtime.

Cerințe:

- Adaugă `CardRetail` care întoarce `"Card Retail"` la `afisare()`.
- Creează `Card[] arr = { new CardCinema(), new CardHotel(), new CardRetail() };` și printează `afisare()`.
- Output (3 linii, în ordine):

```
Card Cinema
Card Hotel
Card Retail
```

Commit: `feat: add exercitiul 40 - dispatch dinamic (override)`

Clarificare:

- În array-ul de tip părinte, apelul `afisare()` execută varianta din clasa concretă a fiecărui element.
