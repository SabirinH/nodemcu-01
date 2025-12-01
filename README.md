# nodemcu-01

## I detta projekt kommer jag visa hur man får en LED att blinka på NodeMCU (ESP8266)

## Steg 1. Konfigurera Board Manager
Börja med att klicka dig in på Arduino IDE. Gå till File → Preferemces. I fältet ADditional Boards Manager URL:s, lägg till ESP8266-URL:en. Detta gör att IDE:n kan hämta samt installera ESP8266-plattformens definitionsfilter.

## Steg 2. Insallera ESP8266-komponenter
Installera ESP8266 på Arduino IDE genom att skriva in det under boards manager i searchboxen 

## Steg 3.
I nästa steg väljer du board och port och trycker sedan på Generic ESP8266 module, sedan klistrar in koden som du hade kopierat 

## Steg 4.
Du ska öppna upp Arduino IDE, och sedan hämta den färdiga BLINK programmet du har.
File - 01.Basics - Blink

## Steg 5. 
Nästa steg är att koppa in NodeMCU. Använd USB-Kabeln från pulsivo-kitet.

## Steg 6. 
Ladda upp prgrammet. Programmet komplieras och laddas upp.

## Steg 7.
Lampan blinkar.


# Här ser ni ett Exempel på en kod:
# Kod
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

