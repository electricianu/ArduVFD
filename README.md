# ArduVFD – Variator de Frecvență Trifazat cu Arduino Mega (Proiect Didactic)

**ArduVFD** este un convertizor de frecvență trifazat (VFD – *Variable Frequency Drive*) conceput în **scop didactic**, destinat studiului generării semnalelor SPWM trifazate și al controlului motoarelor asincrone cu ajutorul platformei **Arduino Mega 2560**.

Proiectul este complet documentat și include atât **codul sursă pentru Arduino IDE**, cât și **simularea completă în Proteus**, permițând testarea și vizualizarea semnalelor direct pe calculator înainte de orice execuție practică.

## Specificații tehnice principale
* **Scop:** Didactic / experimental (studiul acționărilor electrice și al modulării SPWM trifazate)
* **Unitate de control:** Arduino Mega 2560
* **Etaj de putere:** Modul inteligent **IRAMS10UP60A** (IPM – *Intelligent Power Module*, 600V / max. 10A, cu punte IGBT trifazată, drivere gate și protecții integrate)
* **Izolare galvanică:** Intrări de comandă izolate optic (optocuploare) + circuite tampon (buffer) între logică și modulul de putere
* **Interfață utilizator:** Afișaj alfanumeric **LCD 16x2** și taste de navigare/reglaj
* **Alimentare:** Sursă auxiliară de 24V DC (cu stabilizare la 5V pentru partea logică) + bus DC pentru etajul de putere

## Structura acestui repository
* `Documentatie/` – Documentația tehnică completă (`ArduVFD.pdf` cu schema electrică, cablajul PCB și explicații)
* `Firmware/` – Codul sursă complet scris în **Arduino IDE** (`.ino`)
* `Simulare_Proteus/` – Proiectul de simulare în **Proteus** pentru testarea virtuală a montajului și analiza formelor de undă

## Cum se testează în simulare
1. Deschideți fișierul din folderul `Firmware/` în **Arduino IDE**, selectați placa **Arduino Mega 2560** și compilați codul (*Sketch → Export Compiled Binary* pentru a obține fișierul `.hex`).
2. Deschideți proiectul din folderul `Simulare_Proteus/` în **Proteus**, încărcați fișierul `.hex` în microcontrolerul Arduino Mega și porniți simularea.

## Avertisment de siguranță
> **Atenție!** Proiectul este realizat exclusiv în **scop didactic**. Deși modulul `IRAMS10UP60A` suportă până la 600V / 10A, lucrul cu tensiuni mari pe bus-ul DC implică risc major de electrocutare. Construcția și testarea fizică trebuie efectuate doar de persoane calificate, preferabil alimentând inițial etajul de putere la tensiune redusă (ex. prin autotransformator/variac) și cu izolare galvanică corespunzătoare.
