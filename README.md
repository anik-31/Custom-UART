# 🛠️ STM32 UART Communication with FreeRTOS

This project demonstrates how to use FreeRTOS on an STM32F4 microcontroller to handle UART communication. It implements tasks for transmitting and receiving data using the UART peripheral, ensuring thread safety with a mutex.

---

## 📂 Project Structure
.
├── Core
│ ├── Inc # Header files
│ ├── Src # Source files
│ │ └── main.c # Main application
│ └── Startup # Startup files
├── Drivers # HAL Drivers
├── .gitignore # Git ignore file
└── README.md # This file

---

## 📝 Features

- **UART Communication:** Handles UART transmit and receive operations.
- **FreeRTOS Tasks:**
  - **TransmitTask:** Periodically sends data over UART.
  - **ReceiveTask:** Processes received data and echoes back non-ACK messages.
- **Thread Safety:** Ensures UART operations are thread-safe using a FreeRTOS mutex.
- **Message Parsing:** Captures and processes messages terminated by `\n`.

---

## 🚀 How It Works

### 🛠️ System Configuration

#### UART Configuration:
- **Peripheral:** USART1
- **Baud Rate:** 9600 bps
- **Data Bits:** 8
- **Stop Bits:** 1
- **Parity:** None
- **Flow Control:** None

#### FreeRTOS Configuration:
- **Tasks:**
  - `TransmitTask`: Sends "Hello from TransmitTask!" every 1 second.
  - `ReceiveTask`: Reads incoming UART data, processes it, and sends a formatted response.
- **Mutex:** Ensures that UART transmit and receive operations are not interrupted.

### 🔧 UART Functions

#### `UART_Transmit(char *data)`
- Sends a string over UART with mutex protection.

#### `UART_Receive(void)`
- Receives a single character from UART with mutex protection.

---

## 🔍 Code Walkthrough

### 🛠️ Key Functions

#### `TransmitTask`
- Sends a periodic message over UART.
- Ensures transmission is thread-safe using the mutex.

#### `ReceiveTask`
- Continuously listens for incoming UART data.
- Buffers received bytes until a newline (`\n`) or buffer overflow.
- Processes complete messages:
  - If the message is not an "ACK", it echoes the complete message.

---

## 🛠️ Usage

1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo/stm32-uart-freertos.git
2. Open the project in your STM32 IDE (e.g., STM32CubeIDE).
3. Configure your UART connection on USART1 pins:
4. PA9 (TX): UART transmit
5. PA10 (RX): UART receive
6. Flash the firmware onto your STM32 board.
7. Use a serial terminal (e.g., TeraTerm, minicom) to observe UART communication.

💡 Additional Notes
Adjust UART_BAUDRATE or other UART settings if needed for your setup.

Ensure FreeRTOS is properly configured in your project.

| Icon | Description                       |
| ---- | --------------------------------- |
| 🛠️  | Code or functionality explanation |
| 🔧   | Configuration details             |
| 🚀   | How to run the project            |
| 📂   | File structure overview           |
