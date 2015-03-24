This Arduino bootloader is a fork of Adaboot which is a fork of the original bootloader.

The Adaboot bootloader has patches for watchdog fixes and patches to enable the pin 13 led to blink as the sketch downloads.  It also jumps directly to the sketch unless you hit the reset button.

The toasted bootloader extends the pin 13 LED to pulse while it is able to receive downloads.  By default (its configurable in the makefile) it extends the time it waits for a download to about 10 seconds.  This avoids a lot of confusion for users since the prior version required very precise timing when pressing the reset button.

Also since the download time is much longer a feature was added where if you double click the reset button it jumps directly to the sketch.