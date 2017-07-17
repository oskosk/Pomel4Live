# Pomel4Live

Everything related to the Pomel4Live custom MIDI Controller

### What is Pomel4Live

**Pomel4Live** is a custom MIDI controller developed by my wife, Malena. While she was guided and assisted in the construction by [Yaeltex](https://github.com/Yaeltex) as part of the proposed tasks of the [MIDI controller workshop](https://yaeltex.com/tcmidi1-inscripcion/), the controls design and layout was designed by her to suit her needs as a frequent user of DAWs for producing and designing for Theater Plays.



### Controller  overview

Pomel4Live's design is very opinionated and resembles a simple 4 channel mixer. Its main purpose is to controller a specific and reduced set of the [Propellerheads Reason Main Section] controls. Specifically, channellevels, FX returns, and FX Sends.

| <img src="https://user-images.githubusercontent.com/746152/28279616-6a8c1c92-6af7-11e7-954d-d65c3003bdbf.jpg" width=300 /> | <img src="https://user-images.githubusercontent.com/746152/28279909-5fc2b766-6af8-11e7-9ab7-bbc90250f088.jpg" width=300 /> |
|:---:|:---:|
| **Pomel4Live MIDI Controller**| **Pomel4Live MIDI Controller - Front** |

### Controls in the Pomel4Live controller

The controller consists of a few faders, buttons and knobs mainly. Specifically:

* 4 Faders
* 2 main knobs (meant to control something on which the other buttons will depend as FX return levels)
* 8 child knobs (meant to control two things by channel )
* 8 Buttons (meant to control two things by channel)
* A distance sensor. Not specifically used by her.
* Distance Sensor toggle. Enables or disables the distance sensor.


#### Specific purpose

The basic idea was that the two Main knobs (**Knob a** and **Knob b**) were going to handle the Return Level of just two Effect (FXs). The 4 faders would handle the levels of the first 4 channels. The two buttons before each fader would mute or solo the channel. And the knobs labeled a1, b1, a[x], b[x] would handle the Send level of the channel to Effect a and Effect b.

The *Distance Sensor* in the controller was more a Proof of Concept of the variety of interactions that can be mapped to a MIDI interface, than anything else. So it never had a definitive purpose associated. The button to the left of the **Distance Sensor** is meant to toggle the Sensor on or off.


#### Specific purpos in Reason

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

During the workshop, to Ableton Live users where guided by .
So while creating the controller, there was some guidance to those users in order to create
The Ableton Live Automation scripts for the controller but not so much for Reason users..

A few days ago, we decided to revamp the controller and give it a try to make it work seamlessly with Reason without the need to remap the remote controls each time Malena needed to work on a new project.

### Reason Support Files

* Codec File
  * Pomel4Live.midicodec
* Map File
  * Pomel4Live.mapmidi
  
