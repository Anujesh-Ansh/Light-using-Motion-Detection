# Motion Sensor Lamp Project

Welcome to the Motion Sensor Lamp project! 🌟

Experience the magic of creating your own motion-activated lamp using a PIR sensor, LED, resistor, Arduino, and a breadboard. Let's dive into the details of how to set it up and bring this project to life! 🚀

## Components Needed

- PIR (Passive Infrared) Sensor
- LED 💡
- 220 ohm Resistor
- Arduino Board 🛠️
- Breadboard 🔌
- Connecting wires 🧵

## Circuit Connection

Follow these steps to connect the components:

1. Connect the **5V** from the Arduino to the **positive line** of the breadboard (`🟥 red wire`).
2. Connect the **GND** from the Arduino to the **negative line** of the breadboard (`⬛️ black wire`).
3. Connect the **GND** (Ground) pin of the PIR sensor to the **negative line** of the breadboard (`⬛️ black wire`).
4. Connect the **Power** pin of the PIR sensor to the **positive line** of the breadboard (`🟥 red wire`).
5. Connect the **Signal** pin of the PIR sensor to **Digital Pin 2** of the Arduino (`🟨 yellow wire`).
6. Connect **Digital Pin 13** of the Arduino to the **anode (+)** of the LED (`🟩 green wire`).
7. Connect one end of the **220 ohm resistor** to the **cathode (-)** of the LED.
8. Connect the other end of the **220 ohm resistor** to the **negative line** of the breadboard (GND) (`⬛️ black wire`).

![Circuit Diagram](https://github.com/Anujesh-Ansh/Light-using-Motion-Detection/raw/main/circuit-image.JPG)

Now that your circuit is set up, let's move on to the code implementation! 

## Arduino Code

```cpp
int pirsensor = 0;

void setup()
{
  pinMode(13, OUTPUT);  // Set digital pin 13 as an OUTPUT
  pinMode(2, INPUT);    // Set digital pin 2 as an INPUT for PIR sensor
}

void loop()
{
  pirsensor = digitalRead(2);  // Read the value from PIR sensor connected to pin 2

  if (pirsensor == HIGH)
  {
    digitalWrite(13, HIGH);  // Turn on the LED if motion is detected
  }
  else
  {
    digitalWrite(13, LOW);  // Turn off the LED if no motion is detected
  }

  delay(10);  // Delay for stability
}
```

## Usage

1. Upload the provided Arduino code to your Arduino board.
2. Power the circuit by connecting the Arduino to a USB port or an external power source.
3. Place the PIR sensor in a location where it can detect motion.
4. When motion is detected, the LED will illuminate, creating your motion-activated lamp! 💡

Enjoy experimenting with this fun and practical project. Happy making! 🛠️
