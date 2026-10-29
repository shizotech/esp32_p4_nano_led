
# Custom LED software for the esp32-p4-nano board

- Alternative to wled, more powerful, with no limitations

- Better audioreactivity

- Fully programmable and expandable with shizoscript

- Webinterface

- Works with WLAN and Ethernet

- Works with artnet / resolume etc out of the box

# How to install

Check the online flasher here: https://shizotech.com/public/microcontroller/

# Donations

https://buymeacoffee.com/erikm

# Disclaimer

Note this is actually an arduino project, but I cannot make the full source code public because it contains the shizoscript source,
which is not (yet) public.
Only the shizoscript script source files are available (it is kind of like micropython)

# Issues and pull requests

The files here (`data/`, `_flash_files_over_network.shio`) are a copy of the firmware source, which is not public yet.
Every release overwrites them, so a pull request that changes them would be lost: the fix is made in the source and
reaches this repository with the next release.

Please file bugs and wishes as issues here. The overview issue #26 lists them and their state; an issue is closed
when its fix is in the source.

# Flashing the files over the network

```
shz _flash_files_over_network.shio <device name | MAC | IP>
```

It uploads `data/` to that one device, checks that every file was written and only then reboots it. Every new
device is called "ESP32", so use the MAC or IP (shown in the header of the web interface) or give the device a name
first. (This needs the version of the script from the next release.)
