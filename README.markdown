# The Ultimate Akai MPK Mini MK3 MIDI Remote Script for Ableton Live

Forked from [SlyBouhafs](https://github.com/SlyBouhafs/MMMKIII) for the sake of making
some personal preference tweaks.

## Usage

The *BANK B* of the first two programs mirrors the device program, enabling quick 
switching between device mappings using the BANK A/B button. Note that the "CC" pad
mode on the controller must be enabled to use the bindings this script adds to *BANK A*.

### Session
![Session](assets/images/SESSION.png)

### Arrangement
![Arrangement](assets/images/ARRANGEMENT.png)

### Mixer
![Mixer](assets/images/MIXER.png)

### Device
![Device](assets/images/DEVICE.png)

## Installation

First, clone the repository.

1.	Make sure that Live isn't running.
1.	In the `assets/presets/` folder, there are 4 programs, use the MPK Mini MK3 Program Editor to load each one.
1.	Add **mk3** to Ableton Live's MIDI Remote Scripts folder.

	[See Ableton’s help page regarding installing third-party remote scripts.](https://help.ableton.com/hc/en-us/articles/209072009-Installing-third-party-remote-scripts)

1.	Start Live.
1.	Enable **mk3** as a Control Surface in Live

	In Live’s Preferences go to the **MIDI Sync** tab and select **mk3** in the dropdown list of available Control Surfaces. For the MIDI Input and Output, select your controller’s MIDI-port.
	
NB: If you want to make this work for the mk2, have a look at this [issue](https://github.com/SlyBouhafs/MMMKIII/issues/5)

## What this fork changes from the original script
1. "Up" and "down" actions like switching between device banks and scenes are swapped, 
	to make more sense to anyone used to a vim-like scheme of arrow navigation with
	a horizontal row of keys/pads
1. The Session and Arrangement view programs have the knobs control mixer parameters,
	rather than device parameters
1. The mixer knob layout is changed to be more intuitive, as recommended in
	[this issue](https://github.com/SlyBouhafs/MMMKIII/issues/6) for the original script
1. "Play/pause" in Arrangement view has been changed to "play/stop", so that playback
	always resumes from the playhead
1. Mixer pad controls no longer have "first track" and "last track" as actions - instead,
	"previous track" and "next track" are repeated for both up/down and left/right, with
	the intention of making navigation more intuitive in both Session and Arrangement view
1. A bug where two mixer knobs send to the same return track has been fixed
1. Four "bind" programs have been added under `assets/presets` - in total, these programs
	add 32 more knobs with absolute encoders (8 in each program) for the purpose of making
	new MIDI binds without creating any conflicts with the relative encoder bindings that
	control mixer and device parameters