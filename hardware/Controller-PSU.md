The whole setup should be flexible enough to control either dedicated preamp modules, the YahSB modules (which can also be misused as VV), or even intelligent prepare modules.

In concept, similar to the Pass XP32 control unit but more flexible.

**Control Unit and Power Supply:**

- 1 or optionally 2 Cap Multiplier Regulated PSU with ± 15-18V
- 1 PSU for Digital and Relays 3.3V and 5V, possibly 12V for Trigger
- Controller board with MCU (STM32 or ESP32S3)
  - STM32 is somehow cooler, but I am more familiar with ESP32
- Each with I2C bus and SPI 3 wire (for flexibility with an additional CS) for the modules to be controlled
- 2 rotary encoders with switch
- Graphical display approx 3”
- External WiFi antenna (optional)
- Hardware for connecting a measurement microphone for level measurement
- Possibly test signal generation
- Open Hardware

**Software:**

- YahSB Mode (yet another high-end switch box)
  - Web config of blind A/B tests
  - Integration into a cloud-based questionnaire tool for participants of blind tests
- Preamp Mode (normal preamplifier operation)
- Configurable and modularly expandable
- Update via USB or WiFi
- Open Source
