# Programmable Gain Amplifier (ESP32 + MOSFET-switched feedback)

A programmable gain amplifier (PGA) built on a breadboard. An op-amp stage has its feedback resistance selected by MOSFETs, and an ESP32 picks the gain level over serial.

## How it works

- Op-amp based amplifier stage.
- Feedback resistors are switched in and out with MOSFETs.
- An ESP32 drives the MOSFET gates from GPIO outputs.
- The gain level is chosen by typing `1` to `4` into the Arduino IDE Serial Monitor (115200 baud). The ESP32 replies with a confirmation line.

| Gain level | Resistor selected (from serial output) |
|-----------:|:---------------------------------------|
| 1 | 47 kOhm |
| 2 | 22 kOhm |
| 3 | 220 kOhm |
| 4 | 47 kOhm (a second 47 kOhm resistor) |

Example serial output: `Success: Gain Level 3 Selected (220kOhm active).`

## Media

- `media/photos/serial-monitor-gain-1.jpg` ... `gain-4.jpg`: Serial Monitor after selecting each level.
- `media/photos/multimeter-0.501V-*.jpg` and `multimeter-317.4mV.jpg`: multimeter (DM-97) readings on the breadboard. Which gain level and input each reading belongs to is still to be documented.
- `media/videos/demo-1.mp4` ... `demo-4.mp4`: working demos (compressed, audio removed).

## TODO

- [ ] Op-amp part number
- [ ] Input signal (type, amplitude, frequency)
- [ ] Measured output and gain for each level
- [ ] Circuit schematic
- [ ] Add the ESP32 firmware (not in this repo yet)
- [ ] Label which multimeter reading belongs to which gain level
