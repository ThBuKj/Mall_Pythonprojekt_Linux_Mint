# Mall för Pythonprojekt på Linux Mint

En enkel mall för att snabbt komma igång med ett nytt Python-projekt på **Linux Mint**.  
Den hjälper dig att skapa en isolerad miljö med `venv` och installera nödvändiga verktyg, som exempelvis **Mypy**.

---

## Kom igång

### 1. Skapa och gå till projektmappen

Navigera till din utvecklingskatalog och skapa din nya projektmapp:

```bash
# Byt ut 'mitt-nya-projekt-namn' till vad ditt projekt heter
mkdir mitt-nya-projekt-namn
cd mitt-nya-projekt-namn
```

---

### 2. Installera venv-verktyget (körs endast en gång)

Om du får fel när du försöker skapa den virtuella miljön (t.ex. att ensurepip saknas), måste du installera paketet systemomfattande. Kör detta endast vid behov:

```bash
sudo apt install python3.12-venv
```

---

### 3. Skapa och aktivera den virtuella miljön

```bash
# Skapar mappen 'venv' inuti projektet
python3 -m venv venv

# Aktiverar miljön (du ska se (venv) nu)
source venv/bin/activate
```

När miljön är aktiv ser du `(venv)` före prompten i terminalen.

---

### 4. Installera nödvändiga paket och spara beroenden

Installera de paket du behöver i den isolerade miljön. Installera till exempel Mypy och spara sedan alla beroenden i filen `requirements.txt`.

```bash
# 1. Installera dina paket
pip install mypy
# Exempel: pip install requests

# 2. Spara alla installerade paket i en fil för delning (viktigt!)
pip freeze > requirements.txt
```

---

### 5. Starta Visual Studio Code

Öppna projektet i VS Code:

```bash
code .
```

---

## 💡 Tips

Aktivera miljön varje gång du öppnar terminalen:

```bash
source venv/bin/activate
```

Avaktivera miljön:

```bash
deactivate
```

Installera allt från `requirements.txt` (om du delar projektet):

```bash
pip install -r requirements.txt
```

---

✅ **Klart!**  
Nu har du en färdig, isolerad Pythonmiljö redo för utveckling på Linux Mint.
