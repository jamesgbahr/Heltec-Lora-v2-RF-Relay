# **Heltec LoRa V2 RF Relay**

This project utilizes the Heltec WiFi LoRa 32 V2 development board to control relays via LoRa communication. It's ideal for applications requiring long-range wireless control, such as remote switching systems and IoT deployments.

## Features

- **LoRa Communication**: Employs the SX1276 LoRa transceiver for long-range, low-power wireless communication.
- **Relay Control**: Manages relays to switch devices on or off remotely.
- **OLED Display**: Includes a 0.96-inch OLED screen for real-time status updates.
- **ESP32 Microcontroller**: Offers Wi-Fi and Bluetooth capabilities alongside LoRa, enhancing connectivity options.

## Components Required

- Two Heltec WiFi LoRa 32 V2 Boards
- Relay modules compatible with ESP32 GPIO pins
- Connecting wires
- Power supply

## Setup Instructions

### 1. Hardware Assembly

- **Soldering**: Attach pin headers to the Heltec boards if not pre-soldered. Be cautious not to damage the ribbon cable connecting the board to the OLED.
- **Connections**:
  - Connect the relay module's control inputs to the appropriate GPIO pins on the Heltec board.
  - Ensure the relay module is powered correctly, matching its voltage requirements.

### 2. Arduino IDE Configuration

- **Board Setup**:
  - Install the Heltec ESP32 board package in the Arduino IDE.
  - Select 'WiFi LoRa 32 (V2)' from the Tools > Board menu.
- **Library Installation**:
  - Install necessary libraries such as `Heltec ESP32` and `LoRa`.
- **Code Upload**:
  - Open the transmitter and receiver sketches provided by Heltec.
  - Modify the frequency settings to comply with your region's regulations.
  - Upload the respective sketches to each Heltec board.

### 3. Relay Control Logic

- Program the receiver board to activate or deactivate relays based on received LoRa messages.
- Implement safety features, such as a failsafe mechanism to turn off relays if communication is lost.

## Usage

- **Transmitter**: Sends control commands via LoRa to the receiver.
- **Receiver**: Receives LoRa messages and controls the relays accordingly.
- **OLED Display**: Shows the current status of the relays and connection information.

## Troubleshooting

- **No LoRa Communication**:
  - Verify that both boards are set to the same frequency and spreading factor.
  - Ensure antennas are properly connected to avoid damaging the LoRa transceiver.
- **Relay Malfunction**:
  - Check the GPIO pin assignments and ensure they match your hardware setup.
  - Confirm that the relay module is receiving adequate power.

## Additional Resources

- [Heltec WiFi LoRa 32 V2 Documentation](https://resource.heltec.cn/download/WiFi_LoRa_32/WiFi%20Lora32.pdf)
- [Heltec ESP32 Arduino Library](https://github.com/HelTecAutomation/Heltec_ESP32)

## License

This project is licensed under the MIT License.

## Contributions

Contributions are welcome! Feel free to open an issue or submit a pull request.
