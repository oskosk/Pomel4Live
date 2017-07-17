# Pomel4Live

Everything related to the Pomel4Live custom MIDI Controller

### What is Pomel4Live

**Pomel4Live** is a custom MIDI controller developed by my wife, Malena. While she was guided and assisted in the construction by [Yaeltex](https://github.com/Yaeltex) during the [MIDI controller workshop](https://yaeltex.com/tcmidi1-inscripcion/), the controls were thought by Malena to suit her needs as a frequent user of the [Reason DAW](https://www.propellerheads.se/en/reason) for [producing and designing Sound for Theater Plays](http://www.alternativateatral.com/persona5802-malena-graciosi).


### Controller  overview

The design of the **Pomel4Live** MIDI controller is very opinionated and resembles a simple 4 channel mixer with two faders, two knobs and two buttons for each channel. Its main purpose is to control a specific and reduced set of Reason remotable items of the Main Section. Specifically, Channel Levels, Channel Effect Send Levels and Effect Return Levels.

| <img src="https://user-images.githubusercontent.com/746152/28279616-6a8c1c92-6af7-11e7-954d-d65c3003bdbf.jpg" width=300 /> | <img src="https://user-images.githubusercontent.com/746152/28279909-5fc2b766-6af8-11e7-9ab7-bbc90250f088.jpg" width=300 /> |
|:---:|:---:|
| **Pomel4Live MIDI Controller**| **Pomel4Live MIDI Controller - Front** |

#### Specific purpose of the controls

The basic idea was that the two Main knobs (**Knob a** and **Knob b**) were going to handle the Return Level of the first two Effect (FXs). The 4 faders would handle the levels of the first 4 channels. The two buttons before each fader would mute or solo the channel. And the knobs labeled a1, b1, a[x], b[x] would handle the Send level of the channel to Effect a and Effect b.

The *Distance Sensor* in the controller was more a Proof of Concept of the variety of interactions that can be mapped to a MIDI interface, than anything else. So it never had a definitive purpose associated. The button to the left of the **Distance Sensor** is meant to toggle the Sensor on or off.

#### Controls in the Pomel4Live controller

The controller consists of a few faders, buttons and knobs mainly. Specifically:

* 4 Channel Level Faders - Each to be associated with one of the first 4 channels.
* 8 Mute/Sollo Buttons - Meant to mute or solo each of the 4 channels.
* 8 Send Level knobs - Meant to control the Send Level of each of the 4 channels to each of the two Effects.
* 2 Effect level knobs - Each to be associated with the Return Level of the first two Effects.
* A distance sensor. Not specifically used.
* A Distance Sensor Toggle. A button that enables or disables the distance sensor.

#### Pomel4Live's Default Remote Mapping in Reason

| Control | Reason function | Reason device |
|:---:|:---:|:---:|
| Button a | controls FX 1 Return Level | Main Section |
| Button b | controls FX 2 Return Level | Main Section |
| Knob a1 | controls FX 1 Send Level for Channel 1 | Main Section |
| Knob b1 | controls FX 2 Send Level for Channel 1 | Main Section |
| Knob a2 | controls FX 1 Send Level for Channel 2 | Main Section |
| Knob b2 | controls FX 2 Send Level for Channel 2 | Main Section |
| Knob a3 | controls FX 1 Send Level for Channel 3 | Main Section |
| Knob b3 | controls FX 2 Send Level for Channel 3 | Main Section |
| Knob a4 | controls FX 1 Send Level for Channel 4 | Main Section |
| Knob b4 | controls FX 2 Send Level for Channel 4 | Main Section |
| Button 1 | Mutes Channel 1 | Main Section |
| Button 2 | Soloes Channel 1 | Main Section |
| Button 3 | Mutes Channel 2 | Main Section |
| Button 4 | Soloes Channel 2 | Main Section |
| Button 5 | Mutes Channel 3 | Main Section |
| Button 6 | Soloes Channel 3 | Main Section |
| Button 7 | Mutes Channel 4 | Main Section |
| Button 8 | Soloes Channel 4 | Main Section |
| Fader 1 | controls Level for Channel 1 | Main Section |
| Fader 2 | controls Level for Channel 2 | Main Section |
| Fader 3 | controls Level for Channel 3 | Main Section |
| Fader 4 | controls Level for Channel 4 | Main Section |
| Distance Sensor | Nothing currently. Probably best used as a modulator | |
| Distance Sensor Toggle | Enables or disables the distance sensor | No Reason device |

## Usage with Reason

During the workshop, The attendees who were Ableton Live users where guided by the crew in order to generate the specific [Control Surface Scripts](https://help.ableton.com/hc/en-us/articles/206240184-Creating-your-own-Control-Surface-script) for the Ableton Live DAW. But there was not so much focus in the Reason software, so the Remote Scripts for **Pomel4Live** and Propellerheads Reason were never created.

A few days ago, we decided to revamp the controller and give it a try to make it work seamlessly with Reason without the need to remap the remote controls each time Malena needed to work on a new project and after this, I'm creating the repository to publish them.

### Reason Support Files

* Codec File
  * Pomel4Live.midicodec
* Map File
  * Pomel4Live.mapmidi
  
