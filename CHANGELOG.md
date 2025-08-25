# Changelog

## [HW v1.1]
### Added
- Connected `CAL_ON` to `FMC HB20_N` and `J1C` pin 146.
- ADC offset control: added `AD5259` (digital pot; I²C) and `LP2998` (voltage divider).
- I²C expander `TCA9536` for managing `TX_TRIG_SEL`.
- Voltage monitoring `MAX11617` for FMC board.
- Control LEDs on the front panel.

### Fixed
- `I2C SDA/SCL_2V5` reswapped; `CLK_INPUT` block corrected.
- `PDN_GLB` removed from ports; now pulled down with resistor (no external control).
- Previously unconnected pads on connector tied to GND.
- Layout improvements:
  - Moved `INP31`/`INP27` vias away from `ADC_CLKA_P/N`; clock line routed closer to the board edge.
  - Updated `DOUT8B` length-tuning style on `L2` to reduce roll-up.
  - Increased separation between `DOUT8B` vias and `DOUT9B` serpentine.

### Removed
- Direct FPGA access to `TX_TRIG_SEL` (now handled via `TCA9536`).
- 
[HW v1.1]: https://github.com/elhep/FMC_ADC_128CH_10B/tree/v1.1
