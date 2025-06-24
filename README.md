# Super simple AeroSpace autotiling script

The script checks the number of windows in the current workspace, if the number is odd it splits horizontally, and if the number is even it splits vertically

These two options have to be set to false inside your .aerospace.toml configuration file

    enable-normalization-flatten-containers = false
    enable-normalization-opposite-for-nested-containers = false

You also need to trigger the script each time focus changes (this happens when a new window is opened as well)

    on-focus-changed = ['exec-and-forget /absolute/path/to/autotiling']

You can move the autotiling script to some directory, and then you need to add it in the .aerospace.toml configuration file inside on-focus-changed trigger

e.g.

    mv autotiling $HOME/.local/bin

You may need to add execute permission to the autotiling script

    chmod +x autotiling

Then the absolute path would be:

    on-focus-changed = ['exec-and-forget $HOME/.local/bin/autotiling']

Enjoy autotiling!

---
This project is licensed under the terms of the __MIT__ license.
