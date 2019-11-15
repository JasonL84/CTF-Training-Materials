Installation:

Linux/MacOS:
Download the newest release of Radare2 from https://github.com/radareorg/radare2/releases
Unzip file 
Navigate to folder and run command sys/install.sh (if you want global access) otherwise run sys/user.sh

Windows:
Download latest binary from https://radare.mikelloc.com/list (Note as of last update version 4.00 appears to be corrupted, download the msvc installer for version 3.9)
Run binary
Done.

If there are any errors create an issue on the repository and I will take a look at it

Running Radare2:
Linux/MacOS:
To disassemble a file run the command
r2 -v! <file here>

Windows:
Right click on the file and select the Open in Radare2 option
To enter visual mode run the command V! when the shell opens
