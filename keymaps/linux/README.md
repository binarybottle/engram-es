## Linux

Install:

    sudo make install
    echo Now restart your X session.

Activate:

    setxkbmap -layout us    -variant engram         # one layout; no switch
    setxkbmap -layout us,us -variant engram,basic   # dual layout switching

Reinstall (whenever a system-wide XKB package upgrade reverts installation):

    sudo make reinstall

Uninstall:

    sudo make uninstall
