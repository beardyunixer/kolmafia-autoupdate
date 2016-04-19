# kolmafia-autoupdate
An auto-updater/launcher for KoLMafia

This is a quick and dirty script to update to the latest version of KoLMafia, 
and then launch the application.

We check the latest version number (checking only those that built successfully)
and compare it to your own.  If it's a different version, we pull the update.
We don't check if the version is *higher*, we just check if it's different.
This **should** insulate us from any change to the versioning system.

If there's a new version, we download it, then replace the old version with it
(ie, we don't gather hundreds of old files).  Then, whether we downloaded a new
version or not, launch the newest version we have.

You should be able to just chmod +x mafia and then run 'mafia' from the CLI.  
However, from past experience, there are some ill defined issues with unknown 
configurations where you can't just ./mafia

Additionally, if you're running this from an app menu (eg, Klicker) or a desktop
shortcut, you'll also need to explicitly call 'php /path/to/mafia'

Oh, and requirements are weird.  This is written in PHP, so you'll need CLI PHP
installed, which you probably won't on a desktop.  apt-get install php5-cli on
Debian systems.  The reason for this is the script was intended for me and me
alone, and I'm only publishing it because somebody else said they'd find it 
useful.

