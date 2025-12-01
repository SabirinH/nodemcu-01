# Nodemcu-01

## Introduktion
Jag ska visa hur man skriver ett enkelt blinkprogram. Syftet är att kunna förstå hur Arduino IDE fungerar och hur man enkelt styr en innbyggd LED med kod. Här nedan syns en bild på ett Plusivo Kit.

<img width="1590" height="1590" alt="image" src="https://github.com/user-attachments/assets/0ff604d8-1bb9-47c0-bb10-22dc3f52aa5a" />

## Vad är Mikroprocessor?
Mikroprocessor fungerar som en minidator och kan programmeras så att den styr saker t.ex. en lampa eller en sensor. Den har även en WiFI och kan kopplas till internet. Med hjälp av Aurdino IDE kan man programmera den. Här är en bild på en mikroprocess ( ESP8266) som ska användas under projektet. 

<img width="3000" height="3000" alt="image" src="https://github.com/user-attachments/assets/558cbb8f-180e-422c-a190-e606c9ad2e6d" />


# Kort om Arduino och hur den fungerar

 Programmet består av två basfunktioner, alltså två delar
```cpp
 setup()
 ```
 - Den kör en gång när programmet startar
```cpp
loop()
```
  - Den kör om och om igen
  

    
<img width="1024" height="640" alt="image" src="https://github.com/user-attachments/assets/60a96fb9-6c60-4cf9-a396-8e8762a2b797" />



## Portinitialisering 
Portinitialisering är när man talar om för en dator, mikrokontroller eller ett program vilken port som ska användas och hur den ska fungera.
Det är alltså ett sätt att “göra porten redo” innan den används.
Behövs för att LED-lampan på NodeMCU ska fungera.

```cpp
pinMode(LED_BUILTIN, OUTPUT);
```

## Hur man installerar Arduino IDE och får ett fungerande Blink-program

### Steg 1 – Konfigurera Board Manager
Öppna Arduino IDE och gå till File → Preferences. 

### Steg 2 – Installera ESP8266-komponenter
Gå till Tools → Board → Boards Manager. Sök efter ESP8266 och installera den.

### Steg 3 – Val av board och seriell port
Under Tools → Board → boards manager

### Steg 4 – Ladda Blink-exemplet
Öppna Arduino-exemplets Blink-fil via: File → Examples → 01.Basics → Blink.

### Steg 5 – Koppla in hårdvaran
Anslut NodeMCU till datorn via USB. ESP8266 har inbyggd USB-till-seriell omvandlare som gör uppladdning enkel.

### Steg 6 – Kompilera och ladda upp
Tryck på Upload. Arduino IDE kompilerar koden till ESP8266-format och skickar den över USB. Under uppladdningen kan LED:n på kortet blinka snabbt.

### Steg 7 – Funktionstest
När uppladdningen är klar startar programmet automatiskt. LED:n kommer nu blinka varje halv sekund.

### Mitt försök:

<img width="480" height="640" alt="image" src="https://github.com/user-attachments/assets/a3680292-daa4-4d65-98b4-26bd59aa24a9" />



## Kod
```cpp
int ledPin = D4;

void setup() {
  pinMode(ledPin, OUTPUT);
}

void loop() {
  digitalWrite(ledPin, HIGH);
  delay(500);
  digitalWrite(ledPin, LOW);
  delay(500);
}

