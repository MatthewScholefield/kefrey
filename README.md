# Kefrey

*A tool to track system-wide keypress frequencies*

If a laptop key breaks, it's useful to be able to know which keys are
least used across all your tasks. This way, you can swap the least used
key for the one that broke. This script tracks this data with a keylogger
(don't worry, it only stores distribution data).

If you want to parse this distribution data to find the least used square keys on most US laptop keyboards, [here's a script that does that](https://gist.github.com/MatthewScholefield/d4f29dd195415cf2dbd2d0f29cffdec5).


## Install

```bash
pip3 install --user kefrey
```

## Setup Tracking

```bash
kefrey-install
systemctl enable --user kefrey
systemctl start --user kefrey
```

Now, a file `~/.kefrey.json` will contain keypress distribution info,
tracked in the background, started at startup.
