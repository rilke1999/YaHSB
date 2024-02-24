# YaHSB
Yet Another Highend Switch Box
## Project Goal
Fully balanced switching box with level adjustment for the automated blind test of 2 sources, 2 amplifiers, and 2 pairs of speakers.

## Motivation
My old mechanical switching box that I built 20 years ago is not symmetrical, and the level adjustment is only manual and with manual measurement. Moreover, it is only non balanced.

## License Condition
The developed hardware and software are open and free to use. Possibly under the MIT public license?

## Team
Appreciative and open (anyone causing trouble is out).

## Documentation
GitHub (those unfamiliar with it will be taught, it's not rocket science).

## Language
Depending on the team, English or German (thanks to AI, this is no longer a problem today).

## PCB Layout
KiCAD 8

## Brainstorming on Features
(Completely open to ideas and changes)
- Completely symmetrical
- Mono design with central control to be able to place the switch directly near speakers or monoblocks. (Modular design)
- Central PSU and control unit with digital electronics
- 2 pairs of speakers via terminal connectors
- 2 XLR inputs
- 2 XLR outputs
- Optional: Trigger signal for turning on amplifiers
- Volume adjustment via MUSES 72323
- Optional: Input buffer switchable
- Optional: Automatic level measurement
- STM32 or ESP32S3 as controller (If control over web frontend, preferably ESP32)
- OLED display and 2 encoders for control
- Implementation of A/B blind test including documentation

## Project Milestones

- End of March 2024: Final specification
- End of June 2024: Circuit diagram stable
- End of September 2024: RC1 of the PCB
- End of November 2024: Practical test

Is anyone interested?
