# Arduino Ultrasonic Distance Indicator with 3 LEDs

A simple Arduino project that uses an HC-SR04 Ultrasonic Sensor to measure distance and indicate the object's position using three LEDs.

## Features

- Measures distance using the HC-SR04 Ultrasonic Sensor
- Displays distance in the Serial Monitor
- Uses 3 LEDs for visual distance indication:
  - 🟢 Green LED → Object is far away (> 20 cm)
  - 🟡 Yellow LED → Object is at medium distance (10–20 cm)
  - 🔴 Red LED → Object is close (< 10 cm)
- Real-time distance updates every 100 ms

---

## Components Required

| Component | Quantity |
|------------|-----------|
| Arduino Uno | 1 |
| HC-SR04 Ultrasonic Sensor | 1 |
| LEDs (Green, Yellow, Red) | 3 |
| 220Ω Resistors (Optional) | 3 |
| Jumper Wires | Several |
| Breadboard (Optional) | 1 |

---

## Circuit Connections

### HC-SR04 Ultrasonic Sensor

| Sensor Pin | Arduino Pin |
|------------|------------|
| VCC | 5V |
| GND | GND |
| TRIG | D9 |
| ECHO | D10 |

### LEDs

| LED | Arduino Pin |
|------|-------------|
| Green LED (Far) | D2 |
| Yellow LED (Medium) | D3 |
| Red LED (Close) | D4 |

### LED Wiring

- Long leg (Anode) → 220Ω Resistor → Arduino Pin
- Short leg (Cathode) → GND

---

## Distance Logic

| Distance | LED Status |
|-----------|------------|
| Greater than 20 cm | Green LED ON |
| 10 cm to 20 cm | Yellow LED ON |
| Less than 10 cm | Red LED ON |

Only one LED is active at a time.

---

## Arduino Code

Upload the provided Arduino sketch to your Arduino Uno using the Arduino IDE.

The program:

1. Sends an ultrasonic pulse from the HC-SR04 sensor.
2. Receives the reflected pulse.
3. Calculates the distance in centimeters.
4. Prints the distance to the Serial Monitor.
5. Turns on the corresponding LED based on the measured distance.

---

## Example Output

```text
Distance: 35.42 cm
Distance: 18.76 cm
Distance: 7.84 cm
```

LED Response:

```text
35 cm  → Green LED ON
18 cm  → Yellow LED ON
7 cm   → Red LED ON
```

---

## Applications

- Obstacle Detection
- Parking Assistance Systems
- Distance Monitoring
- Robotics Projects
- Smart Safety Systems
- Educational Arduino Projects

---

## How to Run

1. Assemble the circuit according to the wiring diagram.
2. Open the Arduino IDE.
3. Connect the Arduino Uno to your computer.
4. Upload the code.
5. Open the Serial Monitor.
6. Move an object in front of the sensor and observe the LEDs change based on distance.

---

## Future Improvements

- Add a buzzer for audible alerts.
- Display distance on an LCD or OLED screen.
- Implement RGB LED indication.
- Add Bluetooth or Wi-Fi monitoring.
- Log distance measurements to a computer.

---

## License

This project is open-source and available under the MIT License.

---

### Author

Built with Arduino Uno and HC-SR04 Ultrasonic Sensor for simple distance detection and visual indication.
