# System Monitor Tool

The System Monitor Tool is a simple and lightweight C++ terminal program that shows all running processes in real time. It helps you monitor CPU usage, memory usage, and manage processes easily from the terminal. You can kill, suspend, resume, or view details of any running process. It displays the total number of processes, CPU and memory usage, and supports sorting by CPU, memory, or process ID. The interface is built using the ncurses library, which gives it a clean and simple text-based display. To use this tool, you need Ubuntu or Linux (or WSL on Windows) with a g++ compiler (C++17 or newer) and the ncurses library. Install them using: 

# Build setup:
sudo apt update  
sudo apt install g++ libncurses5-dev libncursesw5-dev  

# Run directly: 
g++ -std=c++17 -O2 -o system_monitor_tool system_monitor_tool.cpp -lncurses  
and then run it using:  
sudo ./system_monitor_tool  

# Run Using makefile: 
make && sudo make run  

After running, the tool shows all processes with their PID, user, CPU and memory usage, and name. You can scroll using the up and down arrow keys. Press K to kill a process, S to suspend it, R to resume it, D to view details, O to sort by CPU usage, M to sort by memory usage, P to sort by PID, and Q to quit the program. 
