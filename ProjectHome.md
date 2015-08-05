## [Application and Source](http://code.google.com/p/luks-volume-cracker/downloads/detail?name=application_and_source.zip&can=2&q=) ##
[Help](http://code.google.com/p/luks-volume-cracker/downloads/detail?name=Help.pdf&can=2&q=)

An application for performing a dictionary attack on encrypted volumes. Basically a wrapper around FreeOTFE, which also supports Linux volumes (Cryptoloop, dm-crypt, LUKS).

By design these encrpytion systems are very slow to brute force, so a dictionary based attack is only appropriate for poorly chosen passphrases.

### Benefits ###
  * Check if your passphrase is secure

## How it works ##
  * Count the initial number of drives in the system
  * Loop through the input in the dictionary
    * Execute a command line statement to mount the encrypted image using the current passphrase (/mount /volume [volume](volume.md) /password [password](password.md) /silent N:\\)
    * If it’s a Linux drive, use the WinAPI to automatically fill in the GUI prompt
    * When the number of drives has changed a volume has been mounted, so one of the recently tried passwords was used

## About ##
Uses the excellent FreeOTFE by SDean http://www.freeotfe.org/

Created by Christopher Doman (http://www.christopherdoman.com) for the DC3 Forensics Challenge 2012 (http://www.dc3.mil/challenge/2012). Created on quite a short schedule, so please consider this beta software and inform me of any bugs.

![http://luks-volume-cracker.googlecode.com/files/screenshot.png](http://luks-volume-cracker.googlecode.com/files/screenshot.png)