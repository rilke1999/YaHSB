# YaHSB
Yet Another Highend Switch  Box
## Project Goal
Fully balanced switching box with level adjustment for the automated blind test of 4 sources, 3 amplifiers, and 3 pairs of speakers.

## Motivation
My old mechanical switching box that I built 20 years ago is not symmetrical, and the level adjustment is only manual and with manual measurement. Moreover, it is only non balanced.

## License Condition
The developed hardware and software are open and free to use. Possibly under the MIT public license?

## Team
Appreciative and open minded.

## Documentation
GitHub (those unfamiliar with it will be taught, it's not rocket science).

## Language
Depending on the team, English or German (thanks to AI, this is no longer a problem today).

## PCB Layout
KiCAD 8

## Mechanical CAD
Freecad
## Basic Idea

```mermaid
graph TD;
    A[Controller/PSU] --> BL[SwitchingSlave Left]
    A --> BR[SwitchingSlave Right]

    BL --> BL_inp1[inp1]
    BL --> BL_inp2[inp2]
    BL --> BL_inp3[inp3]
    BL --> BL_inp4[inp4]
    BL --> BL_SPKin1[SPKin1]
    BL --> BL_SPKin2[SPKin2]
    BL --> BL_SPKin3[SPKin3]
    BL --> BL_out1[out1]
    BL --> BL_out2[out2]
    BL --> BL_out3[out3]
    BL --> BL_SPKout1[SPKout1]
    BL --> BL_SPKout2[SPKout2]
    BL --> BL_SPKout3[SPKout3]

    BR --> BR_inp1[inp1]
    BR --> BR_inp2[inp2]
    BR --> BR_inp3[inp3]
    BR --> BR_inp4[inp4]
    BR --> BR_SPKin1[SPKin1]
    BR --> BR_SPKin2[SPKin2]
    BR --> BR_SPKin3[SPKin3]
    BR --> BR_out1[out1]
    BR --> BR_out2[out2]
    BR --> BR_out3[out3]
    BR --> BR_SPKout1[SPKout1]
    BR --> BR_SPKout2[SPKout2]
    BR --> BR_SPKout3[SPKout3]


```
## Brainstorming on Features

- 2 x 4 Inputs Balanced 
- 2 x 3 Outputs Balanced
- 2 x 3 Input Speaker 
- 2 x 3 Output Speaker
- Level attenuation programmable (can be bridged)
- Output Buffer can be configured into the signal path
- Synchronize test process with participant questionnaire
- Preamp mode
- Modules (can but do not have to be built separately)
  - PSU Analog
  - PSU Digital
  - MCU & Display & Hardware UI
  - Volume Leveling Hardware
  - Source Selector Input
  - Sink Selector Output to AMPS
  - AMP Selector Speaker
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
```json
{
    "PathName": "TextDescription of path",
    "Channels": {
        "L": {
            "Input": "inp1",
            "Input_desc" : "TextDescription of Input",   
            "Buffer": "Yes",
            "Level Adjustment": "-x DB",
            "Output": "out1",
            "Output_desc" : "TextDescription of Output",
            "SPKin" : "SPKin1",
            "SPKin_desc" : "TextDescription of Speaker_in",
            "SPKout": "SPKout1"
            "SPKout_desc" : "TextDescription of Speaker_out",
            },
        "R": {
            "Input": "inp1",
            "Input_desc" : "Bricasti M12",
            "Buffer": "No",
            "Level Adjustment": "-12 DB",
            "Output": "out1",
            "Output_desc" : "McIntosh MC275",
            "SPKin" : "SPKin1",
            "SPKin_desc" : "4 Ohm Output MC275",
            "SPKout": "SPKout1"
            "SPKout_desc" : "Magico Q5",
            }
  }
}
```

### Configuration Test Source Signal
Here we Define the source of the test signals. In case of beeing Digital they can be trigger via a UPNP Playlist, or via a Playlist in roon.
- UPNP control [endpoint / playlist]
- Roon API [endpoint / playlist]
- Manual for non streaming content.

### Automatic Volume Leveling
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
