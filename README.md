# YaHSB
Yet Another Highend Switch  Box
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


## Specifications

- 2 x 4 Inputs Balanced 
- 2 x 3 Outputs Balanced
- 2 x 3 Input Speaker
- 2 x 3 Output Speaker
- Level attenuation programmable (can it be turned off?)
- Output Buffer can be configured inthe signal path
- Synchronize test process with participant questionnaire
- Preamp mode
- Modules (can but do not have to be built separately)
  - PSU Analog
  - PSU Digital
  - MCU & Display & Hardware UI
  - Source Selector Input
  - Sink Selector Output
  - Optional: Buffer
  - Level Adjustment
  - Optional additional relay box for additional test scenarios

## Basic Requirements

- No Digital I/O with the slaves during listening
- Remotely configurable via IR / WiFi
- Online updates
- True Dual Mono possible
- Flexible preamp
- Open Source / Open Hardware (license type to be discussed)
- SMD where sensible, TH where necessary

## To be discussed

- Non balanced input / output

## User Stories Test Scenarios: (Idea generation unformatted)

### Definition Test Path

- Maximum 32 Cases
- [NAME TestCASE] Input XLR / Buffer? / Level Adjustment / Output XLR / Input AMP / Output AMP
  
  Configuration Elements:
    TestPathName : [A]
    Channel [L]  
      Input : [XLR_i_1]
      Buffer : [Yes / Now]
      Level Adjustment: [-x] DB
      Output : [XLR_o_1]
      AMP_OUT : [AMP 1]
      Speaker :[SPK_1]
    Channel [R]
      Input : [XLR_i_1]
      Buffer : [Yes / Now]
      Level Adjustment: [-x] DB
      Output : [XLR_o_1]
      AMP_OUT : [AMP 1]
      Speaker :[SPK_1]


### Configuration Test Source Signal
Here we Define the source of the test signals. In case of beeing Digital they can be trigger via a UPNP Playlist, or via a Playlist in roon.
- UPNP control [endpoint / playlist]
- Roon API [endpoint / playlist]
- Manual for non streaming content.

### Test Scenarios

- AMP Test
- Speaker Test
- Source Test

### Test Process

- BLIND Scenario [1,2,3---]
- Include obfuscation by different volume levels
- Manually Switched
- Online questionnaire during the test

## Project Milestones

- End of March 2024: Final specification
- End of June 2024: Circuit diagram stable
- End of September 2024: RC1 of the PCB
- End of November 2024: Practical test

Is anyone interested?
