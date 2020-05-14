# st - simple terminal
st is a simple terminal emulator for X which sucks less.

## Workflow for patching and updating
clone from ggadget6/st <br/>
do git remote add suckless https://git.suckless.org/st <br/>
apply patches to branch "custom" <br/>
set upstream for master branch to suckless <br/>
When updating, switch to master branch and pull <br/>
Then, switch to custom branch and rebase to commit (git rebase --onto <commit> master) <br/>
To push, do git config remote.pushdefault origin, then git config push.default current <br/>
Then feel free to push

## Requirements
In order to build st you need the Xlib header files. <br/>
For the ligature patch, you'll need harfbuzz. This can <br/>
be installed on Ubuntu as libharfbuzz-dev (I believe--if not, build <br/>
from source). [Source](https://www.freedesktop.org/wiki/Software/HarfBuzz/)

## Installation
Edit config.mk to match your local setup (st is installed into
the /usr/local namespace by default).

Afterwards enter the following command to build and install st (if
necessary as root):

    make clean install

## Patches
Here are the patches included in this build
1. Xresources
2. Alpha
3. font2
4. anysize
5. boxdraw
6. ligature

## Configuration
config.def.h and config.h hold lots of configuration settings. To see what Xresources
options there are, look at the Resources array in the aforementioned config files. 

## Running st
If you did not install st with make clean install, you must compile
the st terminfo entry with the following command:

    tic -sx st.info

See the man page for additional details.

## Credits
Based on Aurélien APTEL <aurelien dot aptel at gmail dot com> bt source code.

