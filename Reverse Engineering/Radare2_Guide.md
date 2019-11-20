# Installation:

## Linux/MacOS:
Download the newest release of Radare2 from https://github.com/radareorg/radare2/releases

Unzip file 

Navigate to folder and run command sys/install.sh (if you want global access) otherwise run sys/user.sh

## Windows:
Download latest binary from https://radare.mikelloc.com/list (Note as of last update version 4.00 appears to be corrupted, download the msvc installer for version 3.9)

Run binary

Done.

If there are any errors create an issue on the repository and I will take a look at it

# Running Radare2:
## Linux/MacOS:
To disassemble a file run the command
r2 -v! <file here> //the v! makes radare2 automatically open in video mode

## Windows:
Right click on the file and select the Open in Radare2 option
![image](https://user-images.githubusercontent.com/26120937/68963128-37c66000-07a4-11ea-8114-8700f6c73ced.png)

To enter visual mode run the command V! when the shell opens
![image](https://user-images.githubusercontent.com/26120937/68963187-5f1d2d00-07a4-11ea-9dfb-00b906ec753d.png)

# Anatomy of a Radare2 Session:
//TODO


# Summary of useful commands:

While in visual mode press shift + ; to enter commands (similar to vim)

s \[target\] seeks to target location, target can be specified as a label, as an address (hex) or as an offset to a register ie (R1 + 4) 

ood \[file\] opens the file in debug mode - note make sure that the file is executable done by using chmod in linux

ds (used in debugger mode only) carries out the current instruction and moves to the next line - this is used to track changes in register values

dc (used in debugger mode only) : lets the script continue running until it hits the next breakpoint

# Summary of useful keyboard shortcuts:

//TODO

# I want to do something - wat do? (Common objectives in reverse engineering)
Getting to the main function

Fun fact, the start locaton is not the actual main function(most of the time), typically it does stuff like setup registers/the stack etc... Odds are there is nothing intersting there. To find the main function use the seek command `s main`
# Debugging using Radare 2
