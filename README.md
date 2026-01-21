# Control WS2812B LED Strip using STM32F407VET6

This project demonstrates how to control a WS2812B addressable RGB LED strip using the STM32F407VET6 microcontroller. The system features a variety of pre-programmed lighting effects and includes **Audio Reactive** modes that respond to sound volume and frequency, captured via a MAX9814 microphone module (ADC).

## 🛠️ Hardware Requirements

* **Microcontroller:** STM32F407VET6 Development Board.
* **LEDs:** WS2812B LED Strip (5V).
* **Audio Sensor:** MAX9814 Microphone Module (Auto Gain Control).
* **Input:** 2x Push Buttons.
* **Power:** 5V Power Supply (External power recommended for the LED strip).

## 🔌 Pinout Configuration

| Component | Pin Name | STM32 Pin | Function |
| :--- | :--- | :--- | :--- |
| **WS2812B** | DIN | `PE9` | PWM Output |
| | VCC | 5V | Power |
| | GND | GND | Ground |
| **MAX9814** | OUT | `PA0` | ADC Input |
| | VDD | 3.3V | Power |
| | GND | GND | Ground |
| **MODE BUTTON** | - | `PA4` | Next Effect |
| | VCC | 5V | Power |
| | GND | GND | Ground |
| **BRIGHTNESS MODE BUTTON** | - | `PE11` | Reset Effect |
| | VCC | 5V | Power |
| | GND | GND | Ground |

## 🚀 Usage Guide

1.  **Wiring:** Connect all hardware components according to the Pinout Configuration table above.
    * *Note: Ensure the grounds (GND) of the STM32, LED strip, and Power Supply are connected together.*
2.  **Upload:** Flash the firmware to the STM32F407VET6 using an ST-Link.
3.  **Controls:**
    * **Next Effect Button:** Press to cycle through the available lighting modes.
    * **Brightness Button:** Press to cycle through different brightness levels.
    * **Audio Mode:** When in audio-reactive mode, place a sound source near the MAX9814 module to see the LEDs dance to the music.

## ⚠️ Important Notes

* **Power Supply:** WS2812B LEDs consume a significant amount of current (approx. 60mA per LED at full white brightness). Do not power long strips directly from the STM32's 5V pin; use an external power supply.
* **Logic Level:** WS2812B data logic is 5V, while STM32 is 3.3V. While it often works directly, a Logic Level Shifter is recommended if the LEDs flicker or behave erratically.

---
*Project by:*
* *Nguyen Trong Bao Duy/Thorlion*
* *Nguyen Dang Phuong Duy/DuyNDP*
* *Vu Dai Duong/VuDaiDuong_325*
* *Phan Thanh Duy*
