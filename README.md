# virtualbox-safe-update

A simple libalpm hook to block a pending VirtualBox update if any VM not completely powered off.

The check is only performed for the current logged in user that performed the system update.

## Installation

First of all, copy the script to `/usr/bin/`.
Set the owner to `root:root`.

Then enable the hook by copying it to `/usr/share/libalpm/hooks/`.

Remember to set the correct permission/owner to this file (look for other files in the same directory).

It is better to rename the hook with a leading `00-` in order to stop the update process as soon as possible.


