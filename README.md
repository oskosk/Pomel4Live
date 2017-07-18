# Pomel4Live

Everything related to the **Pomel4Live** custom MIDI Controller

* [Usage with Reason](#usage-with-reason)
  * [Installation](#reason-support-files-installation)
  * [Pomel4Live's Default Remote Mapping in Reason](#pomel4lives-default-remote-mapping-in-reason)
  * [Reason Support Files](#reason-support-files)

### What is Pomel4Live

**Pomel4Live** is a custom MIDI controller developed by my wife, Malena. While she was guided and assisted in the construction by [Yaeltex](https://github.com/Yaeltex) during the [MIDI controller workshop](https://yaeltex.com/tcmidi1-inscripcion/), the controls were thought by Malena to suit her needs as a frequent user of the [Reason DAW](https://www.propellerheads.se/en/reason) for [producing and designing Sound for Theater Plays](http://www.alternativateatral.com/persona5802-malena-graciosi).

During the workshop, The attendees who were Ableton Live users where guided by the crew in order to generate the specific [Control Surface Scripts](https://help.ableton.com/hc/en-us/articles/206240184-Creating-your-own-Control-Surface-script) for the Ableton Live DAW. But there was not so much focus in the Reason software, so the Remote Scripts for **Pomel4Live** and Propellerheads Reason were never created.

A few days ago, we decided to revamp the controller and give it a try to make it work seamlessly with Reason without the need to remap the remote controls each time Malena needed to work on a new project and after this, I'm creating the repository to publish them.

### Controller  overview

The design of the **Pomel4Live** MIDI controller is very opinionated and resembles a simple 4 channel mixer with two faders, two knobs and two buttons for each channel. Its main purpose is to control a specific and reduced set of Reason remotable items of the Master Section. Specifically, Channel Levels, Channel Effect Send Levels and Effect Return Levels.

| <img src="https://user-images.githubusercontent.com/746152/28279616-6a8c1c92-6af7-11e7-954d-d65c3003bdbf.jpg" width=300 /> | <img src="https://user-images.githubusercontent.com/746152/28279909-5fc2b766-6af8-11e7-9ab7-bbc90250f088.jpg" width=300 /> |
|:---:|:---:|
| **Pomel4Live MIDI Controller**| **Pomel4Live MIDI Controller - Front** |

#### Specific purpose of the controls

The basic idea was that the two Main knobs (**Knob a** and **Knob b**) were going to handle the Return Level of the first two Effect (FXs). The 4 faders would handle the levels of the first 4 channels. The two buttons before each fader would mute or solo the channel. And the knobs labeled a1, b1, a[x], b[x] would handle the Send level of the channel to Effect a and Effect b.

The **Distance Sensor** in the controller was more a Proof of Concept of the variety of interactions that can be mapped to a MIDI interface, than anything else. So it never had a definitive purpose associated. The button to the left of the **Distance Sensor** is meant to toggle the Sensor on or off.

#### Controls in the Pomel4Live controller

The controller consists of a few faders, buttons and knobs mainly. Specifically:

* 4 Channel Level Faders - Each to be associated with one of the first 4 channels.
* 8 Mute/Sollo Buttons - Meant to mute or solo each of the 4 channels.
* 8 Send Level knobs - Meant to control the Send Level of each of the 4 channels to each of the two Effects.
* 2 Effect level knobs - Each to be associated with the Return Level of the first two Effects.
* A distance sensor. Not specifically used.
* A Distance Sensor Toggle. A button that enables or disables the distance sensor.

### Usage with Reason

**Pomel4Live** works in a default mapping if the proper setup is followed. For this, you need to follow the [installation steps](#reason-support-files-installation).


#### Reason Support Files

These files need to be copied into Reason specific folders. These are just three files

* The MIDI Codec File
  * [Pomel4Live - Reason Support Files/Codecs/MIDI Codecs/Pomel4Live.midicodec](https://raw.githubusercontent.com/oskosk/Pomel4Live/master/Pomel4Live%20-%20Reason%20Support%20Files/Codecs/MIDI%20Codecs/Pomel4Live.midicodec?token=AAtiqNGEjyNBwKrwL-hUZrxLgmkuQiEmks5Zd1UQwA%3D%3D)
* The Map File
  * [Pomel4Live - Reason Support Files/Maps/Malena Graciosi/Pomel4Live.remotemap](https://raw.githubusercontent.com/oskosk/Pomel4Live/master/Pomel4Live%20-%20Reason%20Support%20Files/Maps/Malena%20Graciosi/Pomel4Live.remotemap?token=AAtiqH_eIOZl232JWR3qhjSej7UgvT4kks5Zd1VOwA%3D%3D).
* The Pomel4Live thumbnail image
  * [Pomel4Live - Reason Support Files/Codecs/MIDI Codecs/Pomel4Live.png](https://github.com/oskosk/Pomel4Live/raw/master/Pomel4Live%20-%20Reason%20Support%20Files/Codecs/MIDI%20Codecs/Pomel4Live.png)

#### Reason Support Files Installation

1. Copy the MIDI codec files for **Pomel4Live**
1. Install the MIDI map files for **Pomel4Live**
1. Autodetect the Control Surface from Reason's Preferences.
1. Lock the surface to the **Reason Master Section**.

#### Pomel4Live's Default Remote Mapping in Reason

| Control | Reason function | Reason device |
|:---:|:---:|:---:|
| Button a | FX1 Return Level | Reason Master Section |
| Button b | FX2 Return Level | Reason Master Section |
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

  
