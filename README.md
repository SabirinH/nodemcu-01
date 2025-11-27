# nodemcu-01

I detta projekt kommer jag visa hur man får en LED att blinka på NodeMCU (ESP8266)

## Kod
´´´cpp
int ledPIN = D4;

void setup() {
     pinMode(ledPin, OUTPUT);
}

void loop() {
  digialWrite(ledPin, HIGH);
  delay(500);
  digialWrite(ledPin, LOW);
  delay(500);
  }
