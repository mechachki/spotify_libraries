# spotify_libraries
Some files required to run the local music files in Ubuntu 16.04 LTS on Spotify 1.0.28.89.

Tested also on Debian Jessie and Scratch (testing) on Jun, 6 2016
Tested also on Ubuntu 20.04 LTS on February, 12 2021

## Instalation

1. Download the package: https://github.com/ramedeiros/spotify_libraries/archive/master.zip
    * Or direct from the terminal: git clone https://github.com/ramedeiros/spotify_libraries.git


1. Put all the files in to `/usr/lib/x86_64-linux-gnu/` with root privileges.
    * use `sudo cp -a /source/. /usr/lib/x86_64-linux-gnu/`  

1. Execute: `sudo ldconfig`

1. If show any problem with link, make new links.
        * e.g.: "/sbin/ldconfig.real: /usr/lib/x86_64-linux-gnu/libavutil.so.52 it's not a symbolic link"
        * So, execute command: `sudo ln -rs` /usr/lib/x86_64-linux-gnu/libavutil.so.52.6.100 /usr/lib/x86_64-linux-gnu/libavutil.so.52
  
## Misc
1. Spotify is fucked if u get latest release from their repository/snap store - if you try to add local files location it crashes, so use the older version (1.1.26.501) of the client from here: 
  * https://repository-origin.spotify.com/pool/non-free/s/spotify-client/

1. Not sure if it was relevant but before installing this I got these extra codecs:
  * `sudo apt install ubuntu-restricted-extras ffmpeg libavcodec-extra libavcodec-extra58 libavutil56 libavformat58 zenity -y`
