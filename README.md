# Progetto: Rule Management System (Gruppo14)

Questo repository contiene un semplice sistema di gestione di regole (Rule Management System) sviluppato in Java, insieme a esempi Python per trigger/azioni esterne.

**Panoramica**
- **Codice Java:** si trova in `Gruppo14/src/` e include:
  - `ActionFolder/` — implementazioni di azioni (es. `ExternalProgramAction`, `WriteStringOnFileAction`, ecc.)
  - `TriggerFolder/` — implementazioni di trigger (file system, ora, data, contatori, ecc.)
  - `RuleFolder/` — gestione delle regole, salvataggio/caricamento
  - `CounterFolder/` — contatori usati da alcune regole
  - `App.java` — interfaccia console principale (menu) per creare/modificare/eseguire regole
- **File di esempio/Python:** `ExProgramTrigger.py`, `ExternalProgramActionExample.py` all'interno della root del progetto
- **File di serializzazione regole:** `rules.ser` (presente in root e in `Gruppo14/src/`)

(TEST E RELATIVE CARTELLE PRESENTI SU GIT PER SCOPO INFORMATIVO E DI ESPOSIZIONE)

Requisiti
- Java JDK 8 o superiore
- (Opzionale per i test) JUnit 4.x o JUnit 5 e relativi jar
- Python 3.x per gli script Python di esempio

Struttura del progetto

- `Gruppo14/src/` — sorgenti Java
- `lib/` — librerie opzionali (se le aggiungi, ad esempio jar per JUnit)

Compilazione ed esecuzione (PowerShell)

1) Compilare tutti i sorgenti Java

```powershell
# Posizionati nella cartella dei sorgenti
cd .\Gruppo14\src

# Raccogli tutti i file .java e compila nella cartella ../bin
$files = Get-ChildItem -Recurse -Filter *.java | ForEach-Object { $_.FullName }
javac -d ..\bin $files
```

2) Eseguire l'applicazione console (menu)

```powershell
# Sempre da Gruppo14\src
java -cp ..\bin App
```
