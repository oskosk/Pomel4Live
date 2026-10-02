# Pomel4Live

Everything related to the **Pomel4Live** custom MIDI Controller

* [Usage with Reason](#usage-with-reason)
  * [Installation](#reason-support-files-installation)
  * [Pomel4Live's Default Remote Mapping in Reason](#pomel4lives-default-remote-mapping-in-reason)
  * [Reason Support Files](#reason-support-files)
* [Pomel4Live controls MIDI values](#pomel4live-controls-midi-values)

### What is Pomel4Live

**Pomel4Live** is a custom MIDI controller developed by my wife, Malena. While she was guided and assisted in the construction by [Yaeltex](https://github.com/Yaeltex) during the [MIDI controller workshop](https://yaeltex.com/tcmidi1-inscripcion/), the controls were designed by Malena to suit her needs as a frequent user of the [Reason DAW](https://www.reasonstudios.com/reason) for [producing and designing sound for theater plays](http://www.alternativateatral.com/persona5802-malena-graciosi).

During the workshop, the attendees who were Ableton Live users were guided by the crew to create the specific [Control Surface Scripts](https://help.ableton.com/hc/en-us/articles/206240184-Creating-your-own-Control-Surface-script) for the Ableton Live DAW. There was less focus on Reason, so Remote files for **Pomel4Live** and Reason were never created.

In July 2017 we revamped the controller to make it work with Reason out of the box, so Malena no longer had to remap the controls for every new project. This repository publishes the resulting Remote files.

### Controller overview

The design of the **Pomel4Live** MIDI controller is very opinionated and resembles a simple 4-channel mixer with a fader, two knobs and two buttons for each channel. Its main purpose is to control a small set of remotable items of Reason's Master Section: channel levels, channel effect send levels and effect return levels.

| <img src="https://user-images.githubusercontent.com/746152/28279616-6a8c1c92-6af7-11e7-954d-d65c3003bdbf.jpg" width=300 /> | <img src="https://user-images.githubusercontent.com/746152/28279909-5fc2b766-6af8-11e7-9ab7-bbc90250f088.jpg" width=300 /> |
|:---:|:---:|
| **Pomel4Live MIDI Controller**| **Pomel4Live MIDI Controller - Front** |

#### Specific purpose of the controls

The basic idea was that the two Main knobs (**Knob a** and **Knob b**) handle the return levels of the first two effects (FX1 and FX2). The 4 faders handle the levels of the first 4 channels. The two buttons before each fader mute or solo the channel. The knobs labeled a1–a4 and b1–b4 handle each channel's send level to FX1 and FX2.

The **Distance Sensor** in the controller is mostly a proof of concept of the variety of interactions that can be mapped to a MIDI interface, so it never had a definite purpose. Reason lists it as **Distance Sensor Fader**. The button to the left of the **Distance Sensor** is meant to toggle the Sensor on or off.

#### Controls in the Pomel4Live controller

The controller consists of:

* 4 Channel Level Faders - Each to be associated with one of the first 4 channels.
* 8 Mute/Solo Buttons - Meant to mute or solo each of the 4 channels.
* 8 Send Level knobs - Meant to control the Send Level of each of the 4 channels to each of the two Effects.
* 2 Effect level knobs - Each to be associated with the Return Level of the first two Effects.
* A Distance Sensor. Not currently mapped.
* A Distance Sensor Toggle. A button that enables or disables the distance sensor.

#### Controls by channel

Each of the four channel strips groups these controls:

| Channel | FX1 send | FX2 send | Mute | Solo | Level |
|:---:|:---:|:---:|:---:|:---:|:---:|
| 1 | Knob a1 | Knob b1 | Button 1 | Button 2 | Fader 1 |
| 2 | Knob a2 | Knob b2 | Button 3 | Button 4 | Fader 2 |
| 3 | Knob a3 | Knob b3 | Button 5 | Button 6 | Fader 3 |
| 4 | Knob a4 | Knob b4 | Button 7 | Button 8 | Fader 4 |

**Knob a** and **Knob b** sit outside the channel strips and control the FX1 and FX2 return levels.

### Usage with Reason

**Pomel4Live** works with a default mapping once its Reason support files are installed. Follow the [installation steps](#reason-support-files-installation).

#### Reason Support Files

The [`Pomel4Live - Reason Support Files`](Pomel4Live%20-%20Reason%20Support%20Files) folder contains three files, laid out the same way as Reason's Remote folder:

| File | Goes in | Purpose |
|---|---|---|
| [Pomel4Live.midicodec](Pomel4Live%20-%20Reason%20Support%20Files/Codecs/MIDI%20Codecs/Pomel4Live.midicodec) | `Codecs/MIDI Codecs/` | Describes the controls and the MIDI messages they send |
| [Pomel4Live.png](Pomel4Live%20-%20Reason%20Support%20Files/Codecs/MIDI%20Codecs/Pomel4Live.png) | `Codecs/MIDI Codecs/` | Thumbnail shown in Reason's Control Surfaces preferences |
| [Pomel4Live.remotemap](Pomel4Live%20-%20Reason%20Support%20Files/Maps/Malena%20Graciosi/Pomel4Live.remotemap) | `Maps/Malena Graciosi/` | Maps the controls to the Reason Master Section |

#### Reason Support Files Installation

1. Quit Reason.
1. Find Reason's Remote folder. Depending on your Reason version, it is one of:
   * macOS: `~/Library/Application Support/Propellerhead Software/Remote/` or `~/Library/Application Support/Reason Studios/Remote/`
   * Windows: `%APPDATA%\Propellerhead Software\Remote\` or `%APPDATA%\Reason Studios\Remote\`
1. Copy the `Codecs` and `Maps` folders from `Pomel4Live - Reason Support Files` into the Remote folder, merging them with any existing `Codecs` and `Maps` folders. Create the folders if they don't exist.
1. Connect **Pomel4Live** and start Reason.
1. Open Preferences (**Reason > Preferences** on macOS, **Edit > Preferences** on Windows), go to **Control Surfaces** and click **Auto-detect Surfaces**. If it isn't detected, click **Add manually** and choose manufacturer **Malena Graciosi**, model **Pomel4Live**, then select its MIDI input.
1. Lock the surface to the Master Section: open **Options > Surface Locking...**, select **Pomel4Live** and lock it to the **Master Section** device. Otherwise the surface follows whichever device is selected in the rack.

#### Pomel4Live's Default Remote Mapping in Reason

| Control | Reason function | Reason device |
|:---:|:---:|:---:|
| Knob a | FX1 Return Level | Reason Master Section |
| Knob b | FX2 Return Level | Reason Master Section |
| Knob a1 | Channel 1 FX1 Send Level | Reason Master Section |
| Knob b1 | Channel 1 FX2 Send Level | Reason Master Section |
| Knob a2 | Channel 2 FX1 Send Level | Reason Master Section |
| Knob b2 | Channel 2 FX2 Send Level | Reason Master Section |
| Knob a3 | Channel 3 FX1 Send Level | Reason Master Section |
| Knob b3 | Channel 3 FX2 Send Level | Reason Master Section |
| Knob a4 | Channel 4 FX1 Send Level | Reason Master Section |
| Knob b4 | Channel 4 FX2 Send Level | Reason Master Section |
| Button 1 | Channel 1 Mute | Reason Master Section |
| Button 2 | Channel 1 Solo | Reason Master Section |
| Button 3 | Channel 2 Mute | Reason Master Section |
| Button 4 | Channel 2 Solo | Reason Master Section |
| Button 5 | Channel 3 Mute | Reason Master Section |
| Button 6 | Channel 3 Solo | Reason Master Section |
| Button 7 | Channel 4 Mute | Reason Master Section |
| Button 8 | Channel 4 Solo | Reason Master Section |
| Fader 1 | Channel 1 Level | Reason Master Section |
| Fader 2 | Channel 2 Level | Reason Master Section |
| Fader 3 | Channel 3 Level | Reason Master Section |
| Fader 4 | Channel 4 Level | Reason Master Section |
| Distance Sensor | Nothing currently. Probably best used as a modulator | |
| Distance Sensor Toggle | Enables or disables the distance sensor | No Reason device |


### Pomel4Live controls MIDI values

All messages are sent on MIDI channel 1 (status bytes `B0` and `90`). The codec accepts them on any channel.

| Control | MIDI Values Hex | Note/Control |
|:---:|:---:|:---:|
| Distance Sensor | B0 64 | CC 100 |
| Knob a | B0 00 | CC 0 |
| Knob b | B0 01 | CC 1 |
| Knob a1 | B0 02 | CC 2 |
| Knob b1 | B0 03 | CC 3 |
| Knob a2 | B0 04 | CC 4 |
| Knob b2 | B0 05 | CC 5 |
| Knob a3 | B0 06 | CC 6 |
| Knob b3 | B0 07 | CC 7 |
| Knob a4 | B0 08 | CC 8 |
| Knob b4 | B0 09 | CC 9 |
| Button 1 | 90 00 | C-2 |
| Button 2 | 90 01 | C#-2 |
| Button 3 | 90 02 | D-2 |
| Button 4 | 90 03 | D#-2 |
| Button 5 | 90 04 | E-2 |
| Button 6 | 90 05 | F-2 |
| Button 7 | 90 06 | F#-2 |
| Button 8 | 90 07 | G-2 |
| Fader 1 | B0 0A | CC 10 |
| Fader 2 | B0 0B | CC 11 |
| Fader 3 | B0 0C | CC 12 |
| Fader 4 | B0 0D | CC 13 |
| Distance Sensor Toggle | Does not send a value | |
