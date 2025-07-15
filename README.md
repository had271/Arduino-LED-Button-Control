# Arduino-LED-Button-Control
This project is about using Arduino with three leds and three buttons. 
Each button controls one LED 

**The components Used**
1. ArduinonUNO
2. 3 buttons
3. 3 LEDs
4. 3  resistors for LEDs, 3  resistors for buttons
5. Breadboard
6. Wires

![Demo Image](arduino_project.png)

*Figure 1: Top view of the full LED-button system.*


#### 🧪 Tinkercad Simulation

You can view and simulate the full Arduino project on Tinkercad using the link below:
[Open Tinkercad Simulation](https://www.tinkercad.com/things/4nhmCCRaghk-arduinoproject)

## Arduino Code

```cpp
void setup() {
  pinMode(7, INPUT);
  pinMode(4, INPUT);
  pinMode(2, INPUT);
  pinMode(13, OUTPUT);
  pinMode(12, OUTPUT);
  pinMode(8, OUTPUT);
}

void loop() {
  if (digitalRead(7) == HIGH) {
    digitalWrite(13, HIGH);
    delay(1000);
    digitalWrite(13, LOW);
    delay(100);
  } 
  else if (digitalRead(4) == HIGH) {
    digitalWrite(12, HIGH);
    delay(1000);
    digitalWrite(12, LOW);
    delay(100);
  } 
  else if (digitalRead(2) == HIGH) {
    digitalWrite(8, HIGH);
    delay(1000);
    digitalWrite(8, LOW);
    delay(100);
  } 
  else {
    digitalWrite(13, LOW);
    digitalWrite(12, LOW);
    digitalWrite(8, LOW);
  }
}
