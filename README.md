# led-status-bar

## Hardware
- Lights: WS2812b or similar
- Support circuitry: 
  - Level Shifter (3.3v Raspberry Pi logic to 5v WS2812b logic)
- MCU: Raspberry Pi
- Power: 5v 2A Power Supply
- Interface: Keyboard Buttons or similar

### Wiring
- USB Power to Raspberry Pi
- Level Shifter
  - 5v rail to level shifter High
  - GND to level shifter both sides
  - Pi pin 18 to level shifter low
- Neopixels
  - 5v to neopixel 5v
  - GND to neopixel GND
  - Level shifter high pin to neopixel input pin
- Buttons
  - Button pin to one side of button, other side attached to GND (Assign pull up resistor to each)

## Software
- Adafruit_Blinka
- CircuitPython support in Python
```
sudo pip3 install rpi_ws281x adafruit-circuitpython-neopixel
sudo python3 -m pip install --force-reinstall adafruit-blinka
```