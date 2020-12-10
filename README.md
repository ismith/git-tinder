# git-tinder
git add -p meets Tinder

Runs `git add -p` in ... Tinder mode.

Swipe right to stage a hunk (IYKWIM. `man git-add` if not, or leave your mind
in the gutter ;-) ), swipe left to give it a pass.

This also supports splitting the current hunk if you pinch out. (Or pinch in, or
swipe up - I have had better luck getting those to register.)

All swipes are 3-finger gestures.

Credit for the idea goes to
https://twitter.com/benawad/status/1336691028473090050 and
https://twitter.com/bcrypt/status/1336934917599444992

INSTALLATION:
=============
Put this in your PATH, and it'll work as a git subcommand (`git tinder`).

DEPENDENCIES:
=============
On my XPS 13 with Ubuntu 18.04, install was:

sudo apt install xdotool libinput-tools
git clone https://github.com/bulletmark/libinput-gestures
cd libinput-gestures
sudo make install
sudo usermod -a -G input $USER

and restart to pick up the new group. YMMV. See the DEBUGGING comment in the
script if it doesn't work.

CONTRIBUTING:
=============
PRs welcome! We run [shellcheck](https://github.com/koalaman/shellcheck) on PRs,
see `.github/workflows/`.
