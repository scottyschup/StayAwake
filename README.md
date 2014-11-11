StayAwake 
=========
is a shell script that will temporarily disable your screensaver and sleep settings. This script is useful when using your laptop to give a presentation as it keeps you from having to go into system preferences and turn the sleep/screensaver functions off and back on again. 

Setup instructions:

* Copy the file "stayawake" into your Home directory; the standard place is the bin directory in your Home directory (/Your-User-Name/bin). If this folder doesn't exist, create it.
* Open a terminal window and navigate to that directory:
> cd ~Your-User-Name/bin

* See if the directory you copied "stayawake" to is already in your PATH variable:
> $PATH

Note that paths are separated by a colon (:).

* If the directory is not in the PATH variable, add it:
> export PATH=$PATH:/Users/Your-User-Name/bin

* Change the new file's mode to executable:
> chmod +x stayawake

* Give it a try!

Usage:

* Open a terminal window 
* Type "stayawake" and the number of minutes you want your screen saver and sleep disabled (I recommend testing it with 1 minute at least once after setup):
> stayawake 1

* To verify that it's working, open a new terminal tab (CMD-T) and type:
> pmset -g

* In the 20 lines or so that you get, look for a line that starts with the word "sleep" and verify that its value is 0. Similarly, look for the line that starts with "displaysleep" and verify that its value is also 0. 

* After StayAwake tells you that sleep settings have been turned back on, repeat the above process and verify that sleep and displaysleep are no longer set to 0.
