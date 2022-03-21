## install
    sudo apt install exe2hex
## Usage
    exe2hex [options]
## Basic Usage
    exe2hex v1.5.1

    Encodes an executable binary file into ASCII text format
    Restore using DEBUG.exe (BATch - x86) or PowerShell (PoSh - x86/x64)

    Quick Guide:
     + Input binary file with -s or -x
     + Output with -b and/or -p
    Example:
     $ /usr/bin/exe2hex -x /usr/share/windows-binaries/sbd.exe
     $ /usr/bin/exe2hex -x /usr/share/windows-binaries/nc.exe -b /var/www/html/nc.txt -cc
     $ cat /usr/share/windows-binaries/whoami.exe | /usr/bin/exe2hex -s -b debug.bat -p ps.cmd

    --- --- --- --- --- --- --- --- --- --- --- --- --- --- ---

    Usage: exe2hex [options]

    Options:
      -h, --help  show this help message and exit
      -x EXE      The EXE binary file to convert
      -s          Read from STDIN
      -b BAT      BAT output file (DEBUG.exe method - x86)
      -p POSH     PoSh output file (PowerShell method - x86/x64)
      -e          URL encode the output
      -r TEXT     pRefix - text to add before the command on each line
      -f TEXT     suFfix - text to add after the command on each line
      -l INT      Maximum HEX values per line
      -c          Clones and compress the file before converting (-cc for higher
                  compression)
      -t          Create a Expect file, to automate to a Telnet session.
      -w          Create a Expect file, to automate to a WinEXE session.
      -v          Enable verbose mode
