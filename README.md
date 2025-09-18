# Arduino LED Chasing Lights

This project demonstrates how to control multiple LEDs in sequence using an Arduino.  
The LEDs turn on one after another, then turn off in the same order, creating a simple "chasing lights" effect.

---

## Breadboard Diagram
![Breadboard Diagram](./13q4trgf.png)

---

## Code

```cpp
const int ledPins[] = {12, 11, 10, 9, 8};
const int numLeds = 5;

void setup() {
  for (int i = 0; i < numLeds; i++) {
    pinMode(ledPins[i], OUTPUT);
  }
}

void loop() {
  // Turn LEDs ON one by one
  for (int i = 0; i < numLeds; i++) {
    digitalWrite(ledPins[i], HIGH);
    delay(1000);
  }
  
  // Turn LEDs OFF one by one
  for (int i = 0; i < numLeds; i++) {
    digitalWrite(ledPins[i], LOW);
    delay(1000);
  }
}
