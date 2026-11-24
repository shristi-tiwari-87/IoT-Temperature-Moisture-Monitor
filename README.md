# IoT Temperature and Moisture Monitoring System

## Project Overview

This project uses an ESP32, DHT22 sensor and OLED display to monitor environmental temperature and humidity. The readings are displayed on the OLED and sent to the Serial Monitor.

An LED and buzzer provide an alert when the measured conditions move outside the configured range.

## Hardware

- ESP32-S3
- DHT22 temperature and humidity sensor
- OLED display
- LED
- Buzzer
- Breadboard
- Jumper wires

## Pin Configuration

| Component | ESP32 Pin |
|---|---|
| DHT22 Data | GPIO 4 |
| OLED SDA | GPIO 8 |
| OLED SCL | GPIO 9 |
| LED | GPIO 5 |
| Buzzer | GPIO 15 |

## Arduino Libraries

Install these libraries from Arduino IDE Library Manager:

- DHT sensor library by Adafruit
- Adafruit GFX Library
- Adafruit SSD1306

## How It Works

The DHT22 measures temperature and humidity. The ESP32 reads the sensor values and displays them on the OLED. The values are also printed in the Serial Monitor.

The current alert limits in the code are:

- Temperature: 20–30 °C
- Humidity: 40–80 %

When a value is outside these limits, the LED and buzzer are activated.

## Uploading the Code

1. Open `IoT_Temperature_Moisture_Monitor.ino` in Arduino IDE.
2. Select the correct ESP32-S3 board.
3. Select the correct COM port.
4. Install the required libraries.
5. Click Upload.
6. Open Serial Monitor at 115200 baud.

## Note

If your DHT22 data wire is connected to a different GPIO, change the `DHTPIN` value in the `.ino` file before uploading.
