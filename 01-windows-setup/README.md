# 🛠️ Setup Mediu Dezvoltare Windows

**Ghid Complet pentru Început în Java pe Windows**

Acest ghid te va ghida prin fiecare pas necesar pentru a configura mediul de dezvoltare Java pe Windows și pentru a crea primul exercițiu cu tema cardurilor de fidelitate.

## 📋 Lista Completă Setup

- [ ] Creează Cont Oracle
- [ ] Descarcă și Instalează Oracle JDK 21
- [ ] Configurează Variabilele de Mediu
- [ ] Creează Cont GitHub
- [ ] Instalează și Configurează Git
- [ ] Instalează IntelliJ IDEA Community Edition
- [ ] Configurează IntelliJ IDEA
- [ ] Primul Exercițiu Java
- [ ] Primul Commit Git

## 🌟 Pasul 1: Creează Cont Oracle

### De ce avem nevoie de un cont Oracle?

**Oracle Corporation** dezvoltă și menține Java. Pentru a descărca Oracle JDK (versiunea oficială și recomandată), ai nevoie de un cont gratuit Oracle.

### Crearea Contului Oracle

1. **Navighează la site-ul Oracle**:

   - Deschide browser-ul web
   - Mergi la [https://www.oracle.com](https://www.oracle.com)
   - Click pe "View Accounts" în colțul din dreapta sus
   - Selectează "Create an Account"

2. **Completează informațiile**:

   ```
   Email Address: email-ul-tau@exemplu.com
   Password: Folosește o parolă puternică
   First Name: Prenumele tău
   Last Name: Numele tău
   Country: Romania
   ```

3. **Verifică email-ul**:
   - Verifică inbox-ul email
   - Click pe link-ul de verificare
   - Contul Oracle este acum activ

## ☕ Pasul 2: Descarcă și Instalează Oracle JDK 21

### Ce este JDK?

**JDK (Java Development Kit)** este setul complet de unelte pentru dezvoltarea Java:

- **JRE**: Pentru rularea programelor Java
- **Compiler (javac)**: Pentru transformarea codului în programe
- **Debugger**: Pentru găsirea erorilor
- **Documentație**: Ghiduri și referințe

### Descărcarea Oracle JDK 21

1. **Login la Oracle**:

   - Mergi la [https://www.oracle.com/java/technologies/downloads/](https://www.oracle.com/java/technologies/downloads/)
   - Click "Sign In" și folosește contul Oracle

2. **Selectează Java 21**:

   - Găsește secțiunea "Java 21"
   - Tab "Windows"
   - Selectează "x64 Installer"
   - Fișierul: `jdk-21.0.x_windows-x64_bin.exe`

3. **Acceptă Licența și Descarcă**:
   - Bifează "I agree to the Oracle License Agreement"
   - Descărcarea începe automat

### Instalarea Oracle JDK 21

1. **Rulează Installer-ul**:

   - Click dreapta pe fișierul `.exe` descărcat
   - Selectează "Run as administrator"
   - Click "Yes" la permisiune

2. **Urmează Ghidul**:

   ```
   Welcome Screen → Click "Next"
   Installation Folder → Lasă default: C:\Program Files\Java\jdk-21
   Click "Next" → Așteaptă instalarea → Click "Close"
   ```

3. **Verifică Instalarea**:
   ```cmd
   "C:\Program Files\Java\jdk-21\bin\java" -version
   ```
   Ar trebui să vezi versiunea Java 21.

## 🔧 Pasul 3: Configurează Variabilele de Mediu

### Ce sunt Variabilele de Mediu?

**Variabilele de Mediu** sunt setări globale care îi spun computerului unde să găsească programele. Pentru Java avem nevoie de:

- **JAVA_HOME**: Unde este instalat Java
- **PATH**: Unde să caute comenzile `java` și `javac`

### Setarea Variabilelor

1. **Deschide System Properties**:

   - Apasă `Windows + R`
   - Scrie `sysdm.cpl` și apasă Enter
   - Click tab "Advanced" → "Environment Variables..."

2. **Creează JAVA_HOME**:

   - În "System variables", click "New..."
   - Variable name: `JAVA_HOME`
   - Variable value: `C:\Program Files\Java\jdk-21`
   - Click "OK"

3. **Actualizează PATH**:
   - Găsește și selectează "Path" în "System variables"
   - Click "Edit..." → "New"
   - Adaugă: `%JAVA_HOME%\bin`
   - Click "OK" pe toate dialogurile

### Verifică Configurația

**Deschide un Command Prompt NOU** și testează:

```cmd
echo %JAVA_HOME%
java -version
javac -version
```

Toate ar trebui să funcționeze fără erori.

## 🐙 Pasul 4: Creează Cont GitHub

### De ce GitHub?

**GitHub** îți permite să:

- Salvezi exercițiile în cloud
- Urmărești progresul de învățare
- Construiești un portofoliu
- Înveți workflow-ul profesional

### Crearea Contului

1. **Vizitează GitHub**:

   - Mergi la [https://github.com](https://github.com)
   - Click "Sign up"

2. **Completează Informațiile**:

   ```
   Username: nume-profesional (ex: ion-popescu-dev)
   Email: Același email ca la Oracle
   Password: Parolă puternică
   ```

3. **Verifică și Setup**:
   - Verifică email-ul
   - Completează pașii de setup
   - Alege planul gratuit

## 🔧 Pasul 5: Instalează și Configurează Git

### Ce este Git?

**Git** este sistemul de control al versiunilor care:

- Urmărește fiecare modificare de cod
- Îți permite să te întorci la versiuni anterioare
- Salvează exercițiile pe GitHub
- Este standard în industrie

### Instalarea Git

1. **Descarcă Git**:

   - Mergi la [https://git-scm.com/download/win](https://git-scm.com/download/win)
   - Descărcarea începe automat
   - Fișier: `Git-2.42.0-64-bit.exe`

2. **Opțiuni Instalare**:

   ```
   Select Components → Păstrează toate default
   Default Editor → "Use Visual Studio Code" (sau Notepad++)
   Initial Branch → "Override" → "main"
   PATH Environment → "Git from command line and 3rd-party software"
   HTTPS Transport → "Use the OpenSSL library"
   Line Ending → "Checkout Windows-style, commit Unix-style"
   Terminal → "Use Windows' default console window"
   Pull Behavior → "Default (fast-forward or merge)"
   Credential Helper → "Git Credential Manager"
   Extra Options → "Enable file system caching"
   ```

3. **Verifică Instalarea**:
   ```cmd
   git --version
   ```

### Configurarea Git

```cmd
git config --global user.name "Numele Tău Complet"
git config --global user.email "email-ul-tau@exemplu.com"
git config --global init.defaultBranch main
```

## 💻 Pasul 6: Instalează IntelliJ IDEA Community Edition

### De ce IntelliJ IDEA Community Edition?

**Community Edition este perfect pentru exercițiile noastre:**

- ✅ **Gratuit pe viață** - zero costuri
- ✅ **Toate funcțiile Java** - tot ce avem nevoie
- ✅ **Git integrat** - commit direct din IDE
- ✅ **Debugging avansat** - găsirea erorilor
- ✅ **Code completion** - scriere mai rapidă
- ✅ **Folosit în industrie** - pregătire profesională

### Descărcarea și Instalarea

1. **Descarcă Community Edition**:

   - Mergi la [https://www.jetbrains.com/idea/](https://www.jetbrains.com/idea/)
   - Click "Download"
   - În secțiunea **Community** (dreapta), click "Download"
   - **NU Ultimate** (stânga) - aceea costă bani

2. **Instalează**:
   ```
   Double-click pe ideaIC-2024.x.x.exe
   → Apasă "Yes" la UAC
   → "Next" → Lasă locația default → "Next"
   → Bifează: ✅ "64-bit launcher"
   → Bifează: ✅ "Update context menu"
   → Bifează: ✅ ".java files"
   → "Next" → "Install" → "Finish"
   ```

## ⚙️ Pasul 7: Configurează IntelliJ IDEA

### Prima Lansare

1. **Deschide IntelliJ IDEA**:

   - Double-click pe shortcut-ul de pe desktop
   - Prima lansare arată wizard-ul de setup

2. **Configurații Inițiale**:
   ```
   Import Settings → "Do not import settings" → "OK"
   License → "Evaluate for free" → Accept terms
   UI Theme → "Darcula" (recomandat) sau "IntelliJ Light"
   Featured Plugins → Păstrează toate activate
   ```

### Configurări Esențiale

1. **SDK Setup**:

   - File → Project Structure → Project
   - Project SDK → "Add SDK" → "JDK"
   - Navighează la: `C:\Program Files\Java\jdk-21`
   - Click "OK"

2. **Git Integration**:
   - File → Settings → Version Control → Git
   - Path to Git executable: `C:\Program Files\Git\bin\git.exe`
   - Test Connection → Should be successful

## 🧪 Pasul 8: Primul Exercițiu Java

### Creează Dosarul pentru Exerciții

1. **Creează Dosarul Principal**:

   ```cmd
   mkdir C:\JavaExercitii
   cd C:\JavaExercitii
   ```

2. **Inițializează Git**:
   ```cmd
   git init
   git remote add origin https://github.com/[NumeleTau]/java-exercitii.git
   ```

### Primul Exercițiu - Card Harry Potter

1. **Deschide IntelliJ**:

   - File → Open → Selectează `C:\JavaExercitii`
   - Click "Trust Project"

2. **Creează Primul Fișier**:

   - Click dreapta pe folderul proiectului
   - New → Java Class
   - Name: `Exercitiul01_CardHarryPotter`

3. **Scrie Primul Program**:

```java
// Exercitiul01_CardHarryPotter.java
// Concepte: variabile String, System.out.println, concatenare
// Dificultate: Începător

public class Exercitiul01_CardHarryPotter {
    public static void main(String[] args) {
        // Variabile pentru cardul Harry Potter
        String numeStudent = "Harry Potter";
        String casaHogwarts = "Gryffindor";
        String anScolar = "Anul 7";

        // Afișare informații card student
        System.out.println("🏰 CARD STUDENT HOGWARTS 🏰");
        System.out.println("===========================");
        System.out.println("Student: " + numeStudent);
        System.out.println("Casa: " + casaHogwarts);
        System.out.println("An școlar: " + anScolar);
        System.out.println("Status: Activ");
        System.out.println();
        System.out.println("✨ Bun venit la Hogwarts, " + numeStudent + "! ✨");
        System.out.println("Casa " + casaHogwarts + " te așteaptă!");
    }
}
```

### 🤔 Explicații Rapide pentru Primul Exercițiu

**Nu te speria de cod! Iată explicațiile de bază (le vom detalia complet în curs):**

#### **Ce este o clasă?**

```java
public class Exercitiul01_CardHarryPotter {
    // Codul nostru aici
}
```

- **Clasa** = o "cutie" care conține codul nostru
- `public` = poate fi folosită de oriunde
- `class` = cuvântul magic care spune "aici începe clasa"
- `Exercitiul01_CardHarryPotter` = numele clasei (trebuie să fie identic cu numele fișierului)
- `{ }` = acoladele marchează începutul și sfârșitul clasei

#### **Ce este metoda main?**

```java
public static void main(String[] args) {
    // Codul care se execută aici
}
```

- **main** = "ușa de intrare" în programul nostru
- Java caută întotdeauna metoda `main` pentru a ști de unde să înceapă
- `public static void` = cuvinte magice pe care le vom înțelege în curs
- `String[] args` = permite programului să primească informații din exterior
- Tot codul dintre `{ }` se execută când rulăm programul

#### **Ce sunt variabilele?**

```java
String numeStudent = "Harry Potter";
String casaHogwarts = "Gryffindor";
```

- **Variabila** = o "cutie cu etichetă" în care stocăm informații
- `String` = tipul de date pentru text (cuvinte, propoziții)
- `numeStudent` = numele cutiei (etichetă)
- `=` = "pune în cutie"
- `"Harry Potter"` = textul pe care îl stocăm (întotdeauna între ghilimele)

#### **Ce face System.out.println?**

```java
System.out.println("Bun venit la Hogwarts!");
System.out.println("Student: " + numeStudent);
```

- **System.out.println** = comanda pentru a afișa text pe ecran
- Tot ce punem între `( )` se afișează în consolă
- `+` = lipește texturile împreună (concatenare)
- `"Student: " + numeStudent` = combină textul cu valoarea din variabilă

#### **Ce sunt comentariile?**

```java
// Acesta este un comentariu pe o linie
/* Acesta este un comentariu
   pe mai multe linii */
```

- **Comentariile** = note pentru oameni, Java le ignoră
- Folosim `//` pentru comentarii scurte
- Folosim `/* */` pentru comentarii lungi
- Ajută să înțelegem ce face codul

### 📚 **Important de Reținut:**

- **Nu memoriza acum tot!** Acestea sunt doar explicații rapide
- **Fiecare concept** va fi explicat în detaliu în lecțiile următoare
- **Focus pe primul exercițiu:** să vezi că programul rulează și afișează textul
- **Întrebările** sunt normale - le vom clarifica pas cu pas în curs!

4. **Rulează Programul**:
   - Click dreapta în editor → "Run 'Exercitiul01_CardHarryPotter.main()'"
   - Ar trebui să vezi output-ul în consola de jos

## 📝 Pasul 9: Primul Commit Git

### Salvează Primul Exercițiu

1. **Verifică Statusul**:

   ```cmd
   git status
   ```

2. **Adaugă Fișierul**:

   ```cmd
   git add Exercitiul01_CardHarryPotter.java
   ```

3. **Primul Commit**:

   ```cmd
   git commit -m "feat: add exercițiul 01 - card Harry Potter cu variabile String

   - Primul program Java cu tema carduri fidelitate
   - Demonstrează declararea și folosirea variabilelor String
   - Învățat System.out.println pentru afișare în consolă
   - Folosit concatenarea string-urilor cu operatorul +
   - Creat structura de bază pentru exercițiile următoare"
   ```

4. **Push pe GitHub**:
   ```cmd
   git push -u origin main
   ```

## ✅ Verificare Setup Complet

După finalizare, ar trebui să poți:

- [ ] ✅ **Java**: `java -version` arată Java 21
- [ ] ✅ **Compiler**: `javac -version` arată versiunea
- [ ] ✅ **Environment**: `echo %JAVA_HOME%` arată calea
- [ ] ✅ **Git**: `git --version` arată versiunea Git
- [ ] ✅ **GitHub**: Vezi primul commit online
- [ ] ✅ **IntelliJ**: Rulezi exerciții Java
- [ ] ✅ **Output**: Vezi mesajul Harry Potter în consolă

## 🎯 Ce Urmează?

**Felicitări! Ai configurat cu succes mediul de dezvoltare Java!**

### Setup-ul Tău Include:

- ✅ **Oracle JDK 21** - Ultima versiune LTS
- ✅ **IntelliJ IDEA Community** - IDE gratuit și puternic
- ✅ **Git & GitHub** - Control versiuni profesional
- ✅ **Primul exercițiu** - Card Harry Potter functional
- ✅ **Workflow complet** - De la cod la GitHub

### Următorii Pași:

👉 **Continuă cu:** [Exercițiile de Variabile](../02-fundamentals/01-variables/README.md)

---

**Mediul de dezvoltare este gata!**

_Să începem să învățăm Java prin exerciții simple și distractive! 🚀_
