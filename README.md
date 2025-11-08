# System Monitor Tool

The System Monitor Tool is a simple and lightweight C++ terminal program that shows all running processes in real time. It helps you monitor CPU usage, memory usage, and manage processes easily from the terminal. You can kill, suspend, resume, or view details of any running process. It displays the total number of processes, CPU and memory usage, and supports sorting by CPU, memory, or process ID. The interface is built using the ncurses library, which gives it a clean and simple text-based display. To use this tool, you need Ubuntu or Linux (or WSL on Windows) with a g++ compiler (C++17 or newer) and the ncurses library. Install them using:  
sudo apt update  
sudo apt install g++ libncurses5-dev libncursesw5-dev  
Once installed, you can build and run the program easily. You can compile it directly with:  
g++ -std=c++17 -O2 -o system_monitor_tool system_monitor_tool.cpp -lncurses  
and then run it using:  
sudo ./system_monitor_tool  
You can also use the included Makefile for a faster setup. Just type:  
make && sudo make run  
The Makefile content used the MakeFile

After running, the tool shows all processes with their PID, user, CPU and memory usage, and name. You can scroll using the up and down arrow keys. Press K to kill a process, S to suspend it, R to resume it, D to view details, O to sort by CPU usage, M to sort by memory usage, P to sort by PID, and Q to quit the program. A sample output looks like this:  
=== SYSTEM MONITOR TOOL ===  
CPU: 5.8%   Memory: 289.6 MB   Processes: 39  
PID       USER           CPU(%)       MEMORY(MB)        NAME  
482       soumyajit        8.3            20.3           python3  
487       soumyajit        6.2            15.1           yes  
[K] Kill  [S] Suspend  [R] Resume  [D] Details  [O] Sort CPU  [M] Sort Mem  [P] Sort PID  [Q] Quit  
The tool works by reading live process data from the /proc directory in Linux, calculating CPU and memory usage, and displaying it using ncurses for a smooth terminal interface. You can easily control processes in real time without needing any external task manager.  
