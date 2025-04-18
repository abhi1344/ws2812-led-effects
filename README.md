# 🌈 WS2812 RGB LED Controller

This project is a simple RGB LED control system using Arduino Nano and WS2812 addressable LEDs. It creates vibrant color effects using customizable animations.

---

## 🔧 Components Used

- Arduino Nano  
- WS2812 LED Strip (NeoPixel)  
- 5V DC Power Supply  
- 470Ω Resistor (Data line)  
- 1000µF Capacitor (recommended for stability)  
- Breadboard & Jumper wires  

---

## 💡 Features

- Custom light animations  
- Brightness and speed control (optional)  
- Uses Adafruit_NeoPixel library  
- Easy to expand for multiple LED strips  

---

## ⚙️ How It Works

- Arduino sends control signals to the data pin of the WS2812 LEDs.  
- The sketch cycles through different colors and effects.  
- You can edit the sketch to change animations, brightness, and number of LEDs.  

---

## 📸 Preview

![RGB LED Preview](./Images/rgb_led_preview.jpg)

---

## 💻 Code

You can find the main code in:

📂 Code/ws2812_control.ino

Example snippet:

```cpp
#include <Adafruit_NeoPixel.h>
#define PIN 6
#define NUMPIXELS 8

Adafruit_NeoPixel pixels(NUMPIXELS, PIN, NEO_GRB + NEO_KHZ800);

void setup() {
  pixels.begin();
}

void loop() {
  for (int i = 0; i < NUMPIXELS; i++) {
    pixels.setPixelColor(i, pixels.Color(255, 0, 0)); // Red
    pixels.show();
    delay(100);
  }
}
