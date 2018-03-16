# TicTacToe-Game
A bash script for TicTacToe game using Nginx frontend and FastCGI backend.

There is 4 elements in this simple TicTacToe game : <br />
1. Command-line interface for interfacing with a web-service, with getopt support etc. <br />
2. Nginx frontend, with automatic startup inside the OS (using a VM is recommended). As-sume static IP (e.g., port forwarding into NAT-based VM). <br />
3. Web backend using FastCGI as default for all URLs, with some exclusions for static files, detected via URL at frontend level. <br />
4. Autotools-based project, including native code dynamic shared library. <br />
