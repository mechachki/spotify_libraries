# spotify_libraries
Some files required to run local music files in Spotify on Linux

* originally for `Spotify 1.0.28.89` running on `Ubuntu 16.04 LTS`

* tested also on:
   * Debian Jessie and Scratch (testing) on Jun, 6 2016
   * Ubuntu 20.04 LTS on February, 12 2021
      * Spotify version: `1.1.26.501`

## Instalation

1. Download the package: [spotify libraries][libs]
    * Or direct from the terminal: `git clone https://github.com/ramedeiros/spotify_libraries.git`


1. Put all the files in to `/usr/lib/x86_64-linux-gnu/` with root privileges.
    * use `sudo cp -a /source/. /usr/lib/x86_64-linux-gnu/`  

1. Execute: `sudo ldconfig`

1. If show any problem with link, make new links.
        * e.g.: "/sbin/ldconfig.real: /usr/lib/x86_64-linux-gnu/libavutil.so.52 it's not a symbolic link"
        * So, execute command: `sudo ln -rs` /usr/lib/x86_64-linux-gnu/libavutil.so.52.6.100 /usr/lib/x86_64-linux-gnu/libavutil.so.52
  
## Misc
1. Snap store and spotify's repository hold a newer broken version which crashes when you try to add local files location, use older version of the client instead:
   * [direct download][client_download]
   * [spotify client repository][client]  - (the above link directly downloads version 1.1.26.501 from this repository) 
   

1. Not sure if it was relevant but before installing this I got these extra codecs:
   * `sudo apt install ubuntu-restricted-extras ffmpeg libavcodec-extra libavcodec-extra58 libavutil56 libavformat58 zenity -y`

[client_download]:         https://repository-origin.spotify.com/pool/non-free/s/spotify-client/spotify-client_1.1.26.501.gbe11e53b-15_amd64.deb      "older spotify client download"
[client]:                  https://repository-origin.spotify.com/pool/non-free/s/spotify-client/         "repository with older versions of the client"
[libs]:                    https://github.com/ramedeiros/spotify_libraries/archive/master.zip            "spotify libraries (master branch of this repository)"
