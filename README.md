# Custom UART Communication

This repository demonstrates the implementation of a **Custom UART Communication Protocol** between an **STM32** and an **ESP32**, showcasing bidirectional data exchange with driver-level coding. It highlights embedded systems development and communication protocol handling.

---

## Features

- **Custom UART Communication**:
  - Enables seamless data transmission between STM32 and ESP32.

- **Driver Development**:
  - Implements low-level UART communication routines for both devices.

- **Bidirectional Data Exchange**:
  - Demonstrates sending and receiving commands between STM32 and ESP32.

---

## Installation

### Prerequisites

1. **Hardware**:
   - STM32 (e.g., STM32F407)
   - ESP32 (e.g., ESP32 WROVER-IB)
   - USB-to-Serial adapters (if required for debugging)

2. **Software**:
   - STM32CubeIDE (for STM32 code)
   - PlatformIO or Arduino IDE (for ESP32 code)

3. **Wiring**:
   - Connect TX (STM32) to RX (ESP32) and RX (STM32) to TX (ESP32).
   - Ensure both devices share a common ground.

### Setting Up

1. Clone the repository:
   ```bash
   git clone https://github.com/anik-31/Custom-UART.git
   cd Custom-UART
   ```

2. Upload the ESP32 code:
   - Navigate to the `ESP32/` folder.
   - Use PlatformIO or Arduino IDE to upload the code to the ESP32.

3. Upload the STM32 code:
   - Navigate to the `STM32/` folder.
   - Open the project in STM32CubeIDE and upload it to the STM32.

---

## Usage

1. Power up the STM32 and ESP32.
2. Monitor UART communication using Serial Monitor or debugging tools.
3. Observe the data exchange and protocol responses between STM32 and ESP32.

---

## Project Structure

```
Custom-UART/
├── STM32/                   # STM32 code
├── ESP32/                   # ESP32 code
├── README.md                # Project documentation
└── LICENSE                  # License information
```

---

## Results

- Successfully implemented UART communication between STM32 and ESP32.
- Verified bidirectional data transfer through debugging and testing.

---

## Technologies Used

- **Hardware**: STM32, ESP32
- **Programming Languages**: Embedded C
- **Tools**: STM32CubeIDE, PlatformIO, Serial Monitor

---

## Future Work

- Optimize UART communication for higher baud rates.
- Add error handling for scenarios like buffer overflow and transmission delays.
- Expand to include additional features such as CRC error-checking.

---

## Contributing

Contributions are welcome! Fork the repository, make your changes, and submit a pull request.

---



---

## Contact

For questions or suggestions, please contact **anik-31** via [GitHub Issues](https://github.com/anik-31/Custom-UART/issues).
