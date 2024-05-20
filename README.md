# ComputerDisabler
The script that will disable a (probably windows) computer from use for a set time, or until some other trigger is set off.

It functions by creating a file in a random accessible location on the filesystem, it then spawns a new (maybe python) instance that isn't linked to the current script.

## NOTE: You must setup a stop sequence on Najort ends everything when it can't connect to the server

## Step-by-step walkthrough of stager

1. This script is run through Najort
2. This script does environment checks
3. This script finds an accessible location on the filesystem with adequate permissions for file creation
4. Creates a script with just the payload, selected trigger(s) and self destruct
5. Runs the payload in a new python instance
6. The script deletes self self
7. The script ends self

## Step-by-step walkthrough of payload
1. The payload sets up listeners for the triggers
2. The payload sets up a failsafe that reconnects all the displays
3. The payload disables the display(s)
4. The triggers are triggered
5. The script deletes self
6. The script ends self
