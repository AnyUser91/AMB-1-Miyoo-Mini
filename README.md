# AMB-1 for the Miyoo Mini Plus

## Support

AMB-1 itself is Charles Vestal's work, and if you like the instrument, [his repository](https://github.com/charlesvestal/fm1-amb)
is where to say so. This port is free. If it was useful to you and you would like to thank me for the port work, you
can support me (https://paypal.me/AnyUser91). It is entirely optional; it does not buy support or
features.

**AMB-1 is a generative ambient machine, inspired by Brian Eno's *Music for Airports*.** It plays itself from the
moment it starts: breathing pad voices, soft bells on tape loops of unequal length, a gliding bass and quiet Euclidean
percussion, all through a tape echo, a long tape loop and a plate reverb. You don't perform it, you tend it: pick a
piece and a scale, take notes out, put them back, and let it grow.

AMB-1 was made by **[Charles Vestal](https://github.com/charlesvestal/fm1-amb)** for the M-VAVE FM-1. This is an
unofficial port of it to the **Miyoo Mini Plus running OnionOS**: the engine, the eight pieces and the screen are his,
unchanged. Only the controls are new: the FM-1's 27 keys, 14 buttons and 7 knobs become the Miyoo's D-pad, face
buttons, shoulders, START and SELECT.


## Install

1. Download `AMB-1-miyoo-mini-plus.zip` from **[Releases](GITHUB-LINK/releases)** and unzip it.
2. Copy the `AMB-1` folder to `App/` on the SD card (`/mnt/SDCARD/App/AMB-1`).
3. Open it from OnionOS's Apps. The first launch shows the controls; any button closes them.

It keeps your pieces and the volume in `amb.sav` in its own folder, and writes `log.txt` there (the last run's
messages: please attach it to a bug report). Leaving with MENU saves what you changed.

## Controls

| | |
|---|---|
| D-pad UP / DOWN | Pick one of the four knobs (the picked one is underlined, and numbered on the right) |
| D-pad LEFT / RIGHT | Turn it; hold to go fast |
| L / R | Previous / next page: Garden, Pad, Bells, Bass, Pulse, Space, Setup |
| A | Grow / rest |
| B | Freeze |
| X | Next chord |
| Y | Home page; Y held with L / R: the tempo |
| START | Save; held for 1.5 s: the piece back to its recipe |
| SELECT held, then | LEFT / RIGHT: move along the twelve notes (left bar); A: add or take out that note; UP / DOWN: the bells' octave; L / R: previous / next piece; X / Y: next / previous mode; B / START: volume down / up |
| SELECT alone | The help screen |
| MENU | Save and quit |


The left bar shows the twelve notes: filled is in the scale, the root is teal. The right bar shows the knob you are
on, whether SELECT is held, and the volume (the app's own, set with SELECT + B / START). The app uses no MENU
combinations, so OnionOS's own system hotkeys are not touched by it.

## What is not here

- The FM-1's USB, MIDI in and out, MIDI clock sync, the USB recording and the screen reader link: the Miyoo has no such
  ports. The tempo is set on the Garden page (or with Y + L / R) and nothing follows an outside clock.
- The hold-a-button help cards still name the FM-1's buttons (OCT+, SEL, ...).
- The battery in the header is read from the kernel's power supply; if the Miyoo does not publish one there, the header
  shows none.
  

## Credits and licence

- **AMB-1** and **fm1-base**: [Charles Vestal](https://github.com/charlesvestal). The idea is from Brian Eno's generative
  music; the reverb is Jon Dattorro's plate.
- **felucca-bsp**: [Leo Kuroshita](https://github.com/hugelton/felucca-bsp) (Hügelton Instruments), which fm1-base is
  built on.
- **OnionOS**: [the Onion team](https://github.com/OnionUI/Onion); the button codes are from its `keymap_hw.h`.
- The Miyoo front end was written with the help of Claude (Anthropic).

MPL-2.0, as AMB-1 (see `LICENSE`). This port is not an official part of AMB-1, and is not affiliated with or endorsed by
Charles Vestal, M-VAVE, Miyoo or OnionOS.
