# nodemcu-01

I detta projekt kommer jag visa hur man får en LED att blinka på NodeMCU (ESP8266)

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

