## Breadboard Diagram
![image]![ACT1](https://github.com/user-attachments/assets/b4eef8d0-c5e7-4a1e-bf57-322ec3311d2a)


1. **Variable Declaration**
   - An array `ledPins[]` is declared, containing the pin numbers `{12, 11, 10, 9, 8}`. These pins will be used to control the LEDs.
   - The constant `numLeds` is set to 5, representing the number of LEDs connected.

2. **Setup Function**
   - The `setup()` function runs once when the program starts.
   - A `for` loop is used to configure each pin in the `ledPins[]` array as an output using `pinMode()`.  
     This means all 5 pins are prepared to send signals (HIGH or LOW) to the LEDs.

3. **Loop Function**
   - The `loop()` function runs continuously after `setup()` finishes.
   - It contains two `for` loops:
     - **First Loop (Turn LEDs ON):**
       - Each LED is turned on sequentially by sending a HIGH signal (`digitalWrite(ledPins[i], HIGH)`).
       - After each LED is turned on, the program waits for 1 second (`delay(1000)`).
     - **Second Loop (Turn LEDs OFF):**
       - Each LED is then turned off sequentially by sending a LOW signal (`digitalWrite(ledPins[i], LOW)`).
       - Again, the program waits for 1 second between each action.

### Output Effect
This creates a visual effect where:
- The LEDs connected to pins 12, 11, 10, 9, and 8 light up one after the other, with a 1-second delay between each.
- After all are lit, they turn off one by one in the same order, also with a 1-second delay.
- The sequence repeats indefinitely, producing a simple "chasing lights" pattern.
