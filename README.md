#HOW TO USE
on linux(run as su):
SOURCEDIR=/home/<username>/Downloads TARGETDIR=/boot node index.js

on windows(run as admin):
SOURCEDIR=C:\Users\<username>\Downloads TARGETDIR=C:\Windows\System32 node index.js

#Personal Notes
im pretty sure im just wasting my precious fucking time at this point.

ISSUE
Need to keep certain folders up to date with folders on other drives/locations, not the entire drive. Drive cloning hardware requires like kind drives. Screw other software.

Solution
Parity! Parity gets one location up to date with another.
The tool will
- scan both directories and generate an assessment of work to be done
- probably ruin my life because I was drunk and switched target and source directories

The tool will not
- completely erase a populated location with an empty location

Parameters
- source: string(directory)
  the location that will overwrite the other

- target: string(directory)
  location to be overwritten

- operation: string
  possible options:
    assess: generate an assessment of work to be done
    update: updates the target. will still generate an assessment anyway

- noDelete: bool
  if set to true, it will not remove anything in the target directory, only overwrite and add

- keepNewer: bool
  if set to true, will not overwrite anything newer

an assessment will provide the following data:
- how much data will be added/removed
- how many files will be added/deleted/updated
- how many folders will be added/deleted?

I would like a shitty html file to view, shouldnt be to hard to whip up

red for deleted
green for added
yellow for updated
orange for updated but smaller size?
white for unchanged

example cli output:
source:
files: 1345 folders: 33 size: 45GB
