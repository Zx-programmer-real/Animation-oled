🎬 OLED Animation Studio
OLED Animation Studio** is a modern web-based tool designed to make it easy for electronics hobbyists (makers) to convert images or videos into C++ code (PROGMEM) for monochrome OLED displays (SSD1306).

This tool is highly useful for creating lyric animations, moving logos, or short footages for your Arduino and ESP32 projects.

(✨ Key Features )
- **Dual Input:** Supports uploading multiple image frames (sequences) or directly uploading a single video file (.mp4/.webm).
- **Video to Frame:** Automatically extracts video into image frames directly within the browser.
- **Live Preview:** Realistic OLED display simulation with resolution options (128x64, 128x32, 64x48).
- **Real-time Threshold:** Adjust black-and-white contrast with an auto-pause feature when dragging the slider for precise adjustments.
- **Universal Code:** Generates C++ code compatible with Arduino Uno, Nano, and ESP32.

(🚀 How to Use )

# 1. Image/Video Preparation
- **If using images:** Ensure the file naming sequence is correct (e.g., `frame1.png`, `frame2.png`, etc.).
- **If using video:** Use short videos (10-15 seconds) to avoid running out of microcontroller memory.

# 2. Using the Web Studio
1. Open this website in your browser.
2. Select your OLED resolution (e.g., 128x64).
3. Upload your files in the **Settings & Upload** section.
4. Adjust the **Threshold** until the lyrics/images look clear in the **Live Preview** section.
5. Click the **⚡ Generate C++ Code** button.
6. Click **📋 Copy Code to Clipboard**.

# 3. Hardware Implementation
1. Open the **Arduino IDE** (or Wokwi / PlatformIO).
2. Create a new tab named `animation.h` and paste the copied code.
3. In the main tab (`.ino`), include the file using `#include "animation.h"`.
4. Use the `display.drawBitmap()` function inside the `loop()` to display the frames sequentially.

🔌 Wiring (ESP32 Standard)
| OLED Pin | ESP32 Pin |
|----------|-----------|
| VCC      | 3.3V      |
| GND      | GND       |
| SDA      | GPIO 21   |
| SCL      | GPIO 22   |

🛠️ Required Libraries
Ensure you have installed the following libraries in your Arduino IDE:
- **Adafruit SSD1306**
- **Adafruit GFX Library**

Made Using Vibe Coding To Explore World with AI
Made with ❤️ for the Arduino & ESP32 community international and indonesian.
