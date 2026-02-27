🚀 STM32 WiFi Relay Automation

📌 Overview

This project implements a simple IoT-based relay control system using STM32F411 and ESP8266 (AT firmware).

The STM32 communicates with the ESP8266 via UART and starts a web server.

connection reference:

![WhatsApp Image 2026-02-27 at 11 26 25 PM](https://github.com/user-attachments/assets/ce1c79f0-6df3-4128-880d-89ec9e27960e)

A relay can be controlled remotely using HTTP commands:

/ledon

/ledoff

The system also displays WiFi status and relay state on a 16x2 I2C LCD.

🛠 Hardware Used

STM32F411 (Nucleo)

ESP8266 WiFi Module

5V Relay Module (Active Low)

16x2 I2C LCD

3.3V Supply for ESP8266

💻 Software & Concepts

Embedded C

Register-level STM32 programming

UART Interrupt Communication

Circular Buffer

AT Command Handling

HTTP Request Parsing

I2C LCD Interface

⚙️ How It Works

STM32 initializes UART, LCD, and GPIO.

ESP8266 connects to WiFi using AT commands.

ESP8266 starts a server on port 80.

When a browser sends:

http://<ESP_IP>/ledon → Relay turns ON

http://<ESP_IP>/ledoff → Relay turns OFF

LCD updates the relay status.

If WiFi disconnects, system automatically reconnects.

📡 Key Features

Interrupt-based UART reception

Non-blocking circular buffer

Automatic WiFi reconnection

Relay control via HTTP

Real-time LCD status display

PC debug output via UART2

📂 Project Structure
Core/
Drivers/
Src/
Inc/
main.c
STM32F411.ioc
README.md

🎯 Learning Outcomes

STM32 peripheral configuration

UART interrupt design

ESP8266 AT command communication

Basic IoT system integration

Embedded string parsing

👨‍💻 Author

Huday Kiran
Embedded Systems Developer

This version is:

Clean ✅

Easy to read ✅

Professional for recruiters ✅

Not overloaded with too much code explanation ✅
