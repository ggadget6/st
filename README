st - simple terminal
--------------------
st is a simple terminal emulator for X which sucks less.

Workflow for patching and updating
---------------------
clone from ggadget6/st
do git remote add suckless https://git.suckless.org/st
apply patches to branch "custom"
set upstream for master branch to suckless
When updating, switch to master branch and pull
Then, switch to custom branch and rebase to commit (git rebase --onto <commit> master)
To push, do git config remote.pushdefault origin, then git config push.default current
Then feel free to push

Requirements
------------
In order to build st you need the Xlib header files.


Installation
------------
Edit config.mk to match your local setup (st is installed into
the /usr/local namespace by default).

Afterwards enter the following command to build and install st (if
necessary as root):

    make clean install


Running st
----------
If you did not install st with make clean install, you must compile
the st terminfo entry with the following command:

    tic -sx st.info

See the man page for additional details.

Credits
-------
Based on Aurélien APTEL <aurelien dot aptel at gmail dot com> bt source code.

