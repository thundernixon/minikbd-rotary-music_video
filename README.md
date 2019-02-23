# MiniKbd rotary: System Music + Video Speed Control

This is my code for the [miniKbd](https://github.com/andyclymer/minikbd), customized from the [TwoEncoder-Multimode](https://github.com/andyclymer/minikbd/tree/master/Software/TwoEncoder-Multimode) starter setup.

In mode 1, it controls macOS system music – play/pause, up/down volume, and skip/prev song.

In mode 2, it controls the Chrome extension [Video Speed Controller](https://chrome.google.com/webstore/detail/video-speed-controller/nffaoalbilbmmfgbnbgppjihopabppdk?hl=en) – play/pause, skip forward/back by 5 seconds, and speed increase/decrease.


## Installation

1. Download or clone this repo
2. Follow [Adafruit's instructions to prevent hidden files on your miniKBD](https://learn.adafruit.com/welcome-to-circuitpython/troubleshooting#running-out-of-file-space-on-non-express-boards-19-37)
3. If needed, clear out existing files in your CIRCUITPY. Open your terminal, then navigate to `/Volumes/CIRCUITPY` (if you haven't already), and delete all files inside:

```
rm -rf ./*
```

4. Now, copy in files from the `CIRCUITPY/` folder in this project to the miniKBD (editing the file paths as needed):

```
cp -R <downloaded_file_path>/minikbd-rotary-music_video/CIRCUITPY/* /Volumes/CIRCUITPY
```

5. In Chrome (or Brave) browser, download the extension extension [Video Speed Controller](https://chrome.google.com/webstore/detail/video-speed-controller/nffaoalbilbmmfgbnbgppjihopabppdk?hl=en). Then, click its icon, and go to settings and set up as follows:

|Function|Hotkey|
|------------|----------------|
| Decrease speed | W |
| Increase speed | E |
| Rewind | Z |
| Advance | X |

## Requirements

All required files are included in the `CIRCUITPY/` folder of this project, but just in case you'd like to update them on your miniKBD, here are the required files from Adafruit:

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