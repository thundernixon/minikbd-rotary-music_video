# miniKbd Two Encoder setup for System Music + Video Speed Control

This is my code for the [miniKbd](https://github.com/andyclymer/minikbd), customized from the [TwoEncoder-Multimode](https://github.com/andyclymer/minikbd/tree/master/Software/TwoEncoder-Multimode) starter setup.

In mode 1, it controls macOS system music – play/pause, up/down volume, and skip/prev song.

In mode 2, it controls the Chrome extension [Video Speed Controller](https://chrome.google.com/webstore/detail/video-speed-controller/nffaoalbilbmmfgbnbgppjihopabppdk?hl=en) – play/pause, skip forward/back by 5 seconds, and speed increase/decrease.

To avoid existing shortcut keys on Vimeo, I have separately configured the Video Speed Controller [settings](chrome-extension://nffaoalbilbmmfgbnbgppjihopabppdk/options.html) to use `W` for _decrease speed_ and `E` for _increase speed_.

CIRCUITPY lib files required for this setup:

```
- lib
  - adafruit_hid
    - __init__.py
    - consumer_control_code.mpy
    - consumer_control.mpy
    - keyboard_layout_us.mpy
    - keyboard.mpy
    - keycode.mpy
  - adafruit_dotstar.mpy
- ._encoder.py
- ._main.py
```

...and the files inside this Gist. The most important one is `main.py`

## Installation

1. Download or clone this repo
2. Follow [Adafruit's instructions to prevent hidden files on your miniKBD](https://learn.adafruit.com/welcome-to-circuitpython/troubleshooting#running-out-of-file-space-on-non-express-boards-19-37)
3. If needed, clear out existing files in your CIRCUITPY. Open your terminal, then navigate to `/Volumes/CIRCUITPY` (if you haven't already), and delete all files inside:

```
rm -rf ./*
```

4. Now, copy in files from the `CIRCUITPY/` folder in this project to the miniKBD:

```
cp -R <downloaded_file_path>/minikbd-rotary-spotify_videospeed/CIRCUITPY/*  /Volumes/CIRCUITPY
```
