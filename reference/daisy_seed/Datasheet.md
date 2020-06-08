# Daisy Seed

Datasheet Version v0.1

Technical Overview of the Daisy Seed

## Electrical Characteristics

Recommended Operating Ranges

| Pin type    | Min | Max | Unit |
| --------    | --- | --- | ---- |
| VIN Range   | +4  | +17 | V    |
| ADC Input   | 0   | +3.3 | V   |
| DAC Output  | 0   | +3.3 | V   |
| GPIO Output | 0   | +3.3 | V   |
| GPIO Input  | 0   | +3.3 | V   |

## Power Pins

These pins should be used only for their specified purpose. 

### Pin 39 - VIN

VIN is a DC voltage input that can be used instead of powering the Daisy via USB.

This voltage must be between +4V and +17V

### Pin 40 - DGND

Digital Ground pin. 

Should be connected to AGND outside of Daisy submodule.

### Pin 20 - AGND

Analog Ground pin.

Should be connected to DGND outside of Daisy submodule.

### Pin 38 - 3v3 Digital

+3v3 digital supply output.

Available current dependent on firmware running on the Daisy. 

Maximum 500mA total combined with MCU/RAM.

### Pin 21 - 3v3 Analog

+3v3 analog supply output.

Available Current TBD **TODO ADD Current**

Maximum 150mA combined with onboard-AK4556 and Analog section of MCU.

## Audio Pins

Line Level, AC Coupled analog audio

Audio will begin to clip when input or output signal approach 3Vpp

For line level audio, the pins can be connected directly to jacks, etc.

## Analog GPIO Pins

### ADCs (Analog Inputs)

Pins 22-32 and 35 can be used as Analog Inputs (with configurable bitdepth up to 16-bits)

Input range:

- 0V to +3V3

### DACs (Analog Outputs)

Pins 29 and 30 can be configured as Analog Outputs (with configurable bitdepth up to 12-bits)

Output code 0x000 (0) correlates to 0V

Output code 0xFFF (4095) correlates to 3V3_A

## Digital GPIO Pins

All other Peripheral GPIO (including the Digital Audio GPIO shown in the pinout diagram) are functionally the same.

When configured as input each pin can configure an internal pull-up, pull-down, or no pull resitor.

When configured as an output each pin can be configured for push-pull or open-drain configuration

I/O levels should be kept between 0V and 3V3

All GPIO Pins are 5V tolerant. **Double check this, there are a few 3v3 tolerant pins on the MCU**

# Datasheet Changelog

### v0.1

- Added initial documentation for voltage ranges, and pin descriptions.
