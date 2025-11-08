# System-Monitor-Tool
System Monitor Tool

The System Monitor Tool is a simple C++ terminal-based program that shows running processes in real time.
It allows you to view CPU usage, memory usage, and process information, as well as kill, suspend, resume, or inspect processes directly from the terminal.

Features

Displays all running processes live

Shows CPU usage, memory usage, and total process count

Allows process control (kill, suspend, resume)

Displays detailed process information

Sorting by CPU usage, memory usage, or PID

Clean text-based interface using the ncurses library

Requirements

Ubuntu or Linux (or WSL on Windows)

g++ compiler (C++17 or later)

ncurses library

Install ncurses if not already installed:

sudo apt update
sudo apt install libncurses5-dev libncursesw5-dev

How to Build and Run
Using g++ manually:
g++ -std=c++17 -O2 -o system_monitor_tool system_monitor_tool.cpp -lncurses
sudo ./system_monitor_tool

Using the Makefile:

A Makefile is included with this project.
You can build, run, and clean the project easily using these commands:

make          # Compile the program
sudo make run # Run the tool
make clean    # Remove build files
