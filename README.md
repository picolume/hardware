# PicoLume Hardware

Hardware designs for the PicoLume wireless LED prop system. All designs are created in KiCad.

## Design Series

### series-prop (Primary)

The primary hardware design for production use. Contains the **PicoLume Board** - a compact control board designed to be installed on each prop in a synchronized LED light show.

**Current Design: receiver-v1**

An RP2040-based control board featuring:

- RP2040 microcontroller with 16MB flash (W25Q16JVS)
- RFM69HCW radio module (915 MHz) for wireless timecode reception
- USB-C connector for programming and show file upload
- Dual power input with automatic switching (LM66200)
- 5V buck converter (AP63205WU) for LED strip power
- Pinout for 0.91" OLED display (I2C)
- Screw terminals for LED strip connection (WS2812B)
- Level shifter (74AHCT1G125) for reliable LED data signal
- Three tactile buttons for configuration
- Onboard WS2812B status LED
- Four M3 mounting holes

The PicoLume Board is the core control component. A complete receiver or transmitter setup requires additional hardware (enclosures, power supplies, antennas, etc.) which are currently being designed.

### series-legacy (Prototypes)

Early prototype designs from the development phase. These boards were used for proof-of-concept testing and firmware development.

**Note:** These designs are prototypes and are not suited for production use.

| Version | Description                   |
| ------- | ----------------------------- |
| v1      | Initial RFM69-based design    |
| v2      | RP2040 with Pi Pico footprint |
| v3      | Refined RP2040 design         |
| v4      | RP2350 Experiment             |

## Related Repositories

- **firmware/** - Arduino firmware for receiver and remote devices

## License

See [LICENSE](LICENSE) for details.
