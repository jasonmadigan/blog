---
title: iPhone - Voicemail Button
date: 2007-09-13T21:00:00
---

You can use your iPhone's Voicemail button to call your local carriers
voicemail number by doing the following:

-   Disable your SIM PIN, if enabled.
-   SSH into your iPhone - I'm going to assume your iPhone has been
    jailbroken, has SSH installed and the latest BSD Subsystem
    installed.
-   The latest BSD Subsystem (1.5) comes with minicom, but you'll need
    to generate a configuration file for it to interact with the
    baseband. You'll need to create `/local/etc/` in `/usr/`.
-   In `/usr/local/etc/`, run `nano minirc.dfl` and paste
    `pu port /dev/tty.baseband`
-   Save the file, `CTRL-O`, exit nano `CTRL-X`
-   Disable the commcenter -
    `launchctl unload -w /System/Library/LaunchDaemons/com.apple.CommCenter.plist`
-   Run@ minicom@
-   Run@ AT+CSVM=1,"171" `where 171 is your carriers voicemail number
    * Exit minicom - `CTRL-a`, then `q@
-   Restart the commcenter
    `- launchctl load -w /System/Library/LaunchDaemons/com.apple.CommCenter.plist`
-   Done!

