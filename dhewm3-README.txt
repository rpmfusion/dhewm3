____  ____  ____                        _____ ____  _____ ____ 
|  _ \| __ )|  _ \  ___   ___  _ __ ___ |___ /| __ )|  ___/ ___|
| |_) |  _ \| | | |/ _ \ / _ \| '_ ` _ \  |_ \|  _ \| |_ | |  _ 
|  _ <| |_) | |_| | (_) | (_) | | | | | |___) | |_) |  _|| |_| |
|_| \_\____/|____/ \___/ \___/|_| |_| |_|____/|____/|_|   \____|
                                                                
** Doom 3 BFG Edition GPL source modification

For the additional features and fixes introduced by this great modification,
please see the original page at:

 https://github.com/RobertBeckebans/RBDOOM-3-BFG

======== Game data

It DOES NOT include game data required to run the game, you have to get the data
yourself buying the game.

To launch the engine pointing at your data files you can use the following
command:

 doom3bfg-engine +set fs_basepath "/path/to/game/content" "$@"

A sample nosrc rpm that can be used to build a binary rpm using the DVD data
files is at: http://slaanesh.fedorapeople.org/

To rebuild it, add the required files to your SOURCES directory and remove the
"NoSource" lines in the spec file.

A high resolution icon has been generated from the game assets, to have a look
at how the resulting menu entries look like see:
http://slaanesh.fedorapeople.org/doom3bfg-menus.png

You should end up with something like this:

 $ rpm -qa dhewm3* doom3*
 dhewm3-1.3.1.1304-19.gitfa231898.fc19.x86_64
 doom3-1.3.1.1304-4.fc18.noarch
 doom3-roe-1.3.1.1304-4.fc18.noarch

======== Options defined at compile time

- Uses unbundled Fedora libraries for the following components:
    OpenAL
    Curl
    Ogg Vorbis
    SDL
    zlib
- Uses SDL2 on Fedora 19+ and RHEL/CentOS 7+.
- Provides a doom3bfg-engine symlink through the alternatives system to easily
  switch between additional variations.
- Removes the bundled libraries and tools required for compiling Doom Classic
  (not working in the current source code). 

======== Notes

- The Doom Classic icons in the main menu do not work; they are not selectable.
  This is by design.
- Bink Videos do not work, the code is patented and not present in the current
  source code.
