# Pomel4Live

Everything related to the **Pomel4Live** custom MIDI Controller

* [What is Pomel4Live](#what-is-pomel4live)
* [Controller overview](#controller-overview)
  * [Controls by channel](#controls-by-channel)
* [Usage with Reason](#usage-with-reason)
  * [Reason Support Files](#reason-support-files)
  * [Installation](#reason-support-files-installation)
  * [Pomel4Live's Default Remote Mapping in Reason](#pomel4lives-default-remote-mapping-in-reason)
  * [Customizing the mapping](#customizing-the-mapping)
* [Pomel4Live controls MIDI values](#pomel4live-controls-midi-values)
* [License](#license)

### What is Pomel4Live

**Pomel4Live** is a custom MIDI controller developed by Malena Graciosi. While she was guided and assisted in the construction by [Yaeltex](https://github.com/Yaeltex) during the [MIDI controller workshop](https://yaeltex.com/tcmidi1-inscripcion/), the controls were designed by Malena to suit her needs as a frequent user of the [Reason DAW](https://www.reasonstudios.com/reason) for [producing and designing sound for theater plays](http://www.alternativateatral.com/persona5802-malena-graciosi).

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

**Pomel4Live** has a default mapping for Reason. To use it, install the Reason support files. Refer to the [installation procedure](#reason-support-files-installation).

#### Reason Support Files

The [`Pomel4Live - Reason Support Files`](Pomel4Live%20-%20Reason%20Support%20Files) folder contains three support files. The structure of this folder is the same as the structure of the Reason Remote folder.

| File | Folder | Function |
|---|---|---|
| [Pomel4Live.midicodec](Pomel4Live%20-%20Reason%20Support%20Files/Codecs/MIDI%20Codecs/Pomel4Live.midicodec) | `Codecs/MIDI Codecs/` | Tells Reason the controls of Pomel4Live and the MIDI messages that they send |
| [Pomel4Live.png](Pomel4Live%20-%20Reason%20Support%20Files/Codecs/MIDI%20Codecs/Pomel4Live.png) | `Codecs/MIDI Codecs/` | The picture that Reason shows in the Control Surfaces preferences |
| [Pomel4Live.remotemap](Pomel4Live%20-%20Reason%20Support%20Files/Maps/Malena%20Graciosi/Pomel4Live.remotemap) | `Maps/Malena Graciosi/` | Connects the controls to the Reason Master Section |

#### Reason Support Files Installation

1. Quit Reason.
1. Find the Reason Remote folder. The location of this folder changes with the Reason version. Use one of these locations:
   * macOS: `~/Library/Application Support/Propellerhead Software/Remote/` or `~/Library/Application Support/Reason Studios/Remote/`
   * Windows: `%APPDATA%\Propellerhead Software\Remote\` or `%APPDATA%\Reason Studios\Remote\`

   > **CAUTION:** If the Remote folder already has a `Codecs` folder or a `Maps` folder, merge the folders. Do not replace them. If you replace them, you remove the support files of your other control surfaces.

1. Copy the `Codecs` folder and the `Maps` folder from `Pomel4Live - Reason Support Files` into the Remote folder.
1. Connect Pomel4Live to the computer.
1. Start Reason.
1. Open the Preferences window:
   * macOS: Select **Reason > Preferences**.
   * Windows: Select **Edit > Preferences**.
1. Select **Control Surfaces**.
1. Click **Auto-detect Surfaces**.
1. If Reason does not find Pomel4Live, do these steps:
   1. Click **Add manually**.
   1. Select the manufacturer **Malena Graciosi** and the model **Pomel4Live**.
   1. Select the MIDI input of Pomel4Live.
1. Select **Options > Surface Locking...**.
1. Select **Pomel4Live** and lock it to the **Master Section** device.

   > **NOTE:** If you do not lock Pomel4Live, it controls the device that you select in the rack.

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

Support file versions: codec 1.0.1, map 1.1.0. These files are from 2017. We did not test them with newer Reason versions.

#### Customizing the mapping

The [Pomel4Live.remotemap](Pomel4Live%20-%20Reason%20Support%20Files/Maps/Malena%20Graciosi/Pomel4Live.remotemap) file contains the mapping. Each `Map` line has this format:

```
Map	<Control name>		<Reason remotable item>
```

Use tab characters between the fields. The control name must be the same as an `Item` name in [Pomel4Live.midicodec](Pomel4Live%20-%20Reason%20Support%20Files/Codecs/MIDI%20Codecs/Pomel4Live.midicodec).

To change the mapping:

1. Quit Reason.
1. Open the installed copy of `Pomel4Live.remotemap` in a text editor. This copy is in the `Maps/Malena Graciosi/` folder of the Reason Remote folder.
1. Add or change `Map` lines. For example, this line connects the distance sensor to the FX3 return level:

   ```
   Map	Distance Sensor Fader		FX3 Return Level
   ```

1. To control a different device, add a `Scope` section for that device.
1. Save the file.
1. Start Reason.

For the file format and the names of the remotable items of each device, refer to the Reason Remote SDK and the *Remote Info* documents that Reason supplies.


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

### License

[MIT](LICENSE)
