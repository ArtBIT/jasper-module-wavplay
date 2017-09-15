# Jasper-Module-WavPlay

Jasper WavPlay Module for my [HAL9000 Raspberry PI Instructable](http://www.instructables.com/id/RaspberryPI-HAL9000/)
Upon trigger, it plays a random wav file from a pre-configured directory.

## Steps to install WavPlay Module

* download some [HAL9000 wav files](http://www.imdb.com/title/tt0062622/externalsites#sounds)
* run the following commands in order:
```
git clone https://github.com/ArtBIT/jasper-module-wavplay.git
cp jasper-module-wavplay/WavPlay.py <path to jasper/client/modules>
#i.e. cp jasper-module-wavplay/WavPlay.py /usr/local/lib/jasper/client/modules/
mkdir ~/wavs
cp path-to-downloaded-wavs/*.wav ~/wavs
```
* Edit `~/.jasper/profile.yml` and add the follwing at the bottom:
```
wavplay:
  path: /home/pi/wavs
```
* Restart the Pi:
```
sudo reboot
```
## Congrats, JASPER WavPlay Module is now installed and ready for use!
Here are some examples:
```
YOU: Say something.
JASPER: *plays a random wav from the ~/wavs directory*
YOU: Dave?
JASPER: *plays a random wav from the ~/wavs directory*
```
