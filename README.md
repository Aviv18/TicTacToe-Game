# TicTacToe-Game
A bash script for TicTacToe game using Nginx frontend and FastCGI backend.

There is 4 elements in this simple TicTacToe game : <br />
1. Command-line interface for interfacing with a web-service, with getopt support etc. <br />
2. Nginx frontend, with automatic startup inside the OS (using a VM is recommended). As-sume static IP (e.g., port forwarding into NAT-based VM). <br />
3. Web backend using FastCGI as default for all URLs, with some exclusions for static files, detected via URL at frontend level. <br />
4. Autotools-based project, including native code dynamic shared library. <br />

-----------------------------------------------------------------------------

The game folder includes the cpp and header files and the autoconfig.
The game folder is for the server side

The script file is for the client side

The crontab is for the automatic activation of the fcgi-spawn after boot

We added AC_SEARCH_LIBS and AC_CHECK_FUNCS to configure.ac as requested.

** importent **
1) The server must open port 1234.
2) because there was some problems with mint, in order to activate automatically the program after boot, we go the game folder and not to the usr/local/bin folder.
please change the path in the crontab file to usr/local/bin/project

In the server side, go to the game folder and do the follow:
1) autoreconf -i
2) ./configure
3) make
4) sudo make install 

After that, reboot the server and the server will automatically activate fcgi-spawn at port 8000
