# cpsort

I have a dummy MP3 player in my car. It always plays files in the filesystem order. I had made a plenty of such kind of utility, but everytime i change a PC i forget to move this utility to new one. This time i decided to push it here. Maybe someone appreciate it.

This time i did it with Python. This is my 1st python script, so go easy on me :)

## Install

Just put cpsort file somewhere and make it executable.

## Usage
The script is pretty simple. 

$ cpsort
cpsort <srcdir> <destdir> 
	<srcdir> - source directory
	<destdir> - destination directory
 
If i want to place ~/Music/SomeGreatStuff to /media/andrey/Transcend folder, i'd simply run
$ cpsort ~/Music/SomeGreatStuff /media/andrey/Transcend

The script walks through the source directory recursively (skips symlinks) and builds the list of files to copy, then sorts the list alphabetically and copies the files using shutil.copy2()

## Compatibility

I used Python 2.7.13
