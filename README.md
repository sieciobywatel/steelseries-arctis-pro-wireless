# THIS IS WORK IN PROGRESS!!!
for now it does not work, but stay tuned

# SteelSeries Arctis 5 pulseaudio profile

The SteelSeries Arctis 5 is a gaming headset which has two stereo audio outputs. One for voice chat and one for the rest of the sound. It can be mixed between with a physical knob.

By default, pulseaudio only enables the voice chat output. This profile enables the second (game) output and the udev rule makes sure this profile is used when plugging in the device.

## Installing

### Ubuntu / Linux Mint

Download and install:

- [pulseaudio-steelseries-arctis-5_0.2_all.deb](https://github.com/DemonTPx/steelseries-arctis-5-pulseaudio-profile/releases/download/0.2/pulseaudio-steelseries-arctis-5_0.2_all.deb)

After that, plug in the device to see if it works.

### From source

Install from by copying the following files:

- `steelseries-arctis-5-output-game.conf` and `steelseries-arctis-5-output-chat.conf` to `/usr/share/pulseaudio/alsa-mixer/paths/`
- `steelseries-arctis-5-usb-audio.conf` to `/usr/share/pulseaudio/alsa-mixer/profile-sets/`
- `91-pulseaudio-steelseries-arctis-5.rules` to `/lib/udev/rules.d/`

Restart pulseaudio:

    pulseaudio -k
    pulseaudio --start

After that, plug in the device to see if it works.
